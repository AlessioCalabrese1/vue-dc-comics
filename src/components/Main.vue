<template>
    <main>
        <div class="jumbotron-container">
            <img class="img-fluid" src="../assets/img/jumbotron.jpg" alt="jumbotron">
        </div>

        <div class="comics-showcase ">
            <div class="current-series">
                Current Series
            </div>
            <div class="comics-container">
                <div class="d-flex flex-wrap pt-4">
                    <ComicsShowcase v-for="(comic, index) in comicsList" :key="index" :comic=comic />
                </div>

                <a href="#" class="btn">Load More</a>
            </div>
        </div>

        <div class="main-options-container">
            <ul>
                <li v-for="(option, index) in mainOptions" :key="index">
                    <div class="option-image-container">
                        <img class="option-image" :src="require(`../assets/img/${option.image}`)" :alt="option.link">
                    </div>
                    
                    <p class="option-text ps-3">
                        {{ option.link }}
                    </p>
                </li>
            </ul>
        </div>
    </main>
</template>

<script>
import ComicsShowcase from './ComicsShowcase.vue'
export default {
    data: function () {
        return {
            mainOptions: [
                {
                    link: "DIGITAL COMICS",
                    image: "buy-comics-digital-comics.png"
                },
                {
                    link: "DC MERCHENDISE",
                    image: "buy-comics-merchandise.png"
                },
                {
                    link: "SUBSCRIPTION",
                    image: "buy-comics-subscriptions.png"
                },
                {
                    link: "COMIC SHOP LOCATOR",
                    image: "buy-comics-shop-locator.png"
                },
                {
                    link: "DC POWER VISA",
                    image: "buy-dc-power-visa.svg"
                },
            ],
            
            comicsList:
            [
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        };
    },
    components: { ComicsShowcase }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";


.img-container {
    height: 60px;
    margin-right: 15px;

    img {
        height: 100%;
    }
}

.content-container {
    background-color: black;

    div {
        margin: 0 auto;
        width: $elements-width;
        font-weight: bold;
        color: white;
        font-size: 25px;
        padding: 25px 0;
    }
}

ul {
    margin: 0;
    padding: 0;
    list-style: none;
    display: flex;
    width: $elements-width;
    display: flex;
    justify-content: space-between;

    li {
        display: flex;
        align-items: center;
    }
}

a {
    font-weight: bold;
    text-decoration: none;
    color: white;
}

.main-options-container {
    background-color: $brandBackGroundColor;
    display: flex;
    justify-content: center;
    padding: 50px;
}

.jumbotron-container{
    height: 280px;
    overflow: hidden;
    img{
        width: 100%;
    }
}
.comics-showcase {
    background-color: #1c1c1c;
    position: relative;
}

.comics-container {
    width: 80%;
    margin: 0 auto;
    text-align: center;
}

a.btn, .current-series{
    color: white;
    background: $brandBackGroundColor;
    border-radius: 0;
    margin-bottom: 20px;
    padding: 5px 25px;
    text-transform: uppercase;
}

.current-series{
    display: inline;
    position: absolute;
    top: -16px;
    left: 180px;
    font-weight: 700;
    font-size: 18px;
}

.option-image-container{
    width: 50px;
}
.option-image{
    width: 100%;
}

.option-text{
    color: white;   
    font-size: 14px; 
    margin: 0;
}
</style>