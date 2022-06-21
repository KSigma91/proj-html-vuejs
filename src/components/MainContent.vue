<template>
    <div class="container-fluid">

         <!-- jumbotron -->
        <div id="call-to-action" class="row d-flex flex-column justify-content-around">

            <!-- testo del jumbotron -->
            <div id="jumbo-text">
                <h1>
                    CONFERENCE ON
                </h1>
                <h1 class="my-2">
                    SOCIAL NETWORKS
                </h1>

                <div id="meet" class="d-flex justify-content-between mx-auto mt-5 py-3 p-1">
                    <h5>23 - 26 MAY 2019</h5>
                    /
                    <h5>SANS FRANCISCO</h5>
                    /
                    <h5>8 SPEAKERS</h5>
                </div>

                <!-- pulsante per la registrazione -->
                <button class="py-3 px-4 mt-4 rounded-3">
                    REGISTER ONLINE
                </button>
            </div>

        </div>

        <!-- informazioni dei componenti dell'azienda -->
        <div id="info-company" class="row d-flex justify-content-center align-items-center">

            <div class="info-text d-flex flex-column justify-content-around p-3"
            v-for="(info, index) in infoList" :key="index">
                <!-- titolo -->
                <div class="info-header d-flex fs-4">
                    <font-awesome-icon :icon="info.icon" class="pe-4" />
                    <h6>
                        {{ info.title }}
                    </h6>
                </div>
                <!-- testo -->
                <p class="ms-5">
                    {{info.text }}
                </p>
                <!-- scopri di più -->
                <a :href="info.url" class="ms-5 text-decoration-none">
                    {{ info.add }}
                </a>
            </div>

        </div>

        <!-- countdown -->
        <div id="countdown" class="row d-flex align-items-center">

            <!-- tessere con il countdown -->
            <div id="content-card" class="d-flex flex-column justify-content-around">
                <div class="card-area d-flex justify-content-center">
                    <div class="card py-4 px-5 mx-2"
                    v-for="(numb, index) in countNumb" :key="index" :style="`background: ${numb.bg}; opacity: ${numb.transp}`">
                        <h1>
                            {{ numb.number }}
                        </h1>
                        <span>
                            {{ numb.text }}
                        </span>
                    </div>
                </div>

                <!-- area del subscribe -->
                <h5 class="fw-bold">
                    SUBSCRIBE FOR UPDATES
                </h5>
                <div id="update">
                    <input type="text" placeholder="Please fill your email"
                    class="p-3 mx-3">
                    <button class="p-3 px-4">
                        SUBSCRIBE
                    </button>
                </div>
            </div>
            
        </div>

        <!-- presentazione del team -->
        <div id="team-members" class="row d-flex flex-column justify-content-center">
            
            <div id="team-area" class="d-flex flex-wrap mx-auto">
                <!-- area di scroll delle immagini -->
                <div id="navigation" class="d-flex justify-content-between align-items-center mb-5">
                    <h2 class="fw-bold">
                        SPEAKERS
                    </h2>
                
                    <div id="change-card" class="d-flex gap-1">
                        <button href="#" class="px-3 py-2">
                            <font-awesome-icon icon="fas fa-angle-left" />
                        </button>
                        <button href="#" class="px-3 py-2">
                            <font-awesome-icon icon="fas fa-angle-right" />
                        </button>
                    </div>
                </div>

                <!-- lista del team -->
                <div id="card-area" class="d-flex justify-content-between">
                    <div class="card-team d-flex flex-column justify-content-evenly"
                    v-for="(cards, index) in listCard" :key="index">
                        <!-- immagine profilo -->
                        <img :src="cards.img" :alt="cards.alt">
                        <!-- info -->
                        <h6 class="mt-3 fw-bolder">
                            {{ cards.name }}
                        </h6>
                        <span>
                            {{ cards.job }}
                        </span>
                    </div>
                </div>
            </div>

        </div>

        <!-- calendario programma -->
        <div id="program-company" class="row d-flex justify-content-around align-items-center">

            <div id="program-area" class="d-flex flex-column justify-content-around">
                <!-- introduzione -->
                <div id="program-header" class="d-flex justify-content-between align-items-center mb-5">
                    <h1 class="align-self-start fw-bolder">
                        PROGRAM
                    </h1>
                    <p class="text-start">
                        This conference run through all 4 days from 23 - 26 May 2016.
                        We also provide free lunch and coffee break in each day.
                    </p>
                    <span>
                        View Full Program
                    </span>
                </div>

                <!-- rubrica -->
                <div id="program-content" class="d-flex flex-column text-start">
                    <!-- lista giorni appuntamento -->
                    <div id="card-header" class="d-flex">
                        <div class="card-day p-3"
                        v-for="(day, index) in listCardDay" :key="index">
                            <ul>
                                <li>
                                    <a href="#">
                                        <h6 class="fw-bolder">
                                            {{ day.nDay }}
                                        </h6>
                                        <span>
                                            {{ day.date }}
                                        </span>
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <div id="meeting" class="d-flex justify-content-around align-items-center">
                            <div id="info-meet" class="d-flex flex-column align-items-center">
                                <ul>
                                    <li class="p-1">
                                        <a href="#">
                                            <font-awesome-icon icon="fas fa-clock"  class="me-2"/>
                                            <span>
                                                09:00 - 10:30
                                            </span>
                                        </a>
                                    </li>
                                    <li class="p-1">
                                        <a href="#">
                                            <font-awesome-icon icon="fas fa-location-arrow" class="me-2"/>
                                            <span>
                                                ROOM A
                                            </span>
                                        </a>
                                    </li>
                                    <li class="p-1">
                                        <a href="#">
                                            <font-awesome-icon icon="fas fa-user" class="me-2"/>
                                            <span>
                                                LAURENCE FRANCIS
                                            </span>
                                        </a>
                                    </li>
                                </ul>
                            </div>

                        <div class="program-text d-flex flex-column justify-content-around">
                            <h4>
                                WELCOMING AND INTRODUCTION
                            </h4>
                            <p style="width: 80%">
                                Vestibulum id ligula porta felis euismod semper. Nullam quis risus eget urna mollis ornare vel eu leo. Donec
                                ullamcorper nulla non metus auctor fringilla. Aenean lacinia bibendum nulla sed consectetur...
                            </p>
                            <img src="../assets/img/speaker-8-150x150.jpg" alt="speaker_img" style="width: 5%"
                            class="rounded-1">
                        </div>
                    </div> 
                </div>
            </div>

        </div>

        <!-- posizione google maps -->
        <div id="map" class="row">

            <div id="map-area" class="position-relative">
                <!-- tasselli per composizione mappa -->
                <div class="tiles d-inline"
                v-for="(puzzle, index) in mapPuzzle" :key="index">
                    <img :src="puzzle.item" :alt="puzzle.alt">
                </div>

                <div class="label">
                    <!-- visualizzazione mappa -->
                    <div id="map-style" class="d-flex position-absolute top-0 start-0 m-3 shadow-sm">
                        <a href="#" class="rounded-start">
                            <h5 class="p-2 fw-bolder"
                            style="color: #000;">
                                Map
                            </h5>
                        </a>
                        <a href="#" class="rounded-end">
                            <h5 class="p-2 border-start border-2">
                                Satellite
                            </h5>
                        </a>  
                    </div>
                    
                    <div id="bottom-label" class="d-flex flex-column align-items-end position-absolute bottom-0 end-0 m-2">
                         <!-- visualizzazione in prima persona -->
                        <div id="street-view" class="d-flex fs-4 mb-3 m-1">
                            <a href="#" class="px-2 rounded-1">
                                <font-awesome-icon icon="fas fa-street-view" style="color: #fbb93e" />
                            </a>
                        </div>

                        <!-- zoom incremento/decremento -->
                        <div id="zoom-map" class="d-flex flex-column fs-4 mb-5 m-1">
                            <a href="#" style="color: #5d5d5c" class="px-2 border-bottom rounded-top">
                                <font-awesome-icon icon="fas fa-plus" />
                            </a>
                            <a href="#" style="color: #5d5d5c" class="px-2 rounded-bottom">
                                <font-awesome-icon icon="fas fa-minus" />
                            </a>
                        </div>
                    </div>
                   
                </div>
            </div>

            <!-- termini d'uso -->
            <span class="d-flex justify-content-end align-items-end mb-2 pe-1">
                Map data &#169;2020 Google 200 m Terms of Use Report a map error
            </span>
        </div>

    </div>


    <!-- info contatti -->
    <!-- <div id="location">

    </div> -->

    <!-- news -->
    <!-- <div id="news">

    </div> -->

    <!-- prezzo dei tickets -->
    <!-- <div id="tickets">

    </div> -->

    <!-- media -->
    <!-- <div id="media">

    </div> -->

    <!-- lista degli sponsor -->
    <!-- <div id="sponsor">

    </div> -->
