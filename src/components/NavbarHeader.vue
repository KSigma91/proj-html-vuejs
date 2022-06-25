<template>
    <!-- barra menu header -->
    <div class="row">
        <div id="navbar" class="d-flex justify-content-evenly align-items-center mx-auto">
            <!-- logo -->
            <img src="../assets/img/logo.png" alt="logo_img">

            <!-- lista menu -->
            <nav>
                <ul class="d-flex justify-content-around align-items-baseline mt-1 mx-auto col-md-8">
                    <!-- gli elementi della barra menu andranno ciclati -->
                    <li class="mx-3"
                    v-for="(menuItem, index) in listMenu" :key="index"
                    >
                        <a :href="menuItem.url" class="py-2">
                            {{ menuItem.text }}
                        </a>
                    </li>

                    <!-- icona di ricerca -->                  
                    <li class="mx-auto">
                        <div id="search-button" class="d-flex align-items-center ms-3 mt-2">
                            <a href="#">
                                <font-awesome-icon icon="fas fa-search" class="mx-4" />
                            </a>
                        </div> 
                    </li>                           
                </ul>    
            </nav>        
        </div>
    </div>
</template>

<script>
export default {
    name: 'NavbarHeader',
    data() {
        return {
            listMenu: [
                {
                    text: "HOME",
                    url: "#",
                    current: false
                },
                {
                    text: "PAGES",
                    url: "#",
                    current: false
                },
                {
                    text: "PROGRAM",
                    url: "#",
                    current: false
                },
                {
                    text: "TICKETS",
                    url: "#",
                    current: false
                },
                {
                    text: "SPEAKERS",
                    url: "#",
                    current: false
                },
                {
                    text: "PAPERS",
                    url: "#",
                    current: false
                },
                {
                    text: "BLOG",
                    url: "#",
                    current: false
                },
                {
                    text: "SHORTCODES",
                    url: "#",
                    current: false
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/scss/Hover-Color.scss";
@import "../assets/scss/Text-Color.scss";
$list-item: none;
$text-list-item: none;
.row {
    width: 100%;
    height: 107px;

    #navbar {
        width: 70%;

        img {
            max-width: 100%;
        }
   
        li {
            list-style-type: $list-item;

            a {
                text-decoration: $text-list-item;
                color: $text-color;
                font-size: 13px;
                font-weight: 700;

                &:not(#search-button):hover {
                    border-bottom: 3px solid $hover-color;
                    color: $hover-color;
                }
            }
        }

        #search-button {
            border-left: 2px solid $text-color;
            height: 12px;
            padding: 0 30px;
            font-size: 13px;

            a {
                color: $text-color;

                &:not(#search-button):hover {
                    border-bottom: none;
                    color: $hover-color;
                }
            }
        }
    }
}
</style>