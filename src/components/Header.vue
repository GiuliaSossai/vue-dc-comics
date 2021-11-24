<template>
  <header>
     <div class="container">
        <div class="header-left">
            <a href="#"><img src="../assets/img/dc-logo.png" alt="dc logo"></a> 
         </div>
         <div class="header-right">
            <ul>
               <li v-for="(link, index) in links" :key="index">
                  <a :class="{active: link.current}" href="link.url">{{link.text}}</a>
               </li>
            </ul>
         </div>
     </div>
  </header>
</template>

<script>
export default {
   name: 'Header',
   data(){
      return{
         links:[
            {
               url:'/characters',
               text: 'characters',
               current: false
            },
            {
               url:'/comics',
               text: 'comics',
               current: true
            },
            {
               url:'/movies',
               text: 'movies',
               current: false
            },
            {
               url:'/tv',
               text: 'tv',
               current: false
            },
            {
               url:'/games',
               text: 'games',
               current: false
            },
            {
               url:'/collectibles',
               text: 'collectibles',
               current: false
            },
            {
               url:'/videos',
               text: 'videos',
               current: false
            },
            {
               url:'/fans',
               text: 'fans',
               current: false
            },
            {
               url:'/news',
               text: 'news',
               current: false
            },
            {
               url:'/shop',
               text: 'shop',
               current: false
            }
         ]
      }
   }
}
</script>

<style lang="scss">
   @import "../assets/style/var.scss";
   @import '../assets/style/mixins.scss';

   header {
      height: 150px;
      .container {
         height: 150px;
         text-transform: uppercase;
         font-weight: bold;
         @include flex-btw;
         ul {
            height: 147px;
            @include flex-btw;
            a {
               padding: 0 1rem;
               line-height: 147px;
               &.active,
               &:hover {
                  color: $main-color;
                  border-bottom: 3px solid $main-color;
               }
            }
          
         }
      }
   }
   
</style>