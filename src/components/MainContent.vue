<template>
    <div class="container-fluid">

         <!-- jumbotron -->
        <div id="call-to-action" class="row d-flex flex-column justify-content-around">

            <!-- testo del jumbotron -->
            <div id="jumbo-text" class="">
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

    </div>
   

   

   

    <!-- presentazione del team -->
    <!-- <div id="team-members">

    </div> -->

    <!-- calendario programma -->
    <!-- <div id="program">

    </div> -->

    <!-- posizione google maps -->
    <!-- <div id="map">

    </div> -->

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
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/scss/Hover-Color.scss";
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
</style>