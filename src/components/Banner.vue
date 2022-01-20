<template>
  <section>
      <div class="banner-content">
            <div class="sm-container">
                <div class="banner-text">
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
    color: white;
    height: 300px;
    background-image: url(../assets/img/slide-1.jpg);
    background-repeat: no-repeat;
    background-position: right;
    background-size: contain;
    position: relative;

    .banner-content{
        border-bottom: 300px solid $primary_color;
        border-left: 0px solid transparent;
        border-right: 100px solid transparent;
        height: 0;
        width: 57%;

        .sm-container{

            .banner-text{
                padding: 50px 0 150px 50px;

                h2{
                    font-size: 40px;
                    font-weight: bold;
                }
                
                p{
                    font-size: 18px;
                }
            }
        }

    }

    
}

</style>