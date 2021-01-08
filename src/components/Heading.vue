<template>
  <div class="hello">
    <h1>{{ links.name }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: ["links"]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello h1{
  text-align: center;
  font-size: 2.6rem;
  letter-spacing: 2rem;
  text-transform: uppercase;
  margin: 3rem 0rem;
  font-weight: 300;
}
</style>
