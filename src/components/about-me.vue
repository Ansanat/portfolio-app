<template>
  <div class="about-me">
    <div class="about-me-name"> {{name}} </div>
    <div class="about-me-spec"> {{spec}} </div>
    <div class="about-me-line"></div>
    <div class="about-me-info"> {{info}} </div>
    <div 
      class="about-me-about-me"
      v-for="item in aboutMeList" :key="item"
    >
      <i :class="'about-me-about-me-icon icon-' + item.icon"></i>
      <div class="about-me-about-me-item"> {{item.text}} </div>
    </div>
    <div class="about-me-line"></div>
  </div>
</template>

<script>
import '@/icons/style.css'

export default {
  name: 'AboutMe',
  props: {
  },
  data() {
    return {
      name: 'Виталий Колточихин',
      spec: 'Web-разработчик',
      info: 'Доброго времени суток! Меня зовут Виталий. Я занимаюсь профессиональной разработкой сайтов под ключ. О себе:',
      aboutMeList: [
        {
          icon: 'checkmark',
          text: 'Программист с высшим образованием'
        },
        {
          icon: 'checkmark',
          text: 'Действующий web-разработчик в аккредитованой IT-компании'
        },
        {
          icon: 'checkmark',
          text: 'Имею большой опыт создания и ведения сайтов для бизнеса'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.about-me {
  color: white;
  padding: 40px;

  &-name {
    font-size: 30px;
  }

  &-spec {
    font-size: 20px;
    opacity: 0.7;
  }

  &-line {
    width: 100%;
    height: 1px;
    background-color: white;
    margin-top: 10px;
  }

  &-info {
    margin-top: 10px;
    text-align: justify;
    font-size: 16px;
    opacity: 0.9;
  }

  &-about-me {
    display: flex;
    opacity: 0.9;
    margin-top: 10px;
    font-size: 15px;
    vertical-align: middle;

    &-icon {
      margin-left: 10px;
    }

    &-item {
      margin-left: 5px;
    }
  }
}
</style>
