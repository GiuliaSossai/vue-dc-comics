<template>
  <main>
      <div class="jumbotron"></div>

      <div class="container">
         <div class="main-cards">
            <MakeCard
               v-for="(card, index) in CardsList"  
               :key="index" 
               :card="card"
            />
            
         </div>
      </div> 
   </main>
</template>

<script>

import MakeCard from './MakeCard';
import CardsList from '../assets/data/cards';

export default {
   name: 'Main',

   components:{
      MakeCard
   },

   data(){
      return{
         CardsList
      }
   }
}
</script>

<style lang="scss">
   main{
      background-color: #1C1C1C;
      .jumbotron{
         height: 300px;
         overflow: hidden;
         background-position: top;
         background-image: url('../assets/img/jumbotron.jpg');
         background-size: cover;
      }

      .container{
         color: #fff;
         padding: 3rem 0;
         text-transform: uppercase;
         .main-cards{
            display: flex;
            flex-wrap: wrap;
         }
      }
      
   }
</style>