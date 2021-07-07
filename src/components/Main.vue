<template>
  <main>
    
      <div class="content">
        <!-- inizio jumbotron -->
        <div class="jumbo"></div>
        <!-- fine jumbotron -->

        <div class="container">
          <h2> Content goes here </h2>
          <ImgCard v-for="(card,i) in cards" :key="i" :cardData="card"/>
        </div>
      </div>
      
      <div class="items-shop">
        <div class="container">
        <ul>
          <li v-for="(item,i) in items" :key="i">
            <img :src="getImgUrl(item.img)" :alt="item.alt">
            <span> {{item.text}} </span>
          </li>
        </ul>
        </div>
      </div>
  </main>
</template>


<script>
import ImgCard from '@/components/ImgCard.vue';
import DcItems from '@/data/DcItems.js';

  export default {
    name: 'Main',
    components: {
      ImgCard
    },
    data(){
      return{
        items : [
          {
            img : 'buy-comics-digital-comics.png',
            alt : 'Digital comics',
            text : 'Digital comics'
          },
          {
            img : 'buy-comics-merchandise.png',
            alt : 'Dc merchandise',
            text : 'Dc merchandise'
          },
          {
            img : 'buy-comics-subscriptions.png',
            alt : 'Subscription',
            text : 'Subscription'
          },
          {
            img : 'buy-comics-shop-locator.png',
            alt : 'Comic shop locator',
            text : 'Comic shop locator'
          },
          {
            img : 'buy-dc-power-visa.svg',
            alt : 'Dc power visa',
            text : 'Dc power visa'
          },
        ],
        cards : DcItems
      }
    },
    methods : {
      getImgUrl(pic) {
        return require('../assets/img/' + pic)
      }
    }
  }
</script>


<style lang="scss" scoped>
  @import '@/style/variables.scss';

  .content,
  .items-shop{
    padding: 40px 0;
    color: white;
  }

  .content{
    background-color: #1c1c1c;

    .jumbo{
      height: 400px;
      background-image: url('../assets/img/jumbotron.jpg');
      background-size: cover;
    }
  }

  .items-shop{
    background-color: $dc-color;

    ul{
      list-style: none;
      display: flex;
      justify-content: space-around;
      align-items: center;
      text-transform: uppercase;

      li{
        display: inline-block;

        img{
          height: 50px;
          vertical-align: middle;
          margin-right: 10px;
        }
      }
    }
  }



</style>