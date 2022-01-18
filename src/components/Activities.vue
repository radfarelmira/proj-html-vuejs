<template>
    <section>
        <div class="container">
            <div class="row">
                <div class="col col-left">
                    <div class="col-image">
                        <img src="../assets/img/33.png" alt="image">
                    </div>
                    <div class="col-content">
                        <h4>Becaome an Instructor</h4>
                        <p>Teach what you love. Masterstudy gives you the tools to create a course.</p>
                        <a class="btn-general" href="#">start teaching</a>
                    </div>
                </div>
                <div class="col col-right">
                    <div class="col-image">
                        <img src="../assets/img/34.png" alt="image">
                    </div>
                    <div class="col-content">
                        <h4>Access For Business</h4>
                        <p>Get unlimited access to 2,500 of top courses for your team</p>
                        <a class="btn-general" href="#">doing business</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Activities',

}
</script>

<style scoped lang="scss">

section{
    padding: 50px 0;

    .container{

        .row{

            .col{
                margin-right: 10px;
                border: 1px solid lightgray;
                display: flex;
                align-items: center;
                padding: 70px 0;

                .col-image{
                    width: 40%;
                    padding:0 40px;
                    
                }

                .col-content{
                    width: 45%;

                    h4{
                        font-weight: bold;
                    }

                    p{
                        color: gray;
                        margin-bottom: 30px;
                    }
                }
            }

            .col-left{
                margin-left: 10px;
            }
            
            .col-right{
                margin-left: 10px;
            }
        }
    }
}

</style>