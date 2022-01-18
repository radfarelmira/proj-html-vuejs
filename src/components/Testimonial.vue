<template>
    <section>
        <!-- <img src="../assets/img/testimonial.jpg" alt=""> -->
        <div class="testimonial-content">
            <h4>Investing for Your Future</h4>
            <p>
                It is no exaggeration to say this MasterStudy experience was transformative/both professionally and personally. This workshp will long remain a high point of my life. Thanks again... i am feeling energized and eager to strat teaching my class next week. I can't wait to use all of my new teaching tools. I will absolutly recommend this workshop to other educators!
            </p>
            <div class="name">
                Linda Green
            </div>
            <div class="job-position">
                Product Manager, Apple Inc
            </div>

            <div id="triangle-right">
            </div>
        </div>
        
    </section>
</template>

<script>
export default {
    name: 'Testimonial'
}
</script>

<style scoped lang="scss">

section{
    padding: 50px 0;
    background-image: url(../assets/img/testimonial.jpg);
    background-size: 100%;
    background-repeat: no-repeat;

    .testimonial-content{
        width: 35%;
        margin-left: 300px;
        background-color: white;
        padding: 50px;
        position: relative;

        h4{
            font-weight: bold;
        }

        p{
          color: gray;
          margin: 30px 0;
        }

        .name{
            font-weight: bold;
        }

        .job-position{
            font-size: 12px;
            color: gray;
        }
    }

    .testimonial-content:after {
        content: " ";
        position: absolute;
        right: -15px;
        top: 180px;
        border-top: 15px solid transparent;
        border-right: none;
        border-left: 20px solid white;
        border-bottom: 15px solid transparent;
    }

}

</style>