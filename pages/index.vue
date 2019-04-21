<template>
  <div class="layout">
    <div class="page-overlay"></div>
    <Hero 
    page="home"
    title="Designer og webdudvikler" 
    text="Jeg designer og udvikler små og store hjemmesider hvor både design, CMS og performance understøtter jeres målsætning og brugernes adfærd optimalt" image="hero-home-bg.png"
    />
<!-- <img src="~assets/images/hero-home-bg.png" alt=""> -->
    <About />
    <Process />
    <Cases colorTheme="home" />
    
  </div>
</template>

<script>
import Hero from '~/components/Hero.vue'
import About from '~/components/AboutHome.vue'
import Process from '~/components/Process.vue'
import Cases from '~/components/cases/Cases.vue'



export default {
  transition: {
    name: 'page',
    mode: 'out-in'
  },

  data() {
    return{
      imgName: '/images/case1.jpg'
    }
  },
  

  components: {
     Hero,
     About,
     Process,
     Cases
    },
}
</script>

<style lang="scss" scoped>



.layout{
  --layout-color: var(--secondary);
  background-color: var(--layout-color);
}

@keyframes fade{
  from{
    background-color: transparent
  }

  to{
    background-color: var(--secondary-light);
  }
}

.about{
  background-color: transparent;
  animation: fade .3s ease-in forwards;
  animation-delay: 3s;
}

h1{
  color: #333;
}


</style>
