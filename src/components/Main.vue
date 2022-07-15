<template>
  <main>
    <div class="content-container">
        <div>
            -->Content goes here<--
        </div>
    </div>
  </main>
</template>

<script>
export default {

}
</script>

<style lang="scss">
@import "../styles/variables.scss";

.content-container{
    background-color: black;

    div{
        margin: 0 auto;
        width: $elements-width;
        font-weight: bold;
        color: white;
        font-size: 25px;
        padding: 25px 0;
    }
}
</style>