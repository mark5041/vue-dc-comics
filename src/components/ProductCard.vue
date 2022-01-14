<template>
  <div class="item">
    <img :src="img" :alt="alt">
    <span>{{titolo}}</span>
  </div>
</template>

<script>
export default {  
    name: "Product",
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
        color: 'blue'
        }
    }
}
</script>

<style lang="scss">
  .item {
        display: flex;
        align-items: center;
        flex-grow: 1;

        img {
            max-width: 60px;
            max-height: 60px;
            margin-right: 0.5em;
        }
    }
</style>