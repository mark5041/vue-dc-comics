<template>
  <div class="thumb">
        <div class="image-box">
            <img :src="img" :alt="alt">
        </div>
        <span class="thumb-title">{{titolo}}</span>
    </div>
</template>

<script>
export default {  
    name: "ThumbCard",
    props: {
        img: {
            type: String,
        },
        alt: {
            type: String,
        },
        titolo: {
            type: String,
        },
        product: Object,
    },
    data() {
        return {

        }
    }
}
</script>

<style lang="scss">
.thumb {
    flex-basis: calc(100% / 6 - 2.4em);
    .image-box {
        width: 100%;
        max-height: 200px;
        overflow: hidden;
        margin-bottom: 1em;
        img {
            width: 100%;
        }
    }
    .thumb-title {
        color: white;
        text-transform: uppercase;
        font-size: 0.8em;
    }
}
</style>