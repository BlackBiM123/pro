<template>
  <div class="spline-wrapper">
    <div class="spline-container">
      <Vue3Spline
          :scene="{
        url: 'https://prod.spline.design/V3Jaj7YMQs7YIUAk/scene.splinecode',
        width: 1064,
        height: 1044
      }"
      />
    </div>
  </div>
</template>

<script>
import { Vue3Spline } from 'vue3-spline'

export default {
  name: "spline-animation",
  components: {
    Vue3Spline,
  },
}
</script>

<style lang="scss" scoped>
.spline-wrapper{
  position: absolute;
  left:0;
  top:0;
  width:100%;
  display:flex;
  justify-content: flex-end;
  align-items: flex-end;
  height:calc(100vh - 100px);

  .spline-container{
    width:880px;
    height:863px;
    margin-right:-150px;
  }
  canvas{
    pointer-events: none;
    width:100% !important;
    height:auto !important;
  }
}
</style>
