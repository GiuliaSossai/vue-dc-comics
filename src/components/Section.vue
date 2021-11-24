<template>
  <section>
     <div class="container">
        <div class="item">
          <div class="little-img">
             <img src="../assets/img/buy-comics-digital-comics.png" alt="DC">
          </div>
          <div class="img-text">digital comics</div>
        </div>

        <div class="item">
          <div class="little-img">
             <img src="../assets/img/buy-comics-merchandise.png" alt="merchandise">
          </div>
          <div class="img-text">dc merchandise</div>
        </div>

        <div class="item">
          <div class="little-img">
             <img src="../assets/img/buy-comics-subscriptions.png" alt="subscription">
          </div>
          <div class="img-text">subscription</div>
        </div>

        <div class="item">
          <div class="little-img">
             <img src="../assets/img/buy-comics-shop-locator.png" alt="shop locator">
          </div>
          <div class="img-text">comic shop locator</div>
        </div>

        <div class="item">
          <div class="little-img">
             <img src="../assets/img/buy-dc-power-visa.svg" alt="power visa">
          </div>
          <div class="img-text">dc power visa</div>
        </div>
      </div>
   </section>
</template>

<script>
export default {
   name: 'Section'
}
</script>

<style lang="scss">
   @import "../assets/style/var.scss";
   @import '../assets/style/mixins.scss';

   section {
      background-color: $main-color;
      color: #fff;
      text-transform: uppercase;
      padding: 2rem 0;
      font-size: 14px;
      .container {
         padding: 0 2rem;
         @include flex-btw;
         .item {
            display: flex;
            align-items: center;
            .little-img {
               width: 30px;
               margin-right: 1rem;
            }
         }
      }
   }
</style>