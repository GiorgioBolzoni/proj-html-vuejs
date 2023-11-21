<template>
    <div>
        <section class="jumbotron">
            <Carousel1 />
        </section>
        <section class="py-3 container">
            <Section2 />
        </section>
    </div>
</template>

<script>
import Carousel1 from './main-sections/Carousel1.vue'; 
import Section2 from './main-sections/Section2.vue'; 

export default {
    components:{
    Carousel1,
    Section2,
    },
    data () {
        

        return {}
    }
}
</script>

<style lang="scss" scoped>
    
</style>