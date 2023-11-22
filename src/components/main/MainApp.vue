<template>
    <div>
        <section class="jumbotron">
            <Carousel1 />
        </section>
        <section class="py-5 container">
            <Section2 />
        </section>
        <section class="py-5 margin container">
            <Carousel2 />
        </section>
        <section class="py-5 margin container">
            <Section4 />
        </section>
    </div>
</template>

<script>
import Carousel1 from './main-sections/Carousel1.vue'; 
import Section2 from './main-sections/Section2.vue'; 
import Carousel2 from './main-sections/Carousel2.vue'; 
import Section4 from './main-sections/Section4.vue'; 



export default {
    components:{
    Carousel1,
    Section2,
    Carousel2,
    Section4,
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