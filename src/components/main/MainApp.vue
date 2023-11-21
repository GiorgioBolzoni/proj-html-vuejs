<template>
    <div>
        <section class="jumbotron border">
            <Carousel1 />
        </section>
    </div>
</template>

<script>
import Carousel1 from './main-sections/Carousel1.vue'; 

export default {
    components:{
    Carousel1,
    },
    data () {
        

        return {}
    }
}
</script>

<style lang="scss" scoped>
    .jumbotron{
        max-height: 300px;
    }
</style>