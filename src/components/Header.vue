<template>
  <header>
    <div class="head-container d-flex justify-content-between">
        <div class="img-container">
            <img class="img-fluid" src="../assets/img/dc-logo.png" alt="Logo">
        </div>

        <nav>
            <ul>
                <li v-for="(link,index) in navOptions" :key="index">
                    <a href="#">{{ link }}</a>
                </li>
            </ul>
        </nav>
    </div>
  </header>
</template>

<script>
export default {
    data: function(){
        return{
            navOptions: [
                "CHARACTERS",
                "COMICS",
                "MOVIES",
                "TV",
                "GAMES",
                "COLLECTIBLES",
                "VIDEOS",
                "FANS",
                "NEWS",
                "SHOP"
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import "../styles/variables.scss";

    .head-container{
        width: $elements-width;
        margin: 0 auto;
        
        .img-container{
            width: 80px;
            padding: 15px 0;
        }
    }

    ul{
        list-style: none;
        margin: 0;
        padding: 0;
        height: 100%;
        display: flex;
        li{
            display:  flex;
            align-items: center;
            height: 100%;
            margin-right: 20px;
            &:hover{
                border-bottom: 2px solid blue;
                a{
                    color: blue;
                }
            }
        }
    }

    a{
        font-size: 12px;
        font-weight: bold;
        color: grey;
        text-decoration: none;
    }
</style>