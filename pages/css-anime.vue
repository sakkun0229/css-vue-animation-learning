<template>
  <div class="container">
    <h1 class="title">{{ title }}</h1>

    <div class="sample1">
      <h2 class="subtitle">sample1</h2>
      <div class="box"></div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'CSS Animation sample'
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  background-color: #333;
  color: #fff;
  text-align: center;
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.title {
  font-size: 3rem;
  margin: 20px;
}
.subtitle {
  font-size: 2.4rem;
  margin: 20px;
}

.box {
  width: 200px;
  height: 200px;
  background-color: #fff;
  margin: 0 auto;
  position: relative;
  left: -100%;
  opacity: 0;
  animation: sample 1.2s 0.5s forwards;
}

@keyframes sample {
  0% {
    left: -100%;
    opacity: 0;
  }
  90% {
  }
  100% {
    left: 0%;
    opacity: 1;
  }
}
</style>
