<template>
    <main>
        <div class="content-section">
            <div class="container">
                <h1>--> Content goes here &#60;-- </h1>
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
import ProductCard from './ProductCard.vue'
export default {
  name: 'Main',
  components: {
    ProductCard,
  },
    data(){
        return {
            title: "Lorem Ipsum",
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
        border-bottom: 15px solid red; 
        .container {
            align-items: center;

            h1 {
                color: white;
                padding: 1.5em 0;
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