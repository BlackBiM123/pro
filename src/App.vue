
<template>
  <header :class="{'fixed': isFixed, 'visible': isVisible, 'opened': menuActive}">
    <div class="logo"><span class="title"><span class="marker-text">prof</span>depo</span></div>
    <ul>
      <li :class="{ active: activeSection === 'home' }"><a href="#home" @click.prevent="scrollToSection('home')">Главная</a></li>
      <li :class="{ active: activeSection === 'about' }"><a href="#about" @click.prevent="scrollToSection('about')">О нас</a></li>
      <li :class="{ active: activeSection === 'products' }"><a href="#products" @click.prevent="scrollToSection('products')">Продукты</a></li>
      <li :class="{ active: activeSection === 'blog' }"><a href="#blog" @click.prevent="scrollToSection('blog')">Блог</a></li>
    </ul>
    <div class="menu-toggle" @click="menuActive = !menuActive">
      <span>
        <span v-if="!menuActive">Меню</span>
        <span v-else>Закрыть</span>
      </span>
      <img v-if="!menuActive"  src="@/assets/img/menu.svg" alt="">
      <img v-else src="@/assets/img/close.svg" alt="">
    </div>
  </header>
  <section class="spline" id="home">
    <div class="container">
      <div class="main-text">
        <div class="top">
          <animated-text :texts="['современный бизнес', 'автоматизацию и продуктивность']" />
          <p>Рабочие инструменты для современного бизнеса. Увеличиваем эффективность специалистов, позволяя зарабатывать больше.</p>
          <button type="button" class="btn pro-btn">Наши <span class="marker-text">pro</span>дукты</button>
        </div>
        <div class="note"><img src="@/assets/img/trade.svg">Искусственный Интеллект </div>
      </div>
      <spline />
    </div>
  </section>
  <section id="about" class="about">
    <div class="container">
      <p class="about-text"><span class="start-offset"></span>Мы <span class="marker-text">prof</span>depo, динамичная команда, стремящаяся революционизировать рабочие процессы в бизнесе с помощью передовых технологий, и программных решений, ориентированных на оптимальный пользовательский опыт. </p>
      <div class="about-items-wrapper">
        <div class="about-item">
          <div class="icon">
            <img src="./assets/img/about-icon1.svg" alt="">
          </div>
          <span class="title">Автоматизация и продуктивность </span>
          <div class="bottom-text">
            <p>Автоматизация рутинных задач позволяет руководителям и специалистам сосредоточиться на важном. Экономия ресурсов и времени делает бизнес конкурентным </p>
          </div>
        </div>
        <div class="about-item accent">
          <div class="icon">
            <img src="./assets/img/trade.svg" alt="">
          </div>
          <span class="title">Человек + ИИ</span>
          <div class="bottom-text">
            <p>Мы PRO людей. Наша цель - не заменить, а помочь специалистам. Наши продукты обрабатывают большой объем данных, человек принимает стратегические решения.</p>
          </div>
        </div>
        <div class="about-item">
          <div class="icon">
            <img src="./assets/img/about-icon3.svg" alt="">
          </div>
          <span class="title">Собственный опыт - путем проб и ошибок</span>
          <div class="bottom-text">
            <p>Наши продукты были созданы основываясь на многолетний опыт работы в сложном и конкурентном мире консалтинга. Мы начали с решения самых важных проблем - персонала и продуктивности.</p>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="bg bg-1"></section>
  <section id="products" class="products">
    <div class="container">
      <span class="title">Наши <span class="marker-text">pro</span>дукты</span>
      <p class="pre-title">Приветствуем вас! Мы Profdepo, динамичная команда, стремящаяся революционизировать рабочие процессы в бизнесе с помощью передовых технологий, и программных решений, ориентированных на оптимальный пользовательский опыт. </p>
      <div class="prod-items-wrapper">
        <div class="prod-item accent">
          <span class="note">Менеджер Переписки</span>
          <span class="title">profdepo <span class="marker-text">TEAM</span></span>
          <ul>
            <li>
              <span class="icon">
                <img src="@/assets/img/prod-icon1.svg" alt="">
              </span>
              <span>Используй в своих проектах для анализа коммуникации в рабочих чатах.</span>
            </li><li>
              <span class="icon">
              <img src="@/assets/img/prod-icon2.svg" alt="">
              </span>
            <span>Изучает переписку в проектных чатах. Выявляет ключевые темы и паттерны общения.</span>
          </li><li>
              <span class="icon">
                <img src="@/assets/img/prod-icon3.svg" alt="">
              </span>
            <span>Oпределяет эффективность взаимодействия членов команды.</span>
          </li><li>
              <span class="icon">
                <img src="@/assets/img/prod-icon4.svg" alt="">
              </span>
            <span>Получи отчет о продуктивности и проблемах команды и рекомендации к их решению. </span>
          </li>
          </ul>
          <button type="button" class="btn pro-btn">Подробнее <span class="marker-text">Pro</span></button>
        </div>
        <div class="prod-item">
          <span class="note">Управление Персоналом</span>
          <span class="title">profdepo <span class="marker-text">HR</span></span>
          <ul>
            <li>
              <span class="icon">
                <img src="@/assets/img/prod-icon1-1.svg" alt="">
              </span>
              <span>Автоматизация рутинных HR-процессов. Оптимизация расходов на управление кадрами.</span>
            </li><li>
              <span class="icon">
              <img src="@/assets/img/prod-icon1-2.svg" alt="">
              </span>
            <span>Увеличивает продуктивность руководителей, HR специалистов и рекрутеров. </span>
          </li><li>
              <span class="icon">
                <img src="@/assets/img/prod-icon1-3.svg" alt="">
              </span>
            <span>Анализ компетенций кандидатов оценка эффективности сотрудников</span>
          </li><li>
              <span class="icon">
                <img src="@/assets/img/prod-icon1-4.svg" alt="">
              </span>
            <span>Решай все задачи по работе с персоналом быстрее, точнее и эффективней.   </span>
          </li>
          </ul>
          <button type="button" class="btn pro-btn dark">Подробнее <span class="marker-text">Pro</span></button>
        </div>
        <div class="prod-item">
          <span class="note"> Агрегатор Вакансий </span>
          <span class="title">profdepo <span class="marker-text">WORK</span></span>
          <ul>
            <li>
              <span class="icon">
                <img src="@/assets/img/prod-icon2-1.svg" alt="">
              </span>
              <span>Найди работу, или специалиста для решения задач своего бизнеса.</span>
            </li><li>
              <span class="icon">
              <img src="@/assets/img/prod-icon2-2.svg" alt="">
              </span>
            <span>Интеграция всех наших продуктов.  </span>
          </li><li>
              <span class="icon">
                <img src="@/assets/img/prod-icon2-3.svg" alt="">
              </span>
            <span>Присоединяйтесь к растущему сообществу профессионалов. Обменивайтесь опытом, налаживайте связи и развивайтесь вместе с нами.</span>
          </li>
          </ul>
          <button type="button" class="btn pro-btn disabled">Скоро появится</button>
        </div>
        <div class="prod-item">
          <span class="note">ИИ Сотрудники</span>
          <span class="title">profdepo <span class="marker-text">Staff</span></span>
          <ul>
            <li>
              <span class="icon">
                <img src="@/assets/img/prod-icon3-1.svg" alt="">
              </span>
              <span>Найми ИИ сотрудника для решения задач бизнеса.</span>
            </li><li>
              <span class="icon">
              <img src="@/assets/img/prod-icon3-2.svg" alt="">
              </span>
            <span>Наши ИИ сотрудники не требуют выходных и постоянно совершенствуются, обеспечивая высокую эффективность и экономию ресурсов.</span>
          </li><li>
              <span class="icon">
                <img src="@/assets/img/prod-icon3-3.svg" alt="">
              </span>
            <span>Отличный выбор для малого бизнеса.</span>
          </li>
          </ul>
          <button type="button" class="btn pro-btn disabled">Скоро появится</button>
        </div>
      </div>
    </div>
  </section>
  <section class="bg bg-2"></section>
  <section id="blog" class="blog">
    <div class="container">
      <span class="title">Блог</span>
      <div class="blog-wrapper">
        <div class="blog-item">
          <div class="img">
            <img src="@/assets/img/blog1.png" alt="">
          </div>
          <div class="info">
            <span class="name">Человек + ИИ</span>
            <p class="description">Мы PRO людей. Наша цель - не заменить, а помочь специалистам. Наши продукты обрабатывают большой объем данных, человек принимает...</p>
            <button type="button" class="btn pro-btn">Подробнее <span class="marker-text">Pro</span></button>
          </div>
        </div>
        <div class="blog-item">
          <div class="img">
            <img src="@/assets/img/blog2.png" alt="">
          </div>
          <div class="info">
            <span class="name">Человек + ИИ</span>
            <p class="description">Мы PRO людей. Наша цель - не заменить, а помочь специалистам. Наши продукты обрабатывают большой объем данных, человек принимает...</p>
            <button type="button" class="btn pro-btn">Подробнее <span class="marker-text">Pro</span></button>
          </div>
        </div>
        <div class="blog-item">
          <div class="img">
            <img src="@/assets/img/blog3.png" alt="">
          </div>
          <div class="info">
            <span class="name">Человек + ИИ</span>
            <p class="description">Мы PRO людей. Наша цель - не заменить, а помочь специалистам. Наши продукты обрабатывают большой объем данных, человек принимает...</p>
            <button type="button" class="btn pro-btn">Подробнее <span class="marker-text">Pro</span></button>
          </div>
        </div>
      </div>
    </div>
  </section>
  <footer>
    <div class="container flex">
        <div class="left">
          <span class="title"><span class="marker-text">prof</span>depo</span>
          <p>Рабочие инструменты для современного бизнеса. Увеличиваем эффективность специалистов, позволяя зарабатывать больше.</p>
          <button type="button" class="btn pro-btn">Cтать <span class="marker-text">pro</span></button>
        </div>
        <div class="right">
          <ul>
            <li>Для Pro</li>
            <li><a href="#">Главная</a></li>
            <li><a href="#">О Нас</a></li>
            <li><a href="#">Контакты</a></li>
            <li><a href="#">Продукты </a></li>
            <li><a href="#">Блог</a></li>
          </ul>
          <ul>
            <li>Соц Сети</li>
            <li><a href="#">Facebook </a></li>
            <li><a href="#">LinkedIn</a></li>
            <li><a href="#">Twitter</a></li>
            <li><a href="#">YouTube </a></li>
            <li><a href="#">Instagram</a></li>
          </ul>
        </div>
    </div>
    <div class="container">
      <span class="bottom">©2024 Profdepo </span>
    </div>
  </footer>
