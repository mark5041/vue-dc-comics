<template>
    <main>
        <div class="content-section">
            <div class="container">
                <div class="title">
                    <h1>CURRIENT SERIES</h1>
                </div>
                <div class="thumbs">
                    <ThumbCard v-for="(element, index) in thumbs" 
                    :key="index" 
                    :img="element.thumb" 
                    :alt="element.series" 
                    :titolo="element.series" />
                </div>
            </div>
        </div>
        <div class="product-section">
            <div class="container">
                <ProductCard v-for="(element, index) in products" :key ="index" class="item" 
                :img="element.image"
                :alt="element.desciption"
                :titolo="element.desciption"
                />
            </div>
        </div>
    </main>
</template>          


<script>
import ThumbCard from './ThumbCard.vue'
import ProductCard from './ProductCard.vue'
export default {
  name: 'Main',
  components: {
    ProductCard,
    ThumbCard,
  },
    data(){
        return {
            title: "Lorem Ipsum",
            thumbs: [
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                price: "$19.99",
                series: "Action Comics",
                type: "comic book"
            },
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                price: "$3.99",
                series: "American Vampire 1976",
                type: "comic book"
            },
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                price: "$16.99",
                series: "Aquaman",
                type: "graphic novel"
            },
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                price: "$2.99",
                series: "Batgirl",
                type: "comic book"
            },
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                price: "$3.99",
                series: "Batman",
                type: "comic book"
            },
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                price: "$2.99",
                series: "Batman Beyond",
                type: "comic book"
            },
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                price: "$3.99",
                series: "Batman/Superman",
                type: "comic book"
            },
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                price: "$4.99",
                series: "Batman/Superman Annual",
                type: "comic book"
            },
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                price: "$5.99",
                series: "Batman: The Joker War Zone",
                type: "comic book"
            },
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                price: "$6.99",
                series: "Batman: Three Jokers",
                type: "comic book"
            },
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                price: "$4.99",
                series: "Batman: White Knight Presents: Harley Quinn",
                type: "comic book"
            },
            {
                thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                price: "$16.99",
                series: "Catwoman",
                type: "graphic novel"
            }
            ],
            products: [
                {
                    image: require("../assets/img/buy-comics-digital-comics.png"),
                    desciption: "COMICS DIGITAL",
                },
                {
                    image: require("../assets/img/buy-comics-merchandise.png"),
                    desciption: "COMICS MERCHANDISE",
                },
                {
                    image: require("../assets/img/buy-comics-shop-locator.png"),
                    desciption: "COMIC SHOP LOCATOR",
                },
                {
                    image: require("../assets/img/buy-comics-subscriptions.png"),
                    desciption: "COMICS SUBSCRIPTION",
                },
                {
                    image: require("../assets/img/buy-dc-power-visa.svg"),
                    desciption: "DC POWER VISA",
                },
            ]
        }
    },
    created() 
    {

    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import "../assets/scss/style.scss";

    .content-section {
        background-color: black;
        padding: 80px 0;
        .container {
            align-items: center;
            position: relative;
            .title {
                position: absolute;
                top: -20%;
                background-color: $lightblue;
                color: white;
                padding: 0.7em 1.3em;
                font-size: 0.8em;
            }
            .thumbs {
                display: flex;
                justify-content: center;
                flex-wrap: wrap;
                gap: 2.4em;
            }
        }
    }

    .product-section {
        background-color: $lightblue;

        .container {
            justify-content: space-between;
            color: white;
            padding: 50px;   
        }
    }


</style>