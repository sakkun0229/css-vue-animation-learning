<template>
  <div class="vue">
    <transition appear name="title">
      <h1 class="title">{{ title }}</h1>
    </transition>

    <div class="wrapper">
      <div class="box animated-sample"></div>
    </div>
  </div>
</template>

<script>
import '@/assets/css/animate.css'

export default {
  data() {
    return {
      title: 'CSS & Vue Animation sample'
    }
  }
}
</script>

<style lang="scss" scoped>
// 共通パーツ
.vue {
  background-color: #111;
  min-height: 100vh;
  color: #fff;
  text-align: center;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.title {
  font-size: 3rem;
  margin: 20px;
}

.wrapper {
  margin-bottom: 60px;
}

.box {
  width: 200px;
  height: 200px;
  background-color: #fff;
  margin: 0 auto;
  position: relative;
  // left: -100%;
  // opacity: 0;
}
// 共通パーツ終わり

.title-enter {
  opacity: 0;
  transform: scale(0.5);
  // transform: scale(0.5) translateX(50%);
}
.title-enter-active {
  transition: 0.5s;
}

.animated-sample {
  // opacity: 0;
  // left: -100%;
  animation: sample 1.2s 0.5s forwards;
}

@keyframes sample {
  0% {
    left: -100%;
    opacity: 0;
  }
  100% {
    left: 0%;
    opacity: 1;
  }
}
</style>
