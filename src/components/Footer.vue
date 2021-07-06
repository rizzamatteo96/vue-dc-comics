<template>
  <footer>
    <!-- inizio parte top -->
    <div class="top">
      <div class="container">
        <!-- inizio prima colonna -->
        <div class="col">
          <h3>Dc comics</h3>
          <ul>
            <li v-for="(item,i) in dcComics" :key="i"><a :href="item.link"> {{item.text}} </a></li>
          </ul>

          <h3>Shop</h3>
          <ul>
            <li v-for="(item,i) in shop" :key="i"><a :href="item.link"> {{item.text}} </a></li>
          </ul>
        </div>
        <!-- fine prima colonna -->

        <!-- inizio seconda colonna -->
        <div class="col">
          <h3>Dc</h3>
          <ul>
            <li v-for="(item,i) in dc" :key="i"><a :href="item.link"> {{item.text}} </a></li>
          </ul>
        </div>
        <!-- fine seconda colonna -->

        <!-- inizio terza colonna -->
        <div class="col">
          <h3>Sites</h3>
          <ul>
            <li v-for="(item,i) in sites" :key="i"><a :href="item.link"> {{item.text}} </a></li>
          </ul>
        </div>
        <!-- fine terza colonna -->

        <!-- inizio colonna logo -->
        <div class="col-logo"></div>
        <!-- fine colonna logo -->
      </div>
    </div>
    <!-- fine parte top -->

    <!-- inizio parte bottom -->
    <div class="bottom">
      <div class="container">

      </div>
    </div>
    <!-- fine parte bottom -->
  </footer>
</template>


<script>
  export default {
    name: 'Footer',
    data(){
      return{
        dcComics : [
          {
            text : 'Characters',
            link : '#'
          },
          {
            text : 'Comics',
            link : '#'
          },
          {
            text : 'Movies',
            link : '#'
          },
          {
            text : 'TV',
            link : '#'
          },
          {
            text : 'Games',
            link : '#'
          },
          {
            text : 'Videos',
            link : '#'
          },
          {
            text : 'News',
            link : '#'
          }
        ],
        shop : [
          {
            text : 'Shop DC',
            link : '#'
          },
          {
            text : 'Shop DC Collectibles',
            link : '#'
          }
        ],
        dc : [
          {
            text : 'Terms Of Use',
            link : '#'
          },
          {
            text : 'Privacy policy (New)',
            link : '#'
          },
          {
            text : 'Ad Choices',
            link : '#'
          },
          {
            text : 'Advertising',
            link : '#'
          },
          {
            text : 'Jobs',
            link : '#'
          },
          {
            text : 'Subscriptions',
            link : '#'
          },
          {
            text : 'Talent Workshops',
            link : '#'
          },
          {
            text : 'CPSC Certificates',
            link : '#'
          },
          {
            text : 'Rating',
            link : '#'
          },
          {
            text : 'Shop Help',
            link : '#'
          },
          {
            text : 'Contact Us',
            link : '#'
          }
        ],
        sites : [
          {
            text : 'DC',
            link : '#'
          },
          {
            text : 'MAD Magazine',
            link : '#'
          },
          {
            text : 'DC Kids',
            link : '#'
          },
          {
            text : 'DC Universe',
            link : '#'
          },
          {
            text : 'DC Power Visa',
            link : '#'
          }
        ]
      }
    }
  }
</script>


<style lang="scss" scoped>
  @import '@/style/variables.scss';

  .top{
    background-image: url('../assets/footer-bg.jpg');
    background-position: center;
    background-size: cover;
    height: 400px;
    color: white;

    .container{
      height: 100%;

      .col{
        float: left;
        margin-right: 20px;
        padding: 40px 0;
  
        h3{
          margin: 15px 0;
          text-transform: uppercase;
        }
  
        ul{
          list-style: none;
          font-size: 1rem;
  
          li{
            padding-top: 5px;
  
            a{
              text-decoration: none;
              color: gray;
            }
          } 
          
        }
      }
  
      .col-logo{
        float: right;
        height: 100%;
        width: 50%;
        background-image: url('../assets/dc-logo-bg.png');
        background-size: cover;
        background-position: center;
      }
    }

    ::after{
      content: '';
      display: table;
      clear: both;
    }

  }
</style>