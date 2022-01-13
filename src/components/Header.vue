<template>
    <div class="nav">
        <div class="container">
                <div class="logo">
                    <img src="../assets/img/dc-logo.png" alt="">
                </div>
                <ul>
                        <li><a href="#">characters</a></li>
                        <li><a href="#">comics</a></li>
                        <li><a href="#">movies</a></li>
                        <li><a href="#">tv</a></li>
                        <li><a href="#">games</a></li>
                        <li><a href="#">collectibles</a></li>
                        <li><a href="#">videos</a></li>
                        <li><a href="#">fans</a></li>
                        <li><a href="#">news</a></li>
                        <li><a href="#">shop</a></li>
                </ul>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Header',
    data(){
        return {
            title: "Lorem Ipsum"
        }
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import "../assets/scss/style.scss";
    .logo {
        flex-grow: 4;
        img {
            width: 60px;
        }
    }

    ul {
        list-style: none;
        height: 100%;
        display: flex;
        justify-content: center;
        li {
            display: flex;
            align-items: center;
            text-transform: uppercase;
            margin: 0 1em 0 1em;
            a {
                text-decoration: none;
                display: inline-block;
                font-weight: 800;
                font-size: 1em;
                line-height: 100px;
                color: black;
                border-bottom: 0.4em solid transparent;
                &.active,
                &:hover {
                    color: $bluehover;
                    border-bottom: 0.4em solid $bluehover;
                }
            }
            
        }
    }
</style>