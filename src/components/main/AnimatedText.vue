
<template>
  <div class="typewriter">
    <span class="marker-text">Pro</span>
    <span>{{ displayText }}</span><span class="cursor">|</span>
  </div>
</template>

<script setup>
/* eslint-disable */
import { ref, onMounted } from 'vue';
const props = defineProps({
  texts: {
    type: Array,
  }
});
const speed = 50;
const delSpeed = 100;
const delayBeforeDeleting = 3000;

const displayText = ref('');
let currentTextIndex = 0;
let currentCharIndex = 0;
let deleting = false;

const type = () => {
  const currentText = props.texts[currentTextIndex];

  if (deleting) {
    if (currentCharIndex > 0) {
      displayText.value = currentText.substring(0, currentCharIndex - 1);
      currentCharIndex--;
      setTimeout(type, delSpeed);
    } else {
      deleting = false;
      currentTextIndex = (currentTextIndex + 1) % props.texts.length;
      setTimeout(type, speed);
    }
  } else {
    if (currentCharIndex < currentText.length) {
      displayText.value = currentText.substring(0, currentCharIndex + 1);
      currentCharIndex++;
      setTimeout(type, speed);
    } else {
      deleting = true;
      setTimeout(type, delayBeforeDeleting);
    }
  }
};

onMounted(() => {
  type();
});
</script>

<style scoped lang="scss">
.typewriter {
  overflow: hidden;
  display: inline-block;
  color:#FFF;
  font-family: "Roboto", sans-serif;
  font-weight: 700;
  font-style: normal;
  font-size:70px;
  line-height: 70px;
  white-space: normal; /* Позволяет тексту переноситься на новую строку */
  word-break: keep-all; /* Переносит слова на новую строку, если они слишком длинные */
  min-height: 150px;
}
.marker-text{
  font-size:70px;
  transform: translateY(-18px);
  display:inline;
  margin-right:20px;
}
.typewriter .cursor {
  animation: blink 0.7s step-end infinite;
  font-size:75px;
}

@keyframes blink {
  from, to { color: #4361EE }
  50% { color: black; }
}
@media(max-width: 767px){
  .typewriter {
    font-size: 45px;
    line-height: 41px;
    max-width:500px;
    display:block;
    min-height: 110px;
    margin:0 auto;
    .marker-text {
      font-size: 45px;
      line-height: 41px;
      margin-right:10px;
    }
    .cursor{
      font-size: 55px;
      position: absolute;
    }
  }
}
@media(max-width: 500px){
  .typewriter {
    font-size: 38px;
    line-height: 37px;
    max-width:320px;
    width:100%;
    min-height: 130px;
    text-align: left;
    margin:0;
    .marker-text {
      font-size: 38px;
      line-height: 37px;
      margin-right:10px;
      display:block;
      transform: none;
    }
    .cursor{
      font-size: 55px;
      position: absolute;
    }
  }
}

</style>
