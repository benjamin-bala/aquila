<template>
  <div class="card">
    <!-- <img src="../assets/cardimage.png" alt="model" /> -->
  </div>
</template>

<script>
export default {
  name: 'ImageCard',
}
</script>


<style scoped>
.card{
    background: #CB2964 url("../assets/cardimage.png");
    background-repeat: no-repeat;
    background-position: bottom;
    background-size: contain;
    -moz-box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.315);
    -webkit-box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.315);
    box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.315);
    padding: 5rem;
    width: 52rem;
    height: 55rem;
    margin: 2rem 0rem;
}


</style>
