<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Sponsor />
    <Place />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Sponsor from '@/components/Sponsor.vue'
import Place from '@/components/Place.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    Sponsor,
    Place
  }
}
</script>
