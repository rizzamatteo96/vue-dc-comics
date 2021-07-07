<template>
  <header>
    <div class="container">

      <!-- logo DC -->
      <img src="../assets/img/dc-logo.png" alt="dc logo">

      <!-- inizio navbar -->
      <nav>
        <ul>
          <li v-for="(link,i) in links" :key="i" :class="{active : link.active}"><a :href="link.url"> {{link.text}} </a></li>
        </ul>
      </nav>
      <!-- fine navbar -->

    </div>
  </header>
</template>


<script>
  export default {
    name: 'Header',
    data(){
      return{
        links : [
          {
            text : 'Characters',
            url : '#',
            active : true
          },
          {
            text : 'Comics',
            url : '#',
            active : false
          },
          {
            text : 'Movies',
            url : '#',
            active : false
          },
          {
            text : 'Tv',
            url : '#',
            active : false
          },
          {
            text : 'Games',
            url : '#',
            active : false
          },
          {
            text : 'Collectibles',
            url : '#',
            active : false
          },
          {
            text : 'Videos',
            url : '#',
            active : false
          },
          {
            text : 'Fans',
            url : '#',
            active : false
          },
          {
            text : 'News',
            url : '#',
            active : false
          },
          {
            text : 'Shop',
            url : '#',
            active : false
          }
        ]
      }
    }
  }
</script>


<style lang="scss" scoped>
  @import '@/style/variables.scss';
  header{
    height: 100px;
    padding: 10px 0;

    .container{
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 100%;

      img{
        height: 100%;
      }
    
      ul{
        list-style: none;
        text-transform: uppercase;
        height: 100%;
        display: inline-block;
        vertical-align: middle;
        line-height: 100px;
    
        li{
          display: inline-block;
          position: relative;
          padding: 0 10px;
          // height: 100%;

          &.active{
            ::after{
              content: '';
              background-color: $dc-color;
              display: block;
              position: absolute;
              bottom: 0;
              left: 0;
              right: 0;
              height: 5px;
            }
          }

          &:hover,
          &.active{
            a{
              color: $dc-color;
            }
          }
          
          a{
            text-decoration: none;
            color: black;
          }
        }
      }
    }
  }
</style>