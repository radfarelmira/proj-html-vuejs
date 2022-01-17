<template>
  <section>
      <div class="row">
        <div class="parallelogram">
        </div>
        <div class="sm-container">
            <div class="banner-content">
                <h2>banner</h2>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aut eum deserunt unde dolore distinctio dolores odio id debitis, corrupti architecto repellendus facilis molestias. Quo, dolore id labore saepe aspernatur inventore?</p>
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
        
        .banner-content{
            z-index: 1;
            width: 50%;
        }
    }
}

</style>