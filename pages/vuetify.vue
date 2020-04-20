<template>
  <v-app>
    <v-content>
      <v-container fluid>
        <h1 class="text-center mb-6 ">Vuetify</h1>
        <transition-group appear name="cards" @before-enter="beforeEnter" @after-enter="afterEnter">
          <v-card class="mx-auto mb-2" color="#26c6da" dark max-width="400" v-for="item in items" :key="item">
            <v-card-title>
              <v-icon large left>
                mdi-twitter
              </v-icon>
              <span class="title font-weight-light">Twitter</span>
            </v-card-title>
            <v-card-text class="headline font-weight-bold">
              "Turns out semicolon-less style is easier and safer in TS because most gotcha edge cases are type invalid
              as well."
            </v-card-text>
          </v-card>
        </transition-group>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: []
    }
  },
  mounted() {
    for (let i = 0; i < 7; i++) {
      setTimeout(() => {
        this.items.push(i)
      }, i * 200)
    }
  },
  methods: {
    beforeEnter(el) {
      // el.style.transitionDelay = 100 * parseInt(el.dataset.index, 10) + 'ms'
      console.log('before Enter')
    },

    afterEnter(el) {
      // el.style.transitionDelay = ''
      console.log('after Enter')
    }
  }
}
</script>

<style lang="scss" scoped>
.cards-enter {
  opacity: 0;
  transform: scale(0.8) translateX(100%);
}
.cards-enter-active {
  transition: 0.4s;
}
</style>
