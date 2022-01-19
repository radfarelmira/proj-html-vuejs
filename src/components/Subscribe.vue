<template>
    <section>
        <div class="sm-container">
            <div class="row">
                <div class="col col-left">
                    <h5>Subscribe our newsletter</h5>
                    <p>There are many variations of passages of Lorem Ipsum availabe, but the majority have suffered alteration in some form, by injected humour, or randommised words</p>
                </div>
                <div class="col col-right">
                    <h5>your e-mail address</h5>
                    <div class="input">
                        <input type="text" placeholder="Enter your E-mail">
                        <button type="button">
                            Subscribe
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

section{
    background-color: $primary_color;
    color: white;
    padding: 50px 0;

    .sm-container{

        .row{

            .col-left{

                h5{
                    font-weight: bold;
                }
            }

            .col-right{
                h5{
                    text-transform:uppercase;
                    font-size: 14px;
                }
                .input{

                    input{
                        border: none;
                        background: #f0f2f5;
                        width: 350px;
                        height: 35px;
                    }

                    ::placeholder{
                        padding-left: 10px;
                        font-size: 14px;
                        color: lightgray;
                    }

                    input:focus {
                        outline-color: lightgray;
                    }

                    button{ 
                        border: none;
                        outline: none;
                        background-color: #457992;
                        color: white;
                        height: 35px;
                        padding: 0 20px;
                    }

                    button:active{
                        background-color: #233e4b;
                    }
                }
            }

        }
    }
}

</style>