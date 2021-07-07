<template>
  <div class="card">
    <img :src="cardData.thumb" :alt="cardData.series">
    <div> {{cardData.series}} </div>
  </div>
</template>


<script>
export default {
  name : 'ImgCard',
  props: {cardData: Object}
}
</script>


<style lang="scss" scoped>


  .card{
    width: calc((100% - (10px * 6))/6);
    margin: 40px 0;

    img{
      margin-bottom: 10px;
    }
  }
</style>