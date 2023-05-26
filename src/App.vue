<template>
  <HeaderPart></HeaderPart>
  <NavPart></NavPart>
 <HomeComponent></HomeComponent>

  <div>testing</div>
</template>

<script>
import HeaderPart from './components/HeaderPart.vue'
import NavPart from './components/NavPart.vue'
import HomeComponent from './components/HomeComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderPart,
    NavPart,
    HomeComponent
  }
}
</script>

<style>

</style>
