<template>
  <section>
    <!-- <HomeHero/> -->
    <v-container>

  <v-card
    class="mx-auto mt-16"
    max-width="800"
  >
    <v-card-title class="text-h6 font-weight-regular justify-center">
      <v-avatar
        color="primary lighten-2"
        class="subheading white--text"
        size="72"
        v-text="step"
      ></v-avatar>
    </v-card-title>
    <v-card-title class="text-h6 text-sm-h4 font-weight-bold justify-center">
      <span>{{ currentTitle }}を教えて下さい</span>
    </v-card-title>

    <v-window class="my-16" v-model="step">
      <v-window-item :value="1">
        <v-card-text>
          <v-select
            class="text-h6 text-center"
            :items="number"
            label="生活人数"
            solo
            height="100"
            suffix="人"
            full-width
            item-disabled
          ></v-select>
          <span class="text-caption grey--text text--darken-1">
            <!-- This is the email you will use to login to your Vuetify account -->
          </span>
        </v-card-text>
      </v-window-item>

      <v-window-item :value="2">
        <v-card-text>
          <v-select
            class="text-h6 text-center"
            :items="number"
            label="生活人数"
            solo
            height="100"
            suffix="人"
            full-width
            item-disabled
          ></v-select>
          <span class="text-caption grey--text text--darken-1">
            <!-- This is the email you will use to login to your Vuetify account -->
          </span>
        </v-card-text>
      </v-window-item>

      <v-window-item :value="3">
        <div class="pa-4 text-center">
          <v-img
            class="mb-4"
            contain
            height="128"
            src="https://cdn.vuetifyjs.com/images/logos/v.svg"
          ></v-img>
          <h3 class="text-h6 font-weight-light mb-2">
            Welcome to Vuetify
          </h3>
          <span class="text-caption grey--text">Thanks for signing up!</span>
        </div>
      </v-window-item>
    </v-window>

    <v-divider></v-divider>

    <v-card-actions class="py-5">
      <v-btn
        :disabled="step === 1"
        text
        @click="step--"
      >
        Back
      </v-btn>
      <v-spacer></v-spacer>
      <v-btn
        :disabled="step === 3"
        color="primary"
        depressed
        @click="step++"
      >
        Next
      </v-btn>
    </v-card-actions>
  </v-card>
      
    </v-container>
  </section>
</template>

<script>
  import HomeHero from '@/components/HomeHero.vue'

  export default {
    name: 'Home',
    components: {
      HomeHero
    },
    data() {
      return {
        step: 1,
        number: [1, 2, 3, 4, 5, 6, 7, 8, 9, '10人以上']
      }
    },
    computed: {
      currentTitle () {
        switch (this.step) {
          case 1: return '生活人数'
          case 2: return '住居の広さ'
          default: return '住居の広さ'
        }
      },
    },
  }

</script>

<style scoped>
  section {
    background: -webkit-linear-gradient(top,#2a5dc5,#39a2af 260px,hsla(0,0%,100%,0) 265px);
  }
</style>