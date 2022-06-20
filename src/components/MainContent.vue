<template>
    <div class="container-fluid">

         <!-- jumbotron -->
        <div id="call-to-action" class="row d-flex flex-column justify-content-around">
            <div class="col-12">
                <!-- background -->
                <!-- <img src="../assets/img/slider-1-bg.jpg" alt="slider_bg_img"
                class="position-relative"> -->

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
        </div>

    </div>
   

    <!-- informazioni dei componenti dell'azienda -->
    <!-- <div id="info-team">

    </div> -->

    <!-- countdown -->
    <!-- <div id="countdown">

    </div> -->

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
}
</script>

<style scoped lang="scss">
@import "../assets/scss/Hover-Color.scss";
$text-main-color: white;

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
</style>