</template>
<script setup>
/* eslint-disable */
import Spline from './components/main/Spline.vue'
import AnimatedText from "@/components/main/AnimatedText";
import { ref, onMounted, onUnmounted } from 'vue'

const sections = ['home', 'about', 'products', 'blog']
const activeSection = ref('home')
const menuActive = ref(false)
const isVisible = ref(true)   // Изначально header виден
const isFixed = ref(false)    // Фиксация header

let lastScrollY = window.scrollY

// Функция для плавного скролла
const scrollToSection = (sectionId) => {
  const element = document.getElementById(sectionId)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
  menuActive.value = false
}

// Отслеживание направления прокрутки
const handleScroll = () => {
  if (menuActive.value) return
  const currentScrollY = window.scrollY

  // Если прокручиваем вверх — показываем header
  if (currentScrollY < lastScrollY) {
    isVisible.value = true
    if (currentScrollY <= 100) {
      isFixed.value = true
    } else {
      isFixed.value = false
    }
  }
  // Если прокручиваем вниз — прячем header
  else if (currentScrollY > lastScrollY) {
    isVisible.value = false
    isFixed.value = false
  }

  lastScrollY = currentScrollY

  // Обновляем активную секцию
  const sectionOffsets = sections.map(section => {
    const element = document.getElementById(section)
    return {
      id: section,
      offset: element ? element.offsetTop : 0,
      height: element ? element.offsetHeight : 0
    }
  })

  const scrollPosition = window.scrollY + window.innerHeight / 2

  const currentSection = sectionOffsets.find(section =>
      scrollPosition >= section.offset && scrollPosition < section.offset + section.height
  )

  if (currentSection) {
    activeSection.value = currentSection.id
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>
<style lang="scss">
header{
  background: #000;
  color:#fff;
  padding:15px 35px;
  display:flex;
  align-items: center;

  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  transition: top 0.3s, opacity 0.3s;
  z-index: 10;
  opacity: 1;

  &:not(.visible) {
    top: -100px;
    opacity: 0;
  }
  &.fixed {
    position: fixed;
    top: 0;
  }
  .logo{
    line-height:24px;
  }
  .title{
    font-size:20px;
    font-family: "Roboto", sans-serif;
    font-weight: 700;
    margin-right:30px;
  }
  ul{
    list-style: none;
    padding:0;
    display:flex;
    margin:0 !important;
    li{
      margin:0 30px 0 0;
      font-size:16px;
      font-weight: 600;
      opacity: 0.6;
      transition: opacity 0.3s;
      &:hover,
      &.active{
        opacity:1;
      }
    }
    a{
      text-decoration: none;
      color:#FFF;
    }
  }
  .menu-toggle{
    align-items: center;
    display:none;
  }
}
.spline{
  box-sizing: border-box;
  background: #000;
  height:100vh;
  padding-top:150px;
  overflow: hidden;
  .container{
    height:100%;
  }
}
.main-text{
  max-width:680px;
  color:#FFF;
  position: relative;
  z-index: 1;
  display:flex;
  flex-direction: column;
  height:100%;
  .top{
    flex-grow: 1;
  }
  .note{
    padding-bottom:70px;
    display:flex;
    align-items: center;
    img{
      margin-right:10px;
    }
  }
  p{
    font-weight:300;
    font-size:18px;
    color:#B9B9B9;
    margin:10px 0 20px;
  }

}
.about{
  padding:50px 0 70px;
  .about-text{
    font-family: "Roboto", sans-serif;
    font-size:30px;
    font-weight:600;
    max-width:1220px;
    margin:0 auto 50px;
    padding-bottom:30px;
    background-image: url('@/assets/img/about-underline.svg');
    background-repeat: no-repeat;
    background-position: 70% 100%;
    .start-offset{
      padding-left:100px;
    }
    .marker-text{
      margin-right: 2px;
    }
  }
  .about-items-wrapper{
    display:flex;
    justify-content: space-between;
    align-items: center;
    padding:0 50px;
    .about-item{
      width:358px;
      background-color: #000;
      min-height:515px;
      border-radius: 32px;
      padding:25px;
      box-sizing: border-box;
      display:flex;
      flex-direction: column;
      &:first-child{
        background-image: url('@/assets/img/about-item1.png');
        background-repeat: no-repeat;
        background-position: center;
      }
      &:last-child{
        background-image: url('@/assets/img/about-item3.png');
        background-repeat: no-repeat;
        background-position: center;
      }
      &.accent{
        width:395px;
        height:547px;
        background-color: #67AAD5;
        background-image: url('@/assets/img/about-item2.png');
        background-repeat: no-repeat;
        background-size: cover;
        .bottom-text{
          color:#FFF;
          padding-bottom:30px;
        }
      }
      .icon{
        width:27px;
        height:27px;
        img{
          width:100%;
        }
      }
      .title{
        font-size:24px;
        line-height: 28px;
        color:#FFF;
        font-weight: 700;
        margin-top:10px;
        display:block;
      }
      .bottom-text{
        display:flex;
        align-items: flex-end;
        flex-grow: 1;
        color:#B9B9B9;
        font-size:14px;
        font-weight: 400;
        line-height: 16px;
      }
    }
  }
}
.bg{
  width:100%;
  display:flex;
  background-color:#000;
  background-repeat: no-repeat;
  &.bg-1{
    height:841px;
    background-position: center 20%;
    background-image: url('@/assets/img/bg-image1.png');
    background-size: 100% auto;
  }&.bg-2{
    height:810px;
    background-position: center 0%;
    background-image: url('@/assets/img/bg-image2.png');
    background-size: 100% auto;
  }
}
.products{
  padding:80px 0;
  .title{
    font-size:70px;
    font-weight: 700;
    line-height: 57px;
    text-align: center;
    display:block;
  }
  .pre-title{
    font-size:16px;
    color:#737373;
    line-height: 18px;
    font-weight: 400;
    text-align:center;
    max-width:780px;
    margin: 20px auto 50px;
  }
  .prod-items-wrapper{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(2, 1fr);
    grid-column-gap: 20px;
    grid-row-gap: 20px;
    .prod-item{
      border-radius: 32px;
      background: #F7F7F7;
      padding:30px 25px;
      &.accent{
        background: #000;
        color:#FFF;
        .note{
          color:#A1B1F7;
        }
        ul{
          color:#B9B9B9;
        }
      }
      .title{
        text-align: left;
        font-size:55px;
        margin:40px 0 20px;
      }
      .note{
        color:#737373;
      }
      ul{
        list-style: none;
        padding:0;
        margin:30px 0;
        min-height:180px;
        li{
          display:flex;
          margin-bottom:10px;
          line-height: 16px;
          font-size:14px;
          font-weight: 400;
          font-family: "Roboto", sans-serif;
          .icon{
            margin-right:5px;
            display:block;
            transform: translateY(-2px);
          }
        }
      }
      button{
        margin-left:auto;
        &.disabled{

        }
      }
    }
  }
}
.blog{
  background: #000;
  color:#FFF;
  padding:80px 0;
  .title{
    font-size:70px;
    font-weight: 700;
    line-height: 57px;
    text-align: center;
    display:block;
    margin:0 0 80px;
  }
  .blog-wrapper{
    display: flex;
    justify-content: space-around;
    .blog-item{
      border-radius: 32px;
      background: #FFF;
      padding:0;
      margin:0 10px;
      border-radius: 32px;
      overflow: hidden;
      width:400px;
      .img{
        width:100%;
        img{
          width:100%;
        }
      }
      .info{
        padding:20px;
        color:#000;
        .name{
          color:#191C1F;
          font-size:24px;
          line-height: 28px;
        }
        .description{
          font-size:16px;
          line-height:18px;
          color:#66717D;
          display: -webkit-box;
          -webkit-line-clamp: 2;
          -webkit-box-orient: vertical;
          overflow: hidden;
          text-overflow: ellipsis;
          max-height: 36px; /* высота для двух строк */
          margin-bottom:40px;
        }
        .btn{
          color:#FFF;
          background: #000;
          margin-left:auto;
        }
      }
    }
  }
}
footer{
  background: #000;
  color:#FFF;
  padding-top:80px;
  .container.flex{
    display:flex;
    .left, .right{
      width:50%;
    }
    .left{
      width:60%;
      .title{
        font-size:55px;
        font-family: "Roboto", sans-serif;
        font-weight: 700;
      }
      p{
        font-size:16px;
        line-height: 24px;
        color:#B9B9B9;
        max-width: 515px;
      }
      button{
        background: #E8ECFD;
      }
    }
    .right{
      display:flex;
      width:40%;
      ul{
        padding:0;
        width:50%;
        list-style: none;
        li{
          margin-bottom:20px;
          font-weight: 600;
        }
      }
      a{
        font-weight: 400;
        transition: color 0.3s;
        color:#75808A;
        text-decoration: none;
        font-size: 16px;
        line-height: 24px;
        &:hover{
          color:#FFF;
        }
      }
    }
  }
  .bottom{
    display:flex;
    padding:80px 0;
    font-size:14px;
    color:#9D9D9D;
  }
}
@media(max-width:1440px){
  .bg{
    width:100%;
    display:flex;
    background-color:#000;
    background-repeat: no-repeat;
    &.bg-1{

      background-position: center 20%;
      background-image: url('@/assets/img/bg-image1.png');
      background-size: auto 100%;
    }&.bg-2{

       background-position: center 0%;
       background-image: url('@/assets/img/bg-image2.png');
       background-size: auto 100%;
     }
  }
}
@media(max-width: 1270px){
  header{
    padding-left:15px;
    padding-right:15px;
  }
  .about{
    .about-items-wrapper{
      padding:0
    }
  }
}
@media(max-width: 1199px){
  .spline{
    padding-top:100px;
  }
  .spline-wrapper .spline-container{
      width:600px !important;
      height:590px !important;
      margin: 0 !important;
  }
  .about{
    padding:20px 0 50px;
    .about-text{
      font-size:24px;
      font-weight:600;
      max-width:100%;
      padding-bottom:40px;
      background-position: left 100%;
      .start-offset{
        padding-left:100px;
      }
    }
    .about-items-wrapper{
      display:flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      padding:0 50px;
      .about-item{
        width:100% !important;
        background-color: #000;
        height:auto !important;
        border-radius: 32px;
        padding:25px;
        box-sizing: border-box;
        display:flex;
        flex-direction: column;
        align-items: center;
        &:first-child{
          background-image: url('@/assets/img/about-item1.png');
          background-repeat: no-repeat;
          background-position: center;
        }
        &:last-child{
          background-image: url('@/assets/img/about-item3.png');
          background-repeat: no-repeat;
          background-position: center;
        }
        &.accent{
          background-size: 100% auto;
          background-position: center;
          margin:30px 0;
        }
        .icon{
          width:27px;
          height:27px;
          img{
            width:100%;
          }
        }
        .title{
          max-width:300px;
          text-align: center;
        }
        .bottom-text{
          display:flex;
          align-items: flex-end;
          max-width:80%;
          text-align: center;
          flex-grow: 1;
          color:#B9B9B9;
          font-size:14px;
          font-weight: 400;
          line-height: 16px;
        }
      }
    }
  }
  .bg{
    &.bg-1{
      height:700px;
    }&.bg-2{
       height:700px;

     }
  }
  .products{
    padding:30px 0;
    .title{
      font-size: 48px;
      line-height:48px;
    }
    .prod-items-wrapper{
      .prod-item{
        .title{
          font-size:35px;
        }
        .note{
          font-size:14px;
        }
      }
    }
  }
  .blog{
    background: #000;
    color:#FFF;
    padding:40px 0;
    .title{
      font-size: 48px;
      line-height:48px;
      margin:0 0 80px;
    }
    .blog-wrapper{
      display: flex;
     flex-direction: column;
      justify-content: center;
      align-items: center;
      .blog-item{
        width:100%;
        max-width:100%;
        margin-bottom:20px;
        .img{
          width:100%;
          background: url('@/assets/img/blog-main-bg.png');
          display:flex;
          justify-content: center;
          align-items: center;
          img{
            height:100%;
            width:auto;
            margin:0 auto;
          }
        }
        .info{
          padding:20px;
          color:#000;
          .name{
            color:#191C1F;
            font-size:24px;
            line-height: 28px;
          }
          .description{
            margin-bottom: 10px;
          }
          .btn{
            width:100%;
          }
        }
      }
    }
  }
  footer{
    padding-top:0;
    .bottom{
      padding:40px 0;
    }
    .container.flex .right ul{
      text-align: right;
    }
  }
}
@media(max-width: 767px){

  header{
    align-items: flex-start;
    flex-wrap: wrap;
    justify-content: space-between;
    height: 60px;
    overflow: hidden;
    transition: 0.3s;
    &.opened{
      height: 100vh;
    }
    .menu-toggle{
      display:flex;
      cursor: pointer;
      user-select: none;
      img{
        margin-left:5px;
      }
    }
    ul{
      order:1;
      min-width:100%;
      display:flex;
      flex-direction: column;
      align-items: center;
      padding:100px 0;
      li{
        width:120px;
        min-height:60px;
        display:flex;
        align-items: center;
        justify-content: center;
        background-size: contain;
        background-repeat: no-repeat;
        &.active{
          background-image: url('@/assets/img/menu-accent.svg');
        }
      }
    }
  }
  .spline{
    padding-top:60px;
    .main-text{
      box-sizing: border-box;
      max-width: none;
      width:100%;
      text-align: center;
      p{
        font-size:16px;
        max-width:500px;
        margin: 0 auto 20px;
      }
      button{
        margin:10px auto;
      }
      .note{
        width: 100%;
        justify-content: center;
        padding-bottom:20px;
        font-size:14px;
      }
    }
    .spline-wrapper{
      padding-top:220px;
      justify-content: center;
      align-items: center;
      .spline-container{
        width:75% !important;
        height:auto !important;
        margin: 0 !important;
      }
    }
  }
  .about{
    padding:20px 0 50px;
    .about-text{
      font-size:20px;
      font-weight:600;
      max-width:100%;
      padding-bottom:30px;
      background-position: left 100%;
      background-size: 70% auto;
      .start-offset{
        padding-left:100px;
      }
    }
    .about-items-wrapper{
      display:flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      padding:0px;
      .about-item{
        width:100% !important;
        background-color: #000;
        height:auto !important;
        border-radius: 32px;
        padding:25px;
        box-sizing: border-box;
        display:flex;
        flex-direction: column;
        align-items: center;
        &:first-child{
          background-image: url('@/assets/img/about-item1.png');
          background-repeat: no-repeat;
          background-position: center;
        }
        &:last-child{
          background-image: url('@/assets/img/about-item3.png');
          background-repeat: no-repeat;
          background-position: center;
        }
        &.accent{
          background-size: 100% auto;
          background-position: center;
          margin:30px 0;
        }
        .icon{
          width:27px;
          height:27px;
          img{
            width:100%;
          }
        }
        .title{
          max-width:300px;
          text-align: center;
        }
        .bottom-text{
          display:flex;
          align-items: flex-end;
          max-width:80%;
          text-align: center;
          flex-grow: 1;
          color:#B9B9B9;
          font-size:14px;
          font-weight: 400;
          line-height: 16px;
        }
      }
    }
  }
  .bg{
    &.bg-1{
      height:600px;
    }&.bg-2{
       height:600px;
     }
  }
  .products{
    padding-top:10px;
    .title{
      text-align: left;
    }
    .pre-title{
      margin-bottom:30px;
      text-align: left;
    }
    .prod-items-wrapper{
      grid-template-columns: repeat(1, 1fr);
      grid-template-rows: repeat(1, 1fr);
      grid-column-gap: 20px;
      grid-row-gap: 20px;
      .prod-item{
        .title, .note{
          display:block;
          text-align: center;
        }
        .title{
          margin:20px 0 0;
        }
        ul{
          margin-top:10px;
          min-height: 0;
        }
        button{
          width:100%;
        }
      }
    }
  }
  footer{
    .container.flex{
      flex-direction: column;
      align-items: center;
      .left{
        width:100%;
        flex-direction: column;
        align-items: center;
        display:flex;
        margin:0 auto;
        max-width:350px;
        text-align: center;
        p{
          margin-top: 5px;
        }
      }

      .right{
        margin-top:50px;
        width:100%;
        max-width:450px;
        display:flex;
        justify-content: space-around;
        ul{
          width:auto;
          text-align: left;
        }
      }
    }
  }
}
@media(max-width: 500px){
  header{
    padding-left:15px;
    padding-right:15px;
  }
  .spline {
    padding-top:80px;
    .main-text {
      text-align: left;
      button{
        margin:0;
      }
    }
  }
  .about{
    padding:20px 0 30px;
    .about-text{
      font-size:18px;
      background-size: 90% auto;
    }
    .about-items-wrapper{
      .about-item{
        .bottom-text{
          max-width:none;
        }
      }
    }
  }
  .bg{
    &.bg-1{
      height:550px;
    }&.bg-2{
       height:550px;
     }
  }
  .products{
    .prod-items-wrapper .prod-item .title {
      margin: 20px auto 0;
      max-width: 70%;
      line-height: 40px;
    }
  }
}
</style>
