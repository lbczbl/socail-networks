<template>
  <div id="app">
    <Navbar/>
    <keep-alive>
      <router-view></router-view>
    </keep-alive>
    <Footer/>
  </div>
</template>

<script>
import Navbar from './components/Navbar';
import Landing from './components/Landing';
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    Navbar,
    Landing,
    Footer
  }
}
</script>

<style>

</style>