</template>

<script>
export default {
    name: 'MainContent',
    data() {
        return {
            infoList: [
                {
                    icon: "fas fa-trophy",
                    url: "#",
                    title: "WHO WE ARE",
                    text: "Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.",
                    add: "Learn More"
                },
                {
                    icon: "fas fa-bolt",
                    url: "#",
                    title: "WHAT WE DO",
                    text: "Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.",
                    add: "Learn More"
                },
                {
                    icon: "fas fa-question",
                    url: "#",
                    title: "WHY US?",
                    text: "Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.",
                    add: "Learn More"
                },
            ],
            countNumb: [
                {
                    number: 3399,
                    text: "DAYS",
                    bg: "#000",
                    transp: "0.8"
                },
                {
                    number: 17,
                    text: "HOURS",
                    bg: "#000",
                    transp: "0.7"
                },
                {
                    number: 28,
                    text: "MINS",
                    bg: "#000",
                    transp: "0.6"
                },
                {
                    number: 17,
                    text: "SECS",
                    bg: "#000",
                    transp: "0.5"
                },
            ],
            listCard: [
                {
                    img: require("../assets/img/speaker-6.jpg"),
                    alt: "patrick_spencer_img",
                    name: "PATRICK SPENCER",
                    job: "S&P Analyzer"
                },
                 {
                    img: require("../assets/img/speaker-5.jpg"),
                    alt: "janet_jones_img",
                    name: "JANET JONES",
                    job: "Newyork Post's GM"
                },
                 {
                    img: require("../assets/img/speaker-4.jpg"),
                    alt: "michael_dover_img",
                    name: "MICHAEL DOVER",
                    job: "Starbuck's CEO"
                },
                 {
                    img: require("../assets/img/speaker-3.jpg"),
                    alt: "angelina_holy_img",
                    name: "ANGELINA HOLY",
                    job: "Maxii's Manager"
                },
            ],
            listCardDay: [
                {
                    nDay: "DAY 1",
                    date: "23 May 2016"
                },
                 {
                    nDay: "DAY 2",
                    date: "23 May 2030"
                },
                 {
                    nDay: "DAY 3",
                    date: "24 May 2030"
                },
                 {
                    nDay: "DAY 4",
                    date: "25 May 2030"
                },
                 {
                    nDay: "DAY 5",
                    date: "26 May 2030"
                }, {
                    nDay: "",
                    date: ""
                },
            ],
            mapPuzzle: [
                {
                    item: require("../assets/img/vt (17).png"),
                    alt: "vt_17_img"
                },
                {
                    item: require("../assets/img/vt (11).png"),
                    alt: "vt_11_img"
                },
                {
                    item: require("../assets/img/vt (1).png"),
                    alt: "vt_1_img"
                },
                {
                    item: require("../assets/img/vt (5).png"),
                    alt: "vt_5_img"
                },
                {
                    item: require("../assets/img/vt (2).png"),
                    alt: "vt_2_img"
                },
                {
                    item: require("../assets/img/vt (25).png"),
                    alt: "vt_25_img"
                },
                ////////
                {
                    item: require("../assets/img/vt (9).png"),
                    alt: "vt_9_img"
                },
                {
                    item: require("../assets/img/vt (3).png"),
                    alt: "vt_3_img"
                },
                {
                    item: require("../assets/img/vt (6).png"),
                    alt: "vt_6_img"
                },
                {
                    item: require("../assets/img/vt (20).png"),
                    alt: "vt_20_img"
                },
                {
                    item: require("../assets/img/vt (24).png"),
                    alt: "vt_24_img"
                },
                {
                    item: require("../assets/img/vt (7).png"),
                    alt: "vt_7_img"
                },
                {
                    item: require("../assets/img/vt (8).png"),
                    alt: "vt_8_img"
                },
                {
                    item: require("../assets/img/vt (10).png"),
                    alt: "vt_10_img"
                },
                {
                    item: require("../assets/img/vt (12).png"),
                    alt: "vt_12_img"
                },
                {
                    item: require("../assets/img/vt (13).png"),
                    alt: "vt_13_img"
                },
                {
                    item: require("../assets/img/vt (14).png"),
                    alt: "vt_14_img"
                },
                {
                    item: require("../assets/img/vt (15).png"),
                    alt: "vt_15_img"
                },
                {
                    item: require("../assets/img/vt (16).png"),
                    alt: "vt_16_img"
                },
                {
                    item: require("../assets/img/vt.png"),
                    alt: "vt_img"
                },
                {
                    item: require("../assets/img/vt (18).png"),
                    alt: "vt_18_img"
                },
                {
                    item: require("../assets/img/vt (19).png"),
                    alt: "vt_19_img"
                },
                {
                    item: require("../assets/img/vt (21).png"),
                    alt: "vt_21_img"
                },
                {
                    item: require("../assets/img/vt (22).png"),
                    alt: "vt_22_img"
                },
                {
                    item: require("../assets/img/vt (23).png"),
                    alt: "vt_23_img"
                },
                {
                    item: require("../assets/img/vt (26).png"),
                    alt: "vt_26_img"
                },
            ]
        }
    },
}
</script>

