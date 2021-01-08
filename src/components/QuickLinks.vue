<template>
  <div class="quick-links">
    <ul>
        <li v-bind:key="name" v-for="name in links.social_media">
            <div class="img-box">
                <img 
                    :src="require(`../assets/${name == `aquilaveion@aquil.com` ? `email` : name == `aquilaveionofficial` ? `instagram` : name == `aquilaveionsnaps` ? `snapchat` : `twitter`}.svg`)" 
                    :alt="name"
                />
                <p>{{`@${name}`}}</p>
            </div>
            
        </li>
    </ul>
  </div>
</template>

<script>
export default {
    name: 'QuickLinks',
    props: ["links"],
    data () {
        return {
            image_name: ["twitter", "instagram","snapchat","email"],
        }
    },
    computed:{
        imagename (){
            let name = this.image_name.map(handle => {
                return require(`../assets/${handle}.svg`)
            })
            return name
        }
    },
}
</script>


<style scoped>
.quick-links{
    position: absolute;
    left: 96%;
    top: 35%,
}
.quick-links ul{
    list-style-type: none;
    transition: all 1s ease-in;
}
.quick-links ul li:hover{
    transform: scale(1.2);
}
.quick-links ul li{
    padding: 2rem 0rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
} 
.quick-links ul li img{
    width: 3rem;
}
.quick-links ul li p {
    padding: 0.4rem 0rem;
    font-size: 1.2rem;
}
.quick-links ul li div p {
    display: none;
}
.img-box{
    display: flex;
    flex-direction: column;
    align-items: center;
}
@media (max-width: 870px) {
    .quick-links{
        top: 0;
        left: 0%;
    }
    .quick-links ul{
        display: flex;
        justify-content: space-between;
    }
    .quick-links ul li{
        margin: 0rem 2rem;
    }
    .quick-links ul li div p{
        display: block;
        font-size: 1.4rem;
    }
    
}
</style>
