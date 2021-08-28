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
        v-text="step + ' / 6'"
      ></v-avatar>
    </v-card-title>
    <v-card-title class="text-h6 text-sm-h4 font-weight-bold justify-center">
      <span>{{ currentTitle }}を教えて下さい</span>
    </v-card-title>

    <v-window class="my-16" v-model="step">
      <v-window-item class="text-right" :value="index+1" v-for="(question, index) in questions" v-bind:key="index">
        <v-card-text>
          <v-select
            class="text-h6 text-center"
            :items="question.options"
            :label="question.label"
            :suffix="question.suffix"
            v-model="question.value"
            solo
            height="100"
          ></v-select>
        </v-card-text>
        <!-- <span class="mr-5 text-caption grey--text">Thanks for the answer!</span> -->
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
        v-show="step !== 6"
        color="primary"
        depressed
        @click="step++"
      >
        Next
      </v-btn>
      <v-btn color="primary" depressed @click="result" v-show="step === 6">Send</v-btn>
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
        number: [1, 2, 3, 4, 5, 6, 7, 8, 9, '10人以上'],
        val: '',
        questions: [
          {
            options: [1, 2, 3, 4, 5, 6, 7, 8, 9, '10人以上'],
            label: '生活人数',
            suffix: '人',
            value: ''
          },
          {
            options: [1, 2, 3, 4, 5, 6, 7, 8, 9, '10部屋以上'],
            label: '部屋数',
            suffix: '部屋',
            value: ''
          },
          {
            options: [1, 2, 3, 4, 5, 6, 7, 8, 9, '10階以上'],
            label: '階数',
            suffix: '階',
            value: ''
          },
          {
            options: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, '14回以上'],
            label: '洗濯時間/週',
            suffix: '回',
            value: ''
          },
          {
            options: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, '14回以上'],
            label: '掃除時間/週',
            suffix: '回',
            value: ''
          },
          {
            options: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, '21回以上'],
            label: '食器洗いの時間/週',
            suffix: '回',
            value: ''
          },
        ]
      }
    },
    computed: {
      currentTitle () {
        switch (this.step) {
          case 1: return '生活人数'
          case 2: return '部屋数'
          case 3: return '階数'
          case 4: return '週の洗濯時間'
          case 5: return '週の掃除時間'
          case 6: return '週の食器洗いの時間'
        }
      },
    },
    methods: {
      result() {
        const livingScale = this.questions[0].value * this.questions[1].value * this.questions[2].value;
        const result = livingScale * this.questions[3].value + livingScale * this.questions[4].value + livingScale * this.questions[5].value
        console.log(result);
      },
    }
  }

</script>

<style scoped>
  section {
    background: -webkit-linear-gradient(top,#2a5dc5,#39a2af 260px,hsla(0,0%,100%,0) 265px);
  }
</style>