<style scoped lang="scss">
@import "../assets/scss/Hover-Color.scss";
@import "../assets/scss/ListStyle.scss";
$text-main-color: white;
$text-main-color-2: #272727;
$text-main-color-3: #878787;

#call-to-action {
    width: 100%;
    height: 65vh;
    background: url(../assets/img/slider-1-bg.jpg);
    background-size: cover;
    background-position: center;

    #jumbo-text {
        color: $text-main-color;

        h1 {
            font-size: 55px;
            font-weight: 300;

            &:nth-child(2) {
                font-size: 85px;
                font-weight: 700;
            }
        }

        #meet {
            width: 30%;
            border-top: 4px solid $text-main-color;
            
            h5 {
                padding: 4px;
                font-size: 17px;
                font-weight: 700;
            }
        }

        button {
            border: 0;
            background: $hover-color;
            color: $text-main-color;
            font-weight: 600;
            font-size: 15px;
        }
    }
}

#info-company {
    width: 100%;
    height: 30vh;

    .info-text {
        width: 21%;
        height: 70%;
        text-align: left;

        .info-header {
            color: #b3b3b3;

            h6 {
                color: $text-main-color-2;
            }
        }

        p {
            font-size: 14px;
            color: $text-main-color-3;
        }

        a {
            color: $hover-color;
            font-style: italic;
        }
    }
}

