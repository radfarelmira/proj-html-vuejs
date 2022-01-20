<template>
  <footer>
    <!-- Footer top -->
      <div class="footer-top">
        <div class="sm-container">
          <div class="row">
            <!-- Cols -->
            <div class="col about">
              <h5>about</h5>
              <p>Voluptas magnam natus ipsa asperiores quisquam, mollitia excepturi, atque dolore facere optio incidunt iusto doloremque consequatur cupiditate nulla aliquam ea qui totam.</p>
            </div>
            <div class="col contact">
              <h5>contact</h5>
              <p>USA, Callifornia 20, First Avenue,<br> Callifornia</p>
              <p>Tel: +1 212 458 300 32 <br> Fax: +1 212 375 24 14</p>
              <div class="text-gray">info@masterstudy.com</div>
            </div>
            <div class="col social">
              <h5>social network</h5>
              <ul>
                <li v-for="(icon, index) in footerTopIconsArray" :key="index">
                  <a :href="icon.href" :style="{'background-color': icon.bgColor}" target="_blank">
                    <i :class="icon.class"></i>
                  </a>
                </li>
              </ul>
            </div>
            <div class="col udemy">
              <img src="../assets/img/top-udemy.jpg" alt="udemy">
            </div>
          </div>
        </div>   
      </div>
    <!-- Footer bottom -->
      <div class="footer-bottom">
        <div class="sm-container">
          <img src="../assets/img/footer-logo.png" alt="MS logo">
          <span>Copyright &copy; 2020. <span class="text-underline">MasterStudy</span>Theme by<span class="text-underline">StylemixThemes</span> </span>
        </div>
      </div>
  </footer>
</template>

<script>
export default {
    name: 'Footer',
    props:{
      footerTopIconsArray: Array,
    }
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

footer{
  background-color: $secondary_color;
  color: white;
  font-size: 12px;

  h5{
    text-transform: uppercase;
    font-size: 14px;
    font-weight: bold;
    margin-bottom: 20px;
  }

  .footer-top{
    border-bottom: 1px solid gray;
    padding: 50px 0;

    .contact{

      p{
        font-size: 14px;
      }

      .text-gray{
        color: gray;
      }
    }

    .social{
      font-size: 18px;
      ul{
        display: flex;
        flex-wrap: wrap;

        li{
          margin: 0 10px 10px 0;
          transition: transform .1s;  

          a{
            padding: 10px 15px;
            background-color: #d4ebb3;
            border-radius: 50px;
          }
        }

        li:hover{
          transform: scale(1.1)
        }
      }
    }

    .udemy{
    
    }

    
  }

  .footer-bottom{
    padding: 20px 0;

    .sm-container{

      img{
        width: 20px;
        margin-right: 10px;
      }

      .text-underline{
        text-decoration: underline;
      }
    }
  }
}
</style>