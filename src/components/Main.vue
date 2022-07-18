<template>
    <main>
        <div class="content-container">
            <div>
                Content goes here </div>
            </div>

            <div class="main-options-container">
                <ul>
                    <li v-for="(option, index) in mainOptions" :key="index">
                        <img :src="require(`../assets/img/${option.image}`)" :alt="option.link">
                        <p>
                            {{ option.link }}
                        </p>
                    </li>
                </ul>
            </div>
    </main>
</template>

<script>
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
                    image: "buy-comics-subsriptions.png"
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
        }
    },
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";


.img-container{
    height: 60px;
    margin-right: 15px;

    img{
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
    background-color: blue;
    display: flex;
    justify-content: center;
    padding: 50px;
}
</style>