<template>
    <footer>
        <div class="footer-container">
            <div class="background-logo">
                <div class="container">
                    <div class="first-col">
                    <h3>dc comics</h3>
                    <ul>
                        <li><a>Characters</a></li>
                        <li><a>Comics</a></li>
                        <li><a>Movies</a></li>
                        <li><a>TV</a></li>
                        <li><a>Games</a></li>
                        <li><a>Videos</a></li>
                        <li><a>News</a></li>
                    </ul>
                    <h3>shop</h3>
                    <ul>
                        <li><a>Shop DC</a></li>
                        <li><a>Shop DC Collectibles</a></li>
                    </ul>
                </div>
                <div class="second-col">
                    <h3>dc</h3>
                    <ul>
                        <li><a>Terms Of Use</a></li>
                        <li><a>Privacy policy (New)</a></li>
                        <li><a>Ad Choiches</a></li>
                        <li><a>Advertising</a></li>
                        <li><a>Jobs</a></li>
                        <li><a>Subscriptions</a></li>
                        <li><a>Talent Workshops</a></li>
                        <li><a>CPSC Certificates</a></li>
                        <li><a>Ratings</a></li>
                        <li><a>Shop Help</a></li>
                        <li><a>Contact Us</a></li>
                    </ul>
                </div>
                <div class="third-col">
                    <h3>sites</h3>
                    <ul>
                        <li><a>DC</a></li>
                        <li><a>MAD Magazine</a></li>
                        <li><a>DC Kids</a></li>
                        <li><a>DC Universe</a></li>
                        <li><a>DC Power Visa</a></li>
                    </ul>
                </div>
                </div>
            </div>
        </div>
        <div class="footer-end">
            <div class="container">
                <div class="sign-up-button">
                    <a href="#">sign-up now!</a>
                </div>
                <div class="social-icon">
                    <h3>follow us</h3>
                    <ul>
                        <li v-for="(element, index) in social" :key ="index">
                            <img :src="`${element.image}`" alt="">
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
  name: 'Header',
    data(){
        return {
            title: "Lorem Ipsum",
            social: [
                {
                    image: require("../assets/img/footer-facebook.png"),
                },
                {
                    image: require("../assets/img/footer-twitter.png"),
                },
                {
                    image: require("../assets/img/footer-youtube.png"),
                },
                {
                    image: require("../assets/img/footer-pinterest.png"),
                },
                {
                    image: require("../assets/img/footer-periscope.png"),
                },
            ],
        }
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import "../assets/scss/style.scss";
    .footer-container {
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: contain;
        
        .background-logo {
            padding: 2em 0;
            background-image: url('../assets/img/dc-logo-bg.png');
            background-repeat: no-repeat;
            background-position-x: 85%;
            background-position-y: 50%;

            .first-col, .second-col, .third-col {
                float: left;
                width: 15%;

                h3 {
                    text-transform: uppercase;
                    padding: 0.8em 0;
                    color: white;
                }

                ul {
                    list-style: none;

                    li {
                        padding-bottom: 0.5em;
                        font-size: 0.9em;

                        a {
                            text-decoration: none;
                            color: $text_grey;
                        }
                    }
                }
            }
            
        }        
    }
        
    .footer-end {
        background-color: $footer_bottom;
        .container {
            display: flex;
            justify-content: space-between;
            text-transform: uppercase;
            padding: 2em 0;

            .sign-up-button {
                border: 2px solid $lightblue;
                padding: 1em;

                a {
                    text-decoration: none;
                    color: white;
                }
            }
            .social-icon {
                display: flex;
                align-items: center;

                h3 {
                    padding-right: 2em;
                    color: $lightblue;
                }

                ul li {
                    display: inline-block;
                    padding: 0 0.5em;
                }
            }
        }
    }
</style>