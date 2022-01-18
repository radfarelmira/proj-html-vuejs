<template>
    <section>
        <div class="container">
            <h3>
                Popular Development Courses
            </h3>

            <div class="row row-cols-1 row-cols-md-6 g-4">
                <Card v-for="(cours, index) in developmentCoursesArray" :key="index" :detailes="cours"/>
            </div>
        </div>
    </section>
</template>

<script>
import Card from "./Card.vue";

export default {
    name: 'DevelopmentCourses',
    components: {
        Card,
    },
    props:{
        developmentCoursesArray: Array,
    }
}
</script>

<style scoped lang="scss">

section{
    padding: 60px 0;

    .container{
        h3{
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 30px;
        }
    }
}

</style>