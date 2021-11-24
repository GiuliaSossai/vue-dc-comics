<template>
  <header>
     <div class="container">
        <div class="header-left">
            <img src="../assets/img/dc-logo.png" alt="">
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
   header {
      height: 150px;
      .container {
         height: 150px;
         text-transform: uppercase;
         font-weight: bold;
         display: flex;
         justify-content: space-between;
         align-items: center;
         ul {
            height: 147px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            a {
               padding: 0 1rem;
               line-height: 147px;
               &.active,
               &:hover {
                  color: #0282F9;
                  border-bottom: 3px solid #0282F9;
               }
            }
          
         }
      }
   }
   
</style>