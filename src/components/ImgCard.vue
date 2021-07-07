<template>
  <div>
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

</style>