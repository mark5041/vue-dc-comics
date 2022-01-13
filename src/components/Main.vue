<template>
    <main>
        <div class="content-section">
            <div class="container">
                <h1>--> Content goes here &#60;-- </h1>
            </div>
        </div>
        <div class="product-section">
            <div class="container">
                <div v-for="(element, index) in products" :key ="index" class="item">
                    <img :src="`${element.image}`" alt="">
                    <span>{{element.desciption}}</span>
                </div>
            </div>
        </div>
    </main>
</template>



                
                
                


<script>
export default {
  name: 'Header',
    data(){
        return {
            title: "Lorem Ipsum",
            products: [
                {
                    image: require("../assets/img/buy-comics-digital-comics.png"),
                    desciption: "comics digital",
                },
                {
                    image: require("../assets/img/buy-comics-merchandise.png"),
                    desciption: "comics merchandise",
                },
                {
                    image: require("../assets/img/buy-comics-shop-locator.png"),
                    desciption: "comics shop locator",
                },
                {
                    image: require("../assets/img/buy-comics-subscriptions.png"),
                    desciption: "comics subscriptions",
                },
            ]
        }
    },
    created() {
        console.log(this.products[1].image);
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import "../assets/scss/style.scss";

    .content-section {
        background-color: black;
        .container {
            align-items: center;
            h1 {
                color: white;
                padding: 1.5em 0;
            }
        }
    }

    .product-section {
        background-color: blue;
        border-bottom: 1em solid yellow;
        .container {
            justify-content: space-between;
            color: white;
            padding: 50px;
            .item {
                display: flex;
                align-items: center;
                img {
                    max-width: 60px;
                    max-height: 60px;
                    margin-right: 0.5em;
                }
            }
        }
    }


</style>