#countdown {
    width: 100%;
    height: 54vh;
    background: url(../assets/img/coutdown-bg1.jpg);
    background-size: container;
    background-position: center;

    #content-card {
        height: 70%;
         .card-area {
            color: $text-main-color;

            h1 {
                font-size: 50px;
                font-weight: 700;
            }
        }

        #update {
            font-size: 13px;
            
            input {
                outline: 0;
                border: 0;
                width: 22%;
            }

            button {
                font-weight: 700;
                border-width: 0 0 3px 0;
                border-color: #d92719;
                background: $hover-color;
                color: $text-main-color;
            }
        }
    }   
}

#team-members {
    width: 100%;
    height: 55vh;
    background: #f1f1f1;

    #team-area {
        width: 59%;
        height: 40vh;

            #navigation {
                width: 100%;

                #change-card {

                    button {
                        font-size: 11px;
                        border: 0;
                        border-radius: 3px;
                        background: $hover-color;
                        color: $text-main-color;
                    }
                }
            }

            img {
                border-radius: 4px;
                max-width: 100%;
                height: 68%;
            }

            .card-team {

                span {
                    color: $text-main-color-3;
                    font-size: 13px;
                }
            }
    }
}

#program-company {
    width: 100%;
    height: 70vh;

    #program-area {
        width: 59%;

        #program-header {

            p {
                width: 57%;
                font-size: 15px;
            }

            span {
                font-size: 14px;
                color: $hover-color;
            }
        }

        #program-content {
            background: $hover-color;

            .card-day {
                width: 30%;     
                border-right: 1px solid #be281a;
                
                &:last-child {
                    border: 0;
                }

                &:hover {
                    background: #be281a;
                }
                
                li {
                    list-style-type: $text-list-item;

                    a {
                        text-decoration: $list-item;
                        color: $text-main-color;

                        span {
                            font-size: 13px;
                        }
                    }
                }
            }

            #meeting {
                height: 30vh;
                background: #f6f6f6;

                #info-meet {
                    width: 49%;
                    height: 22vh;

                    ul {
                        width: 70%;

                        li {
                            padding: 20px;
                            list-style-type: $text-list-item;

                            a {
                                color: $text-main-color-3;
                                text-decoration: $list-item;
                                font-size: 12px;
                                
                                &:hover span {
                                    color: $hover-color;
                                }
                            }
                        }
                    }
                }

                .program-text {
                    height: 25vh;
                }
            }
        }
            
    }
}

#map {
    width: 100%;
    height: 50vh;

        img {
            width: 10%;
            //height: 10%;
        }
    
    .label {

        a {
            text-decoration: $list-item;
            background: $text-main-color;

            h5 {
                font-size: 18px;
            }

            &:nth-last-child(1) {
                color: $text-main-color-3;
            }
        }     
    }

    span {
        font-size: 10px;
        font-weight: 600;
    }
}
</style>