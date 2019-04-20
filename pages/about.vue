<template>
  <div class="layout">
    <div class="page-overlay"></div>
    <Hero title="Title 2" />
    <h1>About us</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error doloremque omnis animi, eligendi magni a voluptatum, vitae, consequuntur rerum illum odit fugit assumenda rem dolores inventore iste reprehenderit maxime! Iusto.</p>
  </div>
  
</template>

<script>
import Hero from '~/components/Hero.vue'

export default {
  metaInfo: {
    title: 'About us'
  },
  components: {
    Hero
  }
}
</script>

<style lang="scss" scoped>

.layout{
  --layout-color: var(--secondary);
}
</style>
