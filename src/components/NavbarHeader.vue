<template>
    <!-- barra menu header -->
    <div class="row">
        <div id="navbar" class="col-12 d-flex justify-content-evenly align-items-center mx-auto">
            <!-- logo -->
            <img src="../assets/img/logo.png" alt="logo_img">

            <!-- lista menu -->
            <nav>
                <ul class="d-flex justify-content-around align-items-baseline mt-1">
                <!-- gli elementi della barra menu andranno ciclati -->
                    <li class="mx-2"
                    v-for="(menuItem, index) in listMenu" :key="index">
                        <a href="#" class="py-2 mx-2">
                            {{ menuItem.text }}
                        </a>
                    </li>
                <!-- icona di ricerca -->                  
                    <li class="mx-2">
                        <div id="search-button" class="d-flex align-items-center ms-3 mt-2">
                            <a href="#">
                                <font-awesome-icon icon="fas fa-search" />
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
                    text: "HOME"
                },
                {
                    text: "PAGES"
                },
                {
                    text: "PROGRAM"
                },
                {
                    text: "TICKETS"
                },
                {
                    text: "SPEAKERS"
                },
                {
                    text: "PAPERS"
                },
                {
                    text: "BLOG"
                },
                {
                    text: "SHORTCODES"
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
$list-item: none;
$text-list-item: none;
$text-color: #7d7d7c;
$hover-color: #f2291b;
.row {
    width: 100%;
    height: 107px;
     // debug
    background: orange;

    #navbar {
    width: 65%;
   
    li {
        list-style-type: $list-item;

        a {
            text-decoration: $text-list-item;
            color: $text-color;
            font-size: 13px;
            font-weight: 700;

            &:hover {
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
        }
    }
}
}
</style>