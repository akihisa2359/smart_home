<template>
  <section>
    <HomeHero/>
    <v-container>

      <v-row justify="center">
        <v-col cols="12" sm="10" md="4">
            <v-subheader>Prefix for dollar currency</v-subheader>
        </v-col>
        <v-col cols="12" sm="10" md="6">
          <v-card ref="form">
            <v-select
              class="px-8 pt-3"
              :items="number"
              label="生活人数"
            ></v-select>
          </v-card>
        </v-col>


      </v-row>
      <v-card width="100%" class="mt-5">
        <v-row justify="center">
          <v-col cols="12" sm="10" md="4">
            <v-subheader class="justify-center">生活人数</v-subheader>
          </v-col>
          <v-col cols="12" sm="10" md="7">
            <v-select
              :items="number"
              filled
              label="生活人数"
              dense
              hide-details
            ></v-select>
          </v-col>

          <v-col cols="12" sm="10" md="4">
            <v-subheader class="justify-center">住居の広さ</v-subheader>
          </v-col>
          <v-col cols="12" sm="10" md="7">
            <v-select
              :items="number"
              filled
              label="生活人数"
              dense
              hide-details
            ></v-select>
          </v-col>

          <v-col cols="12" sm="10" md="4">
            <v-subheader class="justify-center">住居の広さ</v-subheader>
          </v-col>
          <v-col cols="12" sm="10" md="7">
            <v-select
              :items="number"
              filled
              label="生活人数"
              dense
              hide-details
            ></v-select>
          </v-col>

          <v-col cols="12" sm="10" md="4">
            <v-subheader class="justify-center">週の洗濯時間</v-subheader>
          </v-col>
          <v-col cols="12" sm="10" md="7">
            <v-select
              :items="number"
              filled
              label="生活人数"
              dense
              hide-details
            ></v-select>
          </v-col>

          <v-col cols="12" sm="10" md="4">
            <v-subheader class="justify-center">週の掃除時間</v-subheader>
          </v-col>
          <v-col cols="12" sm="10" md="7">
            <v-select
              :items="number"
              filled
              label="生活人数"
              dense
              hide-details
            ></v-select>
          </v-col>

          <v-col cols="12" sm="10" md="4">
            <v-subheader class="justify-center">週の食器洗いの時間</v-subheader>
          </v-col>
          <v-col cols="12" sm="10" md="7">
            <v-select
              :items="number"
              filled
              label="生活人数"
              dense
              hide-details
            ></v-select>
          </v-col>


          
        </v-row>
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
        number: [1, 2, 3, 4, 5, 6, 7, 8, 9, '10人以上']
      }
    }
  }

</script>
