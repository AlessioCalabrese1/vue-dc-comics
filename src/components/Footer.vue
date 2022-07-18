<template>
  <div>
    <div class="footer-links-container">
        <div class="footer-links d-flex  justify-content-between">
            <div class="d-flex row row-cols-3">
                <ul v-for="(object, objectIndex) in footerLinks" :key="objectIndex">
                <p>{{object.name}}</p>
                <li v-for="(link, index) in object.links" :key="index">
                    {{link}}
                </li>
                </ul>
            </div>
            
            <div class="banner-logo">
                
            </div>
        </div>
    </div>

    <div class="sign-in-background d-flex justify-content-center">
        <div class="sign-in d-flex justify-content-between">
        <div>
            <a href="#" class="sing-btn btn">Sing Up Now!</a>
        </div>

        <div>
            <p class="follow">Follow Us</p>

            <div class="socials">
               <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" integrity="sha512-KfkfwYDsLkIlwQp6LFnl8zNdLGxu9YAA1QvwINks4PhcElQSvqcyVLLD9aMhXd13uQjoXtEKNosOWaZqXgel0g==" crossorigin="anonymous" referrerpolicy="no-referrer" />
            </div>
        </div>

    </div>
    </div>
    
  </div>
</template>

<script>
export default {
    data: function(){
        return{
            footerLinks:[
                {
                    name: "Dc Comics",
                    links: [
                        "Character",
                        "Comics",
                        "Character",
                        "Comics",
                        "Character",
                        "Comics",
                    ]
                },

                {
                    name: "Dc",
                    links: [
                        "Character",
                        "Comics",
                        "Character",
                        "Comics",
                        "Character",
                        "Comics",
                        "Character",
                        "Comics",
                    ]
                },

                {
                    name: "Sites",
                    links: [
                        "Character",
                        "Comics",
                        "Character",
                    ]
                },

                {
                    name: "Shop",
                    links: [
                        "Character",
                        "Comics",
                    ]
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

.banner-logo{
    width: 60%;
    height: 320px;
    background-image: url(../assets/img/dc-logo-bg.png);
    background-position: center;
    background-repeat: no-repeat;
    position: relative;
    top: -20px;
    right: 0;
}
ul{
    list-style: none;
    padding: 0;
    margin: 0;
    padding-right: 25px;
    li{
        color: white;
        font-size: 12px;
        color:gray;
    }

    p{
        color: white;
        font-weight: bold;
        font-size: 20px;
    }
}
.footer-links-container{
    background-image: url(../assets/img/footer-bg.jpg);
    padding: 20px 0;
    height: 320px;
}
.footer-links{
    width: $elements-width;
    margin: 0 auto;
}

.sign-in-background{
    background-color: #303030;
    padding: 20px 0;
}

.sign-in{
    width: $elements-width;
}

.sing-btn{
    color: white;
    font-weight: 600;
    border: 2px solid $brandBackGroundColor;
    border-radius: 0;
}

.follow{
    color: $brandBackGroundColor;
    font-weight: bold;
    font-size: 20px;
}
</style>