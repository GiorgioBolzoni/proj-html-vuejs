<template>
    <div class="container">
        <div class="text-center">
            <h3>Don't Miss Our Events</h3>
            <p>Get the amazing cycling experience.</p>
        </div>
        <div>
            <h5>Events</h5>
            <div class="row">
                <div v-for="(image, index) in images" :key="index" class="card col-12 col-md-6 col-lg-4 p-3">
                    <div class="card-image">
                        <img :src="image.img" alt="immagine">
                        <div class="date text-center py-1 px-2">
                            <div v-html="image.date"></div>
                        </div>
                    </div>
                    <div class="card-text p-3 border">
                        <div v-html="image.title" class="my-2"></div>
                        <div v-html="image.fullDate" class="my-2"></div>
                        <div v-html="image.place" class="my-2"></div>
                        <div v-html="image.tag" class="tag py-1 px-2 my-2"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Section4',
    data () {
        

        return {
            images: [
          { 
            img: '/images/event1.jpg',
            date: `
                <div><strong>22</strong></div>
                <div>JUN</div>
            `,
            title: `<h4><strong>Toronto Cycling Event 2023</strong></h4>`,
            fullDate: `<i class="fa-regular fa-clock" style="color: #000000;"></i> 2022-06-22 @ 01:30 - 2024-08-23 @ 07:00  `,
            place: `<i class="fa-solid fa-location-dot" style="color: #000000;"></i> Toronto`,
            tag: `Bicycle Race`,
          },
          { 
            img: '/images/event2.jpg',
            date: `
                <div><strong>30</strong></div>
                <div>JUN</div>
            `,
            title: `<h4><strong>Istanbul Cycling Event 2023</strong></h4>`,
            fullDate: `<i class="fa-regular fa-clock" style="color: #000000;"></i> 2022-06-30 @ 01:30 - 2024-10-19 @ 03:30`,
            place: `<i class="fa-solid fa-location-dot" style="color: #000000;"></i> Instanbul`,
            tag: `Bike Sport`,
          },
          { 
            img: '/images/event3.jpg',
            date: `
                <div><strong>22</strong></div>
                <div>JUN</div>
            `,
            title: `<h4><strong>Paris Cycling Event 2023</strong></h4>`,
            fullDate: `<i class="fa-regular fa-clock" style="color: #000000;"></i> 
                                2022-06-22                                 @ 07:30 - 2024-11-08 @ 16:30                            `,
            place: `<i class="fa-solid fa-location-dot" style="color: #000000;"></i> Paris`,
            tag: `Cycling Tour`,
          },
          { 
            img: '/images/event4.jpg',
            date: `
                <div><strong>25</strong></div>
                <div>JUN</div>
            `,
            title: `<h4><strong>New Jersey Cycling Event 2023</strong></h4>`,
            fullDate: `<i class="fa-regular fa-clock" style="color: #000000;"></i> 
                                2022-06-25                                 @ 03:00 - 2024-08-24 @ 05:30                            `,
            place: `<i class="fa-solid fa-location-dot" style="color: #000000;"></i> New Jersey`,
            tag: `Bicycle Race`,
          },
          { 
            img: '/images/event5.jpg',
            date: `
                <div><strong>28</strong></div>
                <div>JUN</div>
            `,
            title: `<h4><strong>London Cycling Event 2023</strong></h4>`,
            fullDate: `<i class="fa-regular fa-clock" style="color: #000000;"></i> 
                                2022-06-28                                 @ 07:30 - 2024-07-26 @ 12:00                            `,
            place: `<i class="fa-solid fa-location-dot" style="color: #000000;"></i> London`,
            tag: `Bike Sport`,
          },
          { 
            img: '/images/event6.jpg',
            date: `
                <div><strong>29</strong></div>
                <div>JUN</div>
            `,
            title: `<h4><strong>Kiev Cycling Event 2023</strong></h4>`,
            fullDate: `<i class="fa-regular fa-clock" style="color: #000000;"></i> 
                                2022-06-29                                 @ 10:00 - 2024-05-18 @ 04:30                            `,
            place: `<i class="fa-solid fa-location-dot" style="color: #000000;"></i> Kiev`,
            tag: `Bicycle Race`,
          },
          { 
            img: '/images/event7.jpg',
            date: `
                <div><strong>28</strong></div>
                <div>JUN</div>
            `,
            title: `<h4><strong>Colorado Cycling Event 2023</strong></h4>`,
            fullDate: `<i class="fa-regular fa-clock" style="color: #000000;"></i> 
                                2022-06-28                                 @ 04:00 - 2024-08-14 @ 05:30                            `,
            place: `<i class="fa-solid fa-location-dot" style="color: #000000;"></i> Colorado`,
            tag: `Bike Sport`,
          },
          { 
            img: '/images/event8.jpg',
            date: `
                <div><strong>28</strong></div>
                <div>JUN</div>
            `,
            title: `<h4><strong>Amsterdam Cycling Event 2023</strong></h4>`,
            fullDate: `<i class="fa-regular fa-clock" style="color: #000000;"></i> 
                                2022-06-28                                 @ 10:30 - 2024-10-24 @ 10:30                            `,
            place: `<i class="fa-solid fa-location-dot" style="color: #000000;"></i> Amsterdam`,
            tag: `Bicycle Race`,
          },
          { 
            img: '/images/event9.jpg',
            date: `
                <div><strong>22</strong></div>
                <div>JUN</div>
            `,
            title: `<h4><strong>Toronto Cycling Event 2023</strong></h4>`,
            fullDate: `<i class="fa-regular fa-clock" style="color: #000000;"></i> 
                                2022-06-22                                 @ 09:30 - 2024-09-27 @ 17:30                            `,
            place: `<i class="fa-solid fa-location-dot" style="color: #000000;"></i> Toronto`,
            tag: `Bicycle Race`,
          },
          { 
            img: '/images/event10.jpg',
            date: `
                <div><strong>26</strong></div>
                <div>JUN</div>
            `,
            title: `<h4><strong>Paris Cycling Event 2023</strong></h4>`,
            fullDate: `<i class="fa-regular fa-clock" style="color: #000000;"></i> 
                                2022-06-26                                 @ 05:30 - 2024-12-20 @ 14:00                            `,
            place: `<i class="fa-solid fa-location-dot" style="color: #000000;"></i> Paris`,
            tag: `Bicycle Race`,
          },
        ],
        }
    }
}
</script>

<style lang="scss" scoped>
    .card{
        position: relative;
        // height: 300px;

    }
    .card-image{
        position: relative;
        img{
            border-radius: 5px 5px 0 0;

        }
    }
    .card{
        border: none;
        cursor: pointer;
    }
    .card-text{
        border-radius: 0 0 5px 5px;
    }
    .date{
        position: absolute;
        top: 5px;
        left: 5px;
        background: white;
        color: black;
        border-radius: 8px;
    }
    .tag{
        background: #F5F5F5;
        font-size: 0.8em;
        width:fit-content
    }
    
</style>