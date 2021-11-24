<template>
  <footer>
    <div class="footer-top">
      <div class="container">
        <div class="related">
          <div class="little-title">
            <h3>dc comics</h3> 
            <p><a href="#">Characters</a></p>
            <p><a href="#">Comics</a></p>
            <p><a href="#">Movies</a></p>
            <p><a href="#">TV</a></p>
            <p><a href="#">Games</a></p>
            <p><a href="#">Videos</a></p>
            <p><a href="#">News</a></p>
            <div class="little-title listed">
              <h3>shop</h3> 
              <p><a href="#">Shop DC</a></p>
              <p><a href="#">Shop DC Collectibles</a></p>
            </div>
          </div>

          <div class="little-title">
            <h3>dc</h3>
            <p><a href="#">Terms Of Use</a></p>
            <p><a href="#">Privacy Policy (New)</a></p>
            <p><a href="#">Ad Choices</a></p>
            <p><a href="#">Advertising</a></p>
            <p><a href="#">Jobs</a></p>
            <p><a href="#">Subscriptions</a></p>
            <p><a href="#">Talent Workshops</a></p>
            <p><a href="#">CPSC Certificates</a></p>
            <p><a href="#">Ratings</a></p>
            <p><a href="#">Shop Help</a></p>
            <p><a href="#">Contact Us</a></p>
          </div>

          <div class="little-title">
            <h3>sites</h3>
            <p><a href="#">DC</a></p>
            <p><a href="#">MAD Magazine</a></p>
            <p><a href="#">DC Kids</a></p>
            <p><a href="#">DC Universe</a></p>
            <p><a href="#">DC Power Visa</a></p>
          </div>
        </div>

        <div class="big-logo"></div>
      </div>
    </div>

    <div class="footer-bottom">
      <div class="container">
        <div class="call-to-action">
          <a href="#">sign-up now!</a>
        </div>

        <div class="follow">
          <h3>follow us</h3>
          <ul>
            <li>
              <a href="#"><img src="../assets/img/footer-facebook.png" alt="fb"></a>
            </li>
            <li>
              <a href="#"><img src="../assets/img/footer-twitter.png" alt="twitter"></a>
            </li>
            <li>
              <a href="#"><img src="../assets/img/footer-youtube.png" alt="yt"></a>
            </li>
            <li>
              <a href="#"><img src="../assets/img/footer-pinterest.png" alt="pinterest"></a>
            </li>
            <li>
              <a href="#"><img src="../assets/img/footer-periscope.png" alt="gps"></a>
            </li> 
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
   name: 'Footer'
}
</script>

<style lang="scss">
  @import "../assets/style/var.scss";
  @import '../assets/style/mixins.scss';

  .footer-top {
    height: 450px;
    overflow: hidden;
    background-position: center;
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover; 
    .container {
      @include flex-btw;
      .big-logo{
        width: 40%;
        height: 450px;
        background-image: url('../assets/img/dc-logo-bg.png');
        background-position: center;
        background-size: cover;
      } 
    }  
  }

  .related {
    display: flex;
    .little-title {
      h3 {
        color: #fff;
        @include titles;
        padding: 0 3rem 1rem 0;
      }
      &.listed {
        padding: 1rem 0;
      }
      p a {
        color: #959595;
        font-size: 16px;
        margin: 0 20px 7px 0;
        &:hover {
          color: $main-color;
        }
      }
    }
  }

  
  
  .footer-bottom {
    background-color: #303030;
    .container {
      height: 150px;
      @include flex-btw;
      .call-to-action a{
        color: #fff;
        text-transform: uppercase;
        font-size: 22px;
        border: 2px solid $main-color;
        padding: 1rem;
        &:hover {
          color: $main-color;
        }
      }
      .follow {
        @include flex-btw;
        h3 {
          @include titles;
          color: $main-color;
          padding-right: 1rem;  
        }
        ul {
          @include flex-btw;
          a {
          padding: 0 8px;  
          }
        }
        
      }  
    }
  }
</style>