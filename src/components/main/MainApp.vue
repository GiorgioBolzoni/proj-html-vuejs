<template>
    <div>
        <section class="jumbotron">
            <Carousel1 />
        </section>
        <section class="py-5 container">
            <Section2 />
        </section>
        <section class="pt-5 margin container">
            <Carousel2 />
        </section>
        <section class="py-5 container">
            <Section4 />
        </section>
        <section class="py-5 container">
            <Section5 />
        </section>
        <section class="py-5 container">
            <Section6 />
        </section>
    </div>
</template>

<script>
import Carousel1 from './main-sections/Carousel1.vue'; 
import Section2 from './main-sections/Section2.vue'; 
import Carousel2 from './main-sections/Carousel2.vue'; 
import Section4 from './main-sections/Section4.vue'; 
import Section5 from './main-sections/Section5.vue'; 
import Section6 from './main-sections/Section6.vue'; 



export default {
    components:{
    Carousel1,
    Section2,
    Carousel2,
    Section4,
    Section5,
    Section6,
    },
    data () {
        

        return {}
    }
}
</script>

<style lang="scss" scoped>
    .margin{
        margin-top: 150px;
    }
</style>