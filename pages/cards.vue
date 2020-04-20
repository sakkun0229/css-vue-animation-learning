<template>
  <div class="container">
    <transition appear name="slide-in">
      <h1 class="title">Cards example</h1>
    </transition>
    <!-- <transition-group appear name="slidIn" class="grid" tag="div"> -->
    <div class="grid">
      <div v-for="item in items" :key="item.id" class="card">{{ item }}</div>
    </div>
    <!-- </transition-group> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3, 4, 5]
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  background-color: #111;
  min-height: 100vh;
  color: #fff;
  text-align: center;
  // display: flex;
  // justify-content: center;
  // flex-direction: column;
  // align-items: center;
}

.title {
  font-size: 3rem;
  padding: 10px;
  margin-bottom: 30px;
}

.card {
  height: 160px;
  // width: 200px;
  background-color: #fff;
}

.grid {
  display: grid;
  grid-gap: 10px;
  // grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  grid-template-columns: repeat(2, 1fr);
}

.slide-in-enter {
  opacity: 0;
  transform: scale(0.5);
}
.slide-in-enter-active {
  transition: 0.4s ease;
}
</style>
