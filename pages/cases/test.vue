<template>
  <div class="layout">
    <div class="page-overlay"></div>
    <Hero title="Beach tours" text="Jeg designer og udvikler små og store hjemmesider hvor både design, CMS og performance understøtter målsætningerne og brugernes adfærd." image="case-test-img.jpg" />
    <!-- <img src="@/assets/images/case-test-img.jpg" alt=""> -->
    <CasesInfo />
    <div class="box bg-light text-dark pt-8 pb-8">
      <div class="container container--right container--left">
        <h2>Strategi og ny digital identitet tilpasset målgruppens shoppingadfærd</h2>
        <p>Baum und Pferdgarten er et high end fashion brand, der skaber kollektioner fyldt med kolliderende kontraster, stærke farver og unikke prints. Som et brand med en stærk forståelse af, hvem de er, og hvad de står for, var vores udfordring at forenkle og forstærke deres brandplatform og skabe en flagship eCommerce løsning.</p>
      </div>
    </div>
    <div class="box bg-white text-dark pt-8 pb-8">
      <div class="container container--right container--left">
        <h2>Overskrift</h2>
        <p>Baum und Pferdgarten er et high end fashion brand, der skaber kollektioner fyldt med kolliderende kontraster, stærke farver og unikke prints. Som et brand med en stærk forståelse af, hvem de er, og hvad de står for, var vores udfordring at forenkle og forstærke deres brandplatform og skabe en flagship eCommerce løsning.</p>
      </div>
    </div>
    
  </div>
</template>

<script>
import Hero from '~/components/Hero.vue'
import CasesInfo from '~/components/cases/CasesInfo.vue'

export default {
  metaInfo: {
    title: 'Test side'
  },

  data: {
    score: [0,80,320,280,98],
    paperNames:["hapana1","hapana2","hapana3","tikiri","tikiri2"]
  },

  transition: {
    name: 'page-fade',
    mode: 'out-in'
  },
  
  components: {
   Hero,
   CasesInfo
  }
}
</script>
<style lang="scss" scoped>
@import '~/assets/css/global.scss';

.layout{  
  @extend .page.cases-test;
}

.box{
    animation: fadeInAni .3s ease-in;
    animation-delay: 2s;
    animation-fill-mode: backwards; 
}

</style>