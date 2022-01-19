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
                    <div class="input-group">
                    <input type="text" class="form-control" placeholder="Enter your E-mail" aria-label="Recipient's username" aria-describedby="button-addon2">
                    <button class="btn btn-outline-secondary" type="button" id="button-addon2">
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
                .input-group{

                    .btn{
                        background-color: #457992;
                        border-color: #457992;
                        color: white;
                    }

                    ::placeholder{
                        font-size: 14px;
                        color: lightgray;
                    }
                }
            }

        }
    }
}

</style>