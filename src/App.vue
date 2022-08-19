<template>
<div id="app" @mousemove="mouseTrigger">
      <HeaderComponent />
      <router-view/>
  </div>
</template>

<script>
  import HeaderComponent from './components/common/Header.vue'
  export default {
    name: 'App',
    components: {
        HeaderComponent
    },
    methods: {
      mouseTrigger(){

      }
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
}
</style>
