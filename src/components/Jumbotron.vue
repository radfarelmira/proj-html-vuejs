<template>
    <section>
        <div class="sm-container">
            <div class="jumbotron-content">
                <h2>Limitless learning, more possibilities</h2>
                <p>Online courses open the opportunity for learning to almost anyone, regardless of thier scheduling commitments.</p>
                <a class="btn-general" href="#">read more</a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Jumbotron',
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

section{
    padding: 75px 0;
    background-image: url(../assets/img/bg.png);
    background-size: cover;

    .sm-container{

        .jumbotron-content{
            width: 50%;

            h2{
                font-size: 40px;
                font-weight: bold;
            }

            p{
                margin: 20px 0;
            }

            .btn-general{
                margin-top: 30px;
            }
        }
    }

}

</style>