<template>
  <v-app>
    <v-content>
      <v-container fluid>
        <h1 class="text-center mb-6 ">Vuetify</h1>
        <transition-group appear name="cards">
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
      items: [1, 2, 3, 4, 5, 6, 7]
    }
  }
}
</script>

<style lang="scss" scoped>
.cards-enter {
  opacity: 0;
}
.cards-enter-active {
  transition: 1s;
}
</style>
