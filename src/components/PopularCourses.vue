<template>
    <section>
        <div class="container">
            <h2>Popular Courses</h2>
            <p>Discover our most popular courses for self learning</p>

            <div class="row row-cols-1 row-cols-md-6 g-4">
                <Card v-for="(cours, index) in recentCoursesArray" :key="index" :detailes="cours"/>
            </div>


            <div class="arrow-buttons">
                <span class="next-arrow">
                    <i class="fas fa-angle-left"></i>
                </span>
                <span class="prev-arrow">
                    <i class="fas fa-angle-right"></i>
                </span>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'PopularCourses',
    props: {
        popularCoursesArray: Array,
    }
}
</script>

<style scoped lang="scss">

section{
    padding: 50px 0;
    background-color: #f0f4fa;

    .container{
        text-align: center;
        h2{
            font-size: 40px;
            font-weight: bold;
        }

        p{
            color: gray;
        }


        .arrow-buttons{
            margin-top: 50px;

            .next-arrow,
            .prev-arrow
            {
                background-color: white;
                color: lightgray;
                border: 1px solid lightgray;
                padding: 8px 12px;
            }

            .next-arrow:hover,
            .prev-arrow:hover {
                background-color: #457992;
                color: white;
            }
        }
    }
}

</style>