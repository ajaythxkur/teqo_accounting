<template>
  <div id="app">
      <HeaderComponent />
        <router-view/>
      <FooterComponent />
  </div>
</template>

<script>
  import HeaderComponent from './components/common/Header.vue'
  import FooterComponent from './components/common/Footer.vue'
  export default {
    name: 'App',
    components: {
        HeaderComponent,
        FooterComponent
    }
  }
</script>

<style>
#app {
  font-family: MontserratAlternates, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale; 
}
@font-face {
  font-family: MontserratAlternates;
  src: url('./assets/fonts/MontserratAlternates/MontserratAlternates-SemiBold.ttf');
  font-weight: 600;
}
@font-face {
  font-family: MontserratAlternates;
  src: url('./assets/fonts/MontserratAlternates/MontserratAlternates-Regular.ttf');
  font-weight: 400;
}
@font-face {
  font-family: MontserratAlternates;
  src: url('./assets/fonts/MontserratAlternates/MontserratAlternates-Medium.ttf');
  font-weight: 500;
}
@font-face {
  font-family: MontserratAlternates;
  src: url('./assets/fonts/MontserratAlternates/MontserratAlternates-Bold.ttf');
  font-weight: 700;
}
@font-face {
  font-family: MontserratAlternates;
  src: url('./assets/fonts/MontserratAlternates/MontserratAlternates-ExtraBold.ttf');
  font-weight: 800;
}
:root {
  --tq-white: #FFF;
  --tq-blue: #022e6b;
  --tq-orange: #ff6a40;
  --tq-gray: rgba(0,0,0,.7);
  --tq-pinkish-white: #fcf9f7;
  --tq-taxation-shadow: #e2e2e2;
  --tq-bg-support: #f1ede9;
  --tq-red: #dc3850;
  --tq-black: #000;
  --tq-red-pink: #ea3353;
  --tq-form-background: rgba(255,106,64,.1);
  --tq-box-shadow: 1px 1px 10px #d9d9d9;
  --tq-mobile-bg: #000000bd;
  --tq-green: #42db87;
}
</style>
