<template>
  <v-app>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
}
</script>

<style>
  @font-face {
    font-family: 'LuxuriousRoman';
    src: local("LuxuriousRoman"),
    url(./assets/fonts/LuxuriousRoman-Regular.ttf) format('truetype');
  }

  @font-face {
    font-family: 'Newsreader';
    src: local("Newsreader"),
    url(./assets/fonts/Newsreader-VariableFont_opsz,wght.ttf) format('truetype');
  }
  


</style>