<template>
  <div id="app">
    <Heading v-bind:links="links"/>
    <ImageCard />
    <NavBar />
    <QuickLinks v-bind:links="links"/>
  </div>
</template>

<script>
import Heading from './components/Heading.vue'
import ImageCard from './components/ImageCard.vue'
import NavBar from './components/NavBar.vue'
import QuickLinks from './components/QuickLinks.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    Heading,
    ImageCard,
    NavBar,
    QuickLinks
  },
  data() {
    return{
      links: {}
    }
  },
  created() {
    axios.get('https://hirng-x2021.glitch.me/api').then(files => this.links = files.data).catch(console.log)
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600&display=swap');
*,*::before, *::after{
 margin: 0rem;
  padding: 0rem;
  box-sizing: inherit;
}
html{
  font-size: 62.5%;
}
body { 
  background:#CB2964; 
  color: #fafafa;
  box-sizing: border-box;
  font-family: 'Open Sans', sans-serif;
  overflow: hidden;
}
body:after {
  content:"";
  background:#BD0F4D;
  position:fixed;
  top:0;
  bottom:0;
  right:50%;
  left:0;
  content:" ";
  z-index:-1;
}
#app{
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  height: 100vh;
}
@media (max-width: 860px) {
  html{
    font-size: 40%;
  }
}
@media (max-width: 360px) {
  html{
    font-size: 30.5%;
  }
}
</style>
