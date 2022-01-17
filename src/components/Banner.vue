<template>
  <section>
      <div class="row">
        <div class="parallelogram">
        </div>
        <div class="sm-container">
            <div class="banner-content">
                <h2>Udemy Affiliaten Sales</h2>
                <p>Monetize your audience and attract new customers with Udemy!</p>
            </div>
        </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'Banner',
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

section{
    margin-top: 20px;
    background-color:$primary_color ;
    color: white;

    .row{
        height: 300px;
        background-color: $primary_color;
        background-image: url(../assets/img/slide-1.jpg);
        background-repeat: no-repeat;
        background-position: right;
        background-size: contain;
        position: relative;
        

        .parallelogram{
            width: 150px;
            height: 300px;
            transform: skew(20deg);
            background: $primary_color;
            position: absolute;
            top: 0;
            left:650px;
        }
        

        .sm-container{
            z-index: 1;

            .banner-content{
            width: 50%;
            z-index: 1;

            h2{
                font-size: 40px;
                font-weight: bold;
            }
        }
        } 
    }
}

</style>