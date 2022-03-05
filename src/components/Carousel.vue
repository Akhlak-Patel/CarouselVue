<template>
    <div>
        <h2>Carousel</h2>
        <carousel
        :autoplay="false" :nav="false"

        >

    <img src="https://placeimg.com/200/200/any?1" alt="img1">
    

    <img src="https://placeimg.com/200/200/any?2">

    <img src="https://placeimg.com/200/200/any?3">

    <img src="https://placeimg.com/200/200/any?4">

     <template slot="prev"><span class="prev">prev</span></template>



  
    <template  ><span class="next">next</span></template>
</carousel>
    </div>
</template>

<script>
import carousel from 'vue-owl-carousel'
export default {
    name:'Carousel',
    components:{
        carousel,
    }
}
</script>