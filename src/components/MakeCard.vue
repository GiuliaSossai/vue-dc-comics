<template>
  <div class="card-box">
     <img :src="card.thumb" :alt="card.series">
     
     <h5>{{card.series}}</h5>
  </div>

</template>

<script>
export default {
   name: 'MakeCard',
   props: {
      card: Object
   }
}
</script>

<style lang="scss">
   @import '../assets/style/mixins.scss';
   @import '../assets/style/var.scss';

   .card-box {
      flex-basis: calc(100% / 6);
      border: 1rem solid #1C1C1C;
      margin-bottom: 1rem;
      img {
         width: 100vw;
         height: 188px;
         object-fit: cover;
         object-position: top;
      }
      h5 {
         padding-top: 8px;
      }
   }
</style>