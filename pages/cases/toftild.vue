<template>
  <div class="layout">
    <div class="page-overlay"></div>
    <Hero title="Toftild" text="Jeg designer og udvikler små og store hjemmesider hvor både design, CMS og performance understøtter målsætningerne og brugernes adfærd." image="/_nuxt/assets/images/case-test-img.jpg" />
    <!-- <img src="@/assets/images/case-test-img.jpg" alt=""> -->
    <CasesInfo />
  </div>
</template>

<script>
import Hero from '~/components/Hero.vue'
import CasesInfo from '~/components/cases/CasesInfo.vue'

export default {
  metaInfo: {
    title: 'Toftild'
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
  @extend .page.cases-toftild;
}

</style>