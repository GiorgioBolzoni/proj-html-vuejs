<template>
    <div class="footer">
        <div class="container py-5">
            <div class="row">
                <div class="col-xl-3 col-lg-4 px-4">
                    <div class="logo">
                        <img src="../../assets/images/logo-footer-gobike.png" alt="logo-footer">
                    </div>
                    <div class="footer-info py-2">
                        <p><i class="fa-regular fa-location-dot" style="color: #ffffff;"></i> New Jersey, USA</p>
                        <p><i class="fa-regular fa-phone-volume" style="color: #ffffff;"></i> +1 (234) 567 89 10</p>
                        <p><i class="fa-regular fa-envelope" style="color: #ffffff;"></i> example@example.com</p>
                    </div>
                    <div>
                        <ul class="d-flex">
                            <li class="d-flex justify-content-center align-items-center">
                                <a href="#">
                                    <i class="fa-brands fa-facebook-f" style="color: #ffffff;"></i>
                                </a>
                            </li>
                            <li class="d-flex justify-content-center align-items-center">
                                <a href="#">
                                    <i class="fa-brands fa-instagram" style="color: #ffffff;"></i>
                                </a>
                            </li>
                            <li class="d-flex justify-content-center align-items-center">
                                <a href="#">
                                    <i class="fa-brands fa-twitter" style="color: #ffffff;"></i>
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-lg-4 px-4">
                    <h3>Join Our Newsletter</h3>
                    <p class="py-3">Subscribe to receive useful information.</p>
                    <div>
                        <input type="email" name="email" id="email" placeholder="Your Email Address" class="p-3">
                        <button type="button" id="subscribe" class="my-1 p-3">Subscribe</button>
                    </div>
                </div>
                <div class="col-lg-2 px-4">
                    <h3>Trainings</h3>
                    <div>
                        <ul id="footer-menu">
                            <li>
                                <strong>-</strong> &nbsp;
                                <a href="#">Riding Lesson</a>
                            </li>
                            <li>
                                <strong>-</strong> &nbsp;
                                <a href="#">Safe Driving</a>
                            </li>
                            <li>
                                <strong>-</strong> &nbsp;
                                <a href="#">Mountain Bike</a>
                            </li>
                            <li>
                                <strong>-</strong> &nbsp;
                                <a href="#">Trail Drive</a>
                            </li>
                            <li>
                                <strong>-</strong> &nbsp;
                                <a href="#">Pedaling</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="col-lg-2 px-4">
                    <h3>Quick Links</h3>
                    <div>
                        <ul id="footer-menu">
                            <li>
                                <strong>-</strong> &nbsp;
                                <a href="#">Home</a>
                            </li>
                            <li>
                                <strong>-</strong> &nbsp;
                                <a href="#">About Us</a>
                            </li>
                            <li>
                                <strong>-</strong> &nbsp;
                                <a href="#">Blog</a>
                            </li>
                            <li>
                                <strong>-</strong> &nbsp;
                                <a href="#">Packages</a>
                            </li>
                            <li>
                                <strong>-</strong> &nbsp;
                                <a href="#">Contact</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="text-center copyright mt-4 px-4">
                © 2023 Gobike - All Rights Reserved.
            </div>
        </div>
    </div>
</template>

<script>


export default {
    name: 'FooterApp',
    data () {
        

        return {}
    }
}
</script>

<style lang="scss" scoped>
    .footer{
        background-color: black;
        color: white;
        font-size: 16px;
        font-weight: 400;
    }

    .logo{
        width: 100%;
        margin-bottom: 16px;
        img{
            width: auto;
            height: 74px;
            margin-top: -12px;
            vertical-align: middle;

        }   
    }
    .copyright{
        font-size: 16px;
        font-weight: 400;
        padding: 10px;
    }
    ul{
        list-style: none;
        justify-content: start;
        margin-left: -35px;
        li{
            border: 1px solid rgba(255, 255, 255, 0.3);
            width: 71px;
            height: 40px;
            margin-right: 10px;
            font-size: 1.5em;
        }
    }
    h3{
        font-weight: 600;
    }
    #email{
        width: 100%;
        height: 70px;
        border-radius: 5px;
    }
    #subscribe{
        background: white;
        color: black;
        width: 100%;
        height: 70px;
    }
    #footer-menu{
        width: 100%;
        margin: auto;
        li{
        list-style: none;
        width: 100%;
        margin-left: -30px;
        border: none;
        display: flex;
        align-items: center;
        a{
            color: white;
            font-size: 0.7em;
        }
    }
    }
    
</style>