<template>
  <main>
      <div class="jumbotron"></div>

      <div class="container">
         <button class="big-btn">current series</button>
         <div class="main-cards">
            <MakeCard
               v-for="(card, index) in CardsList"  
               :key="index" 
               :card="card"
            />  
         </div>  
      </div>

      <button class="btn">load more</button>
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
      text-align: center;
      .jumbotron{
         height: 400px;
         background-position: top;
         background-image: url('../assets/img/jumbotron.jpg');
         background-size: cover;
      }

      .container{
         color: #fff;
         text-transform: uppercase;
         text-align: start;
         button.big-btn{
            font-size: 24px;
            padding: 8px 24px;
            margin-top: -25px;
            margin-bottom: 2rem;
         }
         .main-cards{
            display: flex;
            flex-wrap: wrap;
         }  
      }

      button.btn{
         font-size: 12px;
         padding: 8px 40px;
         margin-bottom: 1rem;      
      }  
   }
</style>