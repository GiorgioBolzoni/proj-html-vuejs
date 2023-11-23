<template>
    <div class="container">
        <div class="text-center">
            <h3>Our Expert Trainers</h3>
            <p>Learn to ride a bike from the experts.</p>
        </div>
        <div class="card-container d-flex justify-content-between align-items-center py-3">
            <div v-for="(image, index) in images" :key="index" class="card-image">
                <img :src="image.img" alt="immagine" class="active">
                <div class="image-text d-flex flex-column justify-content-between align-items-center py-2">
                    <div class="image-name d-flex justify-content-center align-items-center" v-html="image.name"></div>
                    <p class="d-flex justify-content-center align-items-center">Biker</p>
                    <ul class="d-flex justify-content-center align-items-center">
                        <li>
                            <a href="#">
                                <i class="fa-brands fa-facebook-f" style="color: #ffffff;"></i>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="fa-brands fa-instagram" style="color: #ffffff;"></i>
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <i class="fa-brands fa-twitter" style="color: #ffffff;"></i>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Section5',
    data () {
        

        return {
            images: [
        { 
            img: '/images/biker1.jpg',
            name: `<div>Michael Lee</div>`,
        },
        { 
            img: '/images/biker4.jpg',
            name: `<div>Robert Lee</div>`,
        },
        { 
            img: '/images/biker3.jpg',
            name: `<div>John Doe</div>`
        },
        { 
            img: '/images/biker2.jpg',
            name: `<div>Emily Brown</div>`,
        },
      ],
        }
    }
}
</script>

<style lang="scss" scoped>
    .card-image{
        padding: 5px;
        background-color: #f5f5f5;
        width: calc((100% / 4) - 10px);
        position: relative;
        cursor: pointer;
        img{
            height: 100%;
        }
        .image-text{
            background-color: black;
            color: white;
            text-align: center;
            font-weight: 600;
            position: absolute;
            width: calc(100% - 10px);
            bottom: 5px;
            left: 5px;
            overflow: hidden;

            .image-name{
                font-size: 1.5em;
            }
            p{
                font-size: 1.2em;
                font-weight: 600;
                color: #B3B3B3;
            }
        }
        li{
            list-style: none;
            margin-right: 10px;
        }

        &:hover img{
            filter: brightness(70%);
            // transform: scale(110%);
            // overflow: hidden;
        }
    }
</style>