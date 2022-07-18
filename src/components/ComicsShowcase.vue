<template>
  <div class="comic">
    <div class="thumb-container">
        <img :src="comic.thumb" :alt="comic.series">
    </div>
    
    <p class="comic-name">
        {{comic.series}}
    </p>
  </div>
</template>

<script>
export default {
    props: {
        comic: Object,
    },
}
</script>

<style lang="scss" scoped>

    .thumb-container{
        width: 100%;
        height: 250px;
        overflow: hidden;
        img{
            width: 100%;
        }
    }

    .comic{
    width: calc((100% / 6) - 1.25rem);
    margin: 10px;
    .comic-name{
        color: white;
        text-align: start;
        font-size: 12px;
        }
    }
</style>