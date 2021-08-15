<template>
  <section class="home-hero">
    <v-container fluid fill-height class="home-hero__content">
      <v-row>
        <v-col class="home-hero__content-text">
          <p>節約時間</p>
          <p>シミュレーター</p>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<style  lang="scss" scoped>
.home-hero__content {
  background: url("https://smart-hometechnology.com/wp-content/uploads/2021/07/cropped-3f04768f324246f71a08f6a4e5013bd0.jpg");
  background-size: cover;
  background-position: center center;
  width: 100%;
  height: 30vh;
 
  &-text {
    color: white;
    text-align: center;
    font-size: 28px;
    font-weight: bold;
  }
}
</style>