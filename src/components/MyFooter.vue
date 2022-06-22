<template>
    <!-- footer content -->
    <div id="footer" class="row">
        
        <div id="footer-top" class="d-flex flex-column justify-content-start pt-5">
            <div class="footer-content d-flex justify-content-center gap-5">

                <!-- recap presentazione azienda + social -->
                <div class="about d-flex flex-column text-start">
                    <h6 class="mb-4">
                        ABOUT US
                    </h6>
                    <p class="mb-4">
                        Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
                    </p>

                    <!-- icone dei social -->
                    <a href="#" class="d-flex gap-3 fs-4">
                        <font-awesome-icon :icon="['fab', 'facebook-square']" />
                        <font-awesome-icon :icon="['fab', 'twitter-square']" />
                        <font-awesome-icon :icon="['fab', 'linkedin']" />
                        <font-awesome-icon :icon="['fab', 'google-plus']" />
                        <font-awesome-icon :icon="['fab', 'pinterest-square']" />
                        <font-awesome-icon :icon="['fab', 'flickr']" />
                    </a>
                </div>
                
                <!-- recap news -->
                <div class="news d-flex flex-column align-items-start text-start">
                    <ul>
                        <li>
                            <h6 class="mb-4">
                                RECENT NEWS
                            </h6>
                        </li>
                        <li class="mb-3">
                            <a href="#">
                                <font-awesome-icon icon="fas fa-angle-right"
                                class="me-2" />
                                SEM PORTA MOLLIS PARTURIENT
                            </a>
                        </li>
                        <li class="mb-3">
                            <a href="#">
                                <font-awesome-icon icon="fas fa-angle-right"
                                class="me-2" />
                                NULLAM LOREM MATTIS PURUS
                            </a>
                        </li>
                        <li class="mb-3">
                            <a href="#">
                                <font-awesome-icon icon="fas fa-angle-right"
                                class="me-2" />
                                NIBH SEM SIT ULLAMCORPER
                            </a>
                        </li>
                        <li class="mb-3">
                            <a href="#">
                                <font-awesome-icon icon="fas fa-angle-right"
                                class="me-2" />
                                DONEC LUCTUS IMPERDIET
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <font-awesome-icon icon="fas fa-angle-right"
                                class="me-2" />
                                MAGNA PARS STUDIORUM
                            </a>
                        </li>
                    </ul>
                </div>

                <!-- recap tickets -->
                <div class="seat d-flex flex-column text-start">
                    <h6 class="mb-4">
                        GET YOUR SEAT!
                    </h6>
                    <p class="mb-4">
                        Book for your seat before it's too rate. We provide variety of ticket options.
                    </p>
                    <button class="p-3 px-4">
                        CHECK OUT TICKETS!
                    </button>
                </div>

                <!-- recap galleria immagini -->
                <div class="gallery d-flex flex-column text-start"
                v-for="(image, index) in listGallery" :key="index">
                    <h6 class="mb-4">
                        GALLERY FROM LAST YEAR
                    </h6>

                    <div class="card-image d-flex flex-wrap gap-2">
                        <img :src="image.tile1" alt="tile1">
                        <img :src="image.tile2" alt="tile2">
                        <img :src="image.tile3" alt="tile3">
                        <img :src="image.tile4" alt="tile4">
                        <img :src="image.tile5" alt="tile5">
                        <img :src="image.tile6" alt="tile6">
                        <img :src="image.tile7" alt="tile7">
                        <img :src="image.tile8" alt="tile8">
                        <img :src="image.tile9" alt="tile9">
                        <img :src="image.tile10" alt="tile10">
                        <img :src="image.tile11" alt="tile11">
                        <img :src="image.tile12" alt="tile12">
                    </div>
                </div>
                
            </div>
        </div>

        <div id="footer-bottom" class="d-flex align-items-center">

            <div id="text-footer-bottom" class="d-flex justify-content-between mx-auto">
                 <span>
                    &copy; Copyright GooLayers, All Right Reserved
                </span>

                <span>
                    About Us | Accommodation | Call For Paper | Contatct Us
                </span>
            </div>

        </div>

    </div>   
</template>

<script>
export default {
    name: 'MyFooter',
    data() {
        return {
            listGallery: [
                {
                    tile1: require("../assets/img/photodune-7770665-two-white-coffee-mug-with-diy-decoration-o (1).jpg"),
                    tile2: require("../assets/img/photodune-8523683-speaker-at-business-convention-and-present.jpg"),
                    tile3: require("../assets/img/photodune-6745579-modern-creative-man-relaxing-on-workspace-.jpg"),
                    tile4: require("../assets/img/photodune-8522811-speaker-at-business-conference-and-present (1).jpg"),
                    tile5: require("../assets/img/photodune-8797753-multiethnic-people-with-startup-business-t (1).jpg"),
                    tile6: require("../assets/img/card04-150x150.jpg"),
                    tile7: require("../assets/img/photodune-6745606-man-wristwatch-calendar-key-and-glasses-on.jpg"),
                    tile8: require("../assets/img/photodune-6745585-modern-creative-workspace-m-150x150.jpg"),
                    tile9: require("../assets/img/6426608875_186070f8ca_o-150x150.jpg"),
                    tile10: require("../assets/img/card01-150x150.jpg"),
                    tile11: require("../assets/img/13349065283_64d09b067c_o-150x150.jpg"),
                    tile12: require("../assets/img/photodune-8795110-overhead-of-essentials-denim-clothes-m-150.jpg")
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/scss/Hover-Color.scss";
@import "../assets/scss/ListStyle.scss";

#footer {
    width: 100%;
    height: 47vh;
    //debug
    background: orange;

    #footer-top {
        width: 100%;
        height: 48vh;
        background: #272727;

        h6 {
            color: #d9d9d9;
            font-size: 14px;
            font-weight: 600;
        }

        p {
            color: #adadad;
            font-size: 13px;
        }

        .about {
            width: 15%;

            a {
                color: #ffffff;
            }
        }

        .news {
            

            li {
                list-style-type: $text-list-item;

                a {
                    text-decoration: $list-item;
                    color: #878787;
                    font-size: 13px;
                }
            }
        }

        .seat {
            width: 20%;

            button {
                font-weight: 700;
                font-size: 12px;
                border-width: 0 0 3px 0;
                border-color: #d92719;
                background: $hover-color;
                color: #ffffff;
            }
        }

        .gallery {
            width: 30%;

            .card-image {
                width: 50%;

                img {
                    max-width: 100%;
                    height: 6vh;
                }
            }
        }
    }

    #footer-bottom {
        height: calc(100% - 39vh);
        background: #171717;

        #text-footer-bottom {
            width: 58%;
            font-size: 13px;

            span {
                color: #4d4d4a;

                &:last-child {
                    color: #6c6a6b;
                }
            }
        }
    }
}
</style>