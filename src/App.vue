<template>
  <div id="app">
    <div class="container">
      <HeaderTMP />
      <Welcome />
      <About />
      <FormSub />
      <FooterTMP/>
    </div>
  </div>
</template>

<script>
import HeaderTMP from './components/header.vue'
import Welcome from './components/welcome.vue'
import FooterTMP from './components/footer.vue'
import About from './components/about.vue'
import FormSub from './components/form.vue'
export default {
  name: 'App',
  components: {
    HeaderTMP,
    Welcome,
    FooterTMP,
    About,
    FormSub
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Inter',serif;
}
html{
  scroll-behavior: smooth;
}
.container{
  width: 80%;
  margin:0 auto;
  }
#app {
   background: #171836;
   min-height: 100vh;
}

@media (max-width:410px) {
  .container{
    width: 95%;
  }
}
</style>
