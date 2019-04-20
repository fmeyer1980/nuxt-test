<template>
  <div class="layout">
    <div class="page-overlay"></div>
    <Cases />
  </div>
</template>

<script>
import Cases from '~/components/cases/Cases.vue'

export default {
  metaInfo: {
    title: 'About us'
  },
  components: {
    Cases
  }
}
</script>
<style lang="scss" scoped>
@import '~/assets/css/global.scss';

.layout{
  --layout-color: var(--light-gray-light);

  background-color: var(--layout-color);
}

@keyframes fade{
  from{
    background-color: transparent
  }

  to{
    background-color: $white;
  }
}

.cases{
    background-color: transparent;
    animation: fade .3s ease-in forwards;
    animation-delay: .5s;
}





</style>