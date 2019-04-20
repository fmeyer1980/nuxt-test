<template>
  <div class="layout">
    <div class="page-overlay"></div>
    <Hero title="Beach tours" text="Jeg designer og udvikler små og store hjemmesider hvor både design, CMS og performance understøtter målsætningerne og brugernes adfærd." image="case-test-img.jpg" />
    <!-- <img src="@/assets/images/case-test-img.jpg" alt=""> -->
    <CasesInfo />
    <div class="container container--right container--left">
      <h2>Strategi og ny digital identitet tilpasset målgruppens shoppingadfærd</h2>
      <p>Baum und Pferdgarten er et high end fashion brand, der skaber kollektioner fyldt med kolliderende kontraster, stærke farver og unikke prints. Som et brand med en stærk forståelse af, hvem de er, og hvad de står for, var vores udfordring at forenkle og forstærke deres brandplatform og skabe en flagship eCommerce løsning.</p>
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
@import '~/assets/css/pages.scss';

.layout{  
  @extend .page.cases-test;
}

</style>