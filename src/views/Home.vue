<template>
  <section>
    <!-- <v-row>
      <v-card height="1500" width="100%">
        <v-img
          src="https://smart-hometechnology.com/wp-content/uploads/2021/07/cropped-3f04768f324246f71a08f6a4e5013bd0.jpg"
        >
          <v-card-title class="justify-center align-center white--text">
            シミュレーション
          </v-card-title>
        </v-img>
        <v-card-title class="justify-center align-center ">
            シミュレーション
          </v-card-title>
      </v-card>
    </v-row> -->
    <HomeHero/>
    <v-container>
      <!-- <v-card>
        <v-card-text align="center" class="text-center text-h4 text--primary">
          <p>節約時間</p>
          <p>シミュレーター</p>
        </v-card-text>
      </v-card> -->

      <!-- <v-form class="mt-16">
        <v-select
          :items="number"
          filled
          label="生活人数"
        ></v-select>
        <v-select
          :items="number"
          filled
          label="部屋数"
        ></v-select>
        <v-select
          :items="number"
          filled
          label="xx数"
        ></v-select>


        <v-text-field
          label="1~10に二条"
        ></v-text-field>


      </v-form> -->
      <v-row justify="center">
        <v-col
          cols="12"
          sm="10"
          md="8"
        >
          <v-card class="mt-10" ref="form">
            <v-select
              class="px-8 pt-3"
              :items="number"
              label="生活人数"
            ></v-select>

            <v-select
              class="px-8 pt-3"
              :items="number"
              label="部屋数"
            ></v-select>

            <v-select
              class="px-8 pt-3"
              :items="number"
              label="階数"
            ></v-select>                

            <v-select
              class="px-8 pt-3"
              :items="number"
              label="週の洗濯時間"
            ></v-select>
              <v-select
                class="px-8 pt-3"
                :items="number"
                label="週の掃除時間"
            ></v-select>
            <v-select
              class="px-8 pt-3"
              :items="number"
              label="週の食器洗いの時間"
            ></v-select>
            <v-btn
              class="justify-center"
              width="50%"
            >
              Block Button
            </v-btn>
          </v-card>
        </v-col>
      </v-row>
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
        number: [1, 2, 3, 4, 5, 6, 7, 8, 9, '10人以上']
      }
    }
  }

</script>
