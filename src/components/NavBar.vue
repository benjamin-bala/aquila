<template>
  <div class="nav">
    <ul>
        <li>Home</li>
        <li>About</li>
        <li class="nav-image"></li>
        <li>Gallery</li>
        <li>Contact</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
}
</script>


<style scoped>
.nav ul{
    display: flex;
    width: 100%;
    justify-content: space-around;
    margin: 2rem;
    font-size: 1.8rem;
    font-weight: 300;
    list-style-type: none;
    align-items: center;
}
.nav ul li{
    margin: 0rem 3rem;
    letter-spacing: 0.5rem;
    text-transform: uppercase;
}
.nav-image{
    background: url("../assets/navimage.jpg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    border-radius: 50%;
    width: 100px;
    height: 100px;
    -moz-box-shadow: inset 1px 1px 20px rgba(0, 0, 0, 0.315);
    -webkit-box-shadow: inset 1px 1px 20px rgba(0, 0, 0, 0.315);
    box-shadow: inset 1px 1px 20px rgba(0, 0, 0, 0.315);
}
@media (max-width: 860px) {
    .nav ul li {
        margin: 0rem 1rem;
    }
    .nav-image{
        width: 50px;
        height: 50px;
    }
}
</style>
