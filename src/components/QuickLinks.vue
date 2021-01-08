<template>
  <div class="quick-links">
    <ul>
        <li v-bind:key="name" v-for="name in links.social_media">
            <div>
                <img 
                    :src="require(`../assets/${'instagram'}.svg`)" 
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
            // let key = Object.keys(this.links.social_media);
            let name = this.image_name.map(handle => {
                return require(`../assets/${handle}.svg`)
            })
            return name
        }
    },
    // methods:{
    //     generate(){
    //         let key = Object.keys(this.links.social_media);
    //         key.map(img =>{
    //             return
    //         })
    //     }
    // }
}
</script>


<style scoped>
.quick-links{
    position: absolute;
    left: 97%;
    top: 35%,
}
.quick-links ul{
    list-style-type: none;
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
/* @media (max-width: 768px) {
    .quick-links{
        top: 0;
        right: 50%;
    }
    .quick-links ul{
        display: flex;
        justify-content: space-between;
    }
    .quick-links ul li{
        margin: 0rem 2rem;
    }
} */
</style>
