<template>
  <div :class="['page',$nuxt.$route.name]">
    <Nav />
    <nuxt />
  </div>
</template>

<script>

import Nav from './partials/nav';
import Hero from '@/components/Hero';

export default {
   data(){
    return{
      title: "sdsd"
    }
  },

  transition: {
    name: 'page',
    mode: 'out-in'
  },

  components: {
    Nav, Hero
  }
}

</script>


<style lang="scss">

</style>
