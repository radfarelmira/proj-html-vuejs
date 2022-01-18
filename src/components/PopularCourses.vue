<template>
    <section>
        <div class="container">
            <h2>Popular Courses</h2>
            <p>Discover our most popular courses for self learning</p>

            <div class="row row-cols-1 row-cols-md-6 g-4">
                <Card v-for="(cours, index) in popularCourses" :key="index" :detailes="cours" :class="currentActiveCourse === index? 'active-cours': 0 "/>
            </div>


            <div class="arrow-buttons">
                <span @click="showNextCours" class="next-arrow">
                    <i class="fas fa-angle-left"></i>
                </span>
                <span @click="showPrevCours" class="prev-arrow">
                    <i class="fas fa-angle-right"></i>
                </span>
            </div>
        </div>
    </section>
</template>

<script>
import Card from "./Card.vue";

export default {
    name: 'PopularCourses',
    components:{
        Card,
    },
    props: {
        allCoursesArray: Array,
    },
    data: function(){
        return{
            popularCourses: [],
            currentActiveCourse: 0,
        };
    },
    methods: {
        getPopularCourses: function (){
            this.popularCourses= [...this.allCoursesArray]

            this.popularCourses.splice(6)
        },
        showNextCours: function (){
            if( this.currentActiveCourse < this.popularCourses.length - 1){
                this.currentActiveCourse++;
            } else {
                this.currentActiveCourse = 0;
            }
        },
        showPrevCours: function (){
            if(this.currentActiveCourse > 0){
                this.currentActiveCourse--;
            } else{
                this.currentActiveCourse = this.popularCourses.length - 1;
            }
        }
    },
    created: function(){
        this.getPopularCourses()
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

        .row{
            margin: 20px 0 50px 0;
        }

        .arrow-buttons{

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