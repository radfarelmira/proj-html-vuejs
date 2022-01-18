<template>
  <section>
      <div class="sm-container">
            <div class="banner-content">
                <h2>Udemy Affiliaten Sales</h2>
                <p>Monetize your audience and attract new customers with Udemy!</p>
            </div>
            <div class="triangle">
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
    color: white;
    height: 300px;
    background-color: $primary_color;
    background-image: url(../assets/img/slide-1.jpg);
    background-repeat: no-repeat;
    background-position: right;
    background-size: contain;
    padding: 100px 0;
    position: relative;

    .sm-container{

        .banner-content{
            width: 50%;
            background-color: $primary_color;

            h2{
                font-size: 40px;
                font-weight: bold;
            }
        }

        .triangle{
            width: 0;
            height: 0;
            border-bottom: 300px solid $primary_color;
            border-right: 150px solid transparent;
            position: absolute;
            left: 684.5px;
            bottom: 0;
        }
    }

    
}

</style>