<template>
    <section>
        <div class="container">
           <h2>Recent Courses</h2>
           <nav>
               <ul>
                   <li v-for="(cours, index) in recentCoursesLinksArray" :key="index" >
                       <a :class="index === 0? 'active': 0" href="#">{{cours}}</a>
                   </li>
               </ul>
            </nav> 

            <div class="row row-cols-1 row-cols-md-6 g-4">
                <Card v-for="(cours, index) in recentCoursesArray" :key="index" :detailes="cours"/>
            </div>

            <a class="btn-general" href="#">show all</a>
        </div>
    </section>
</template>

<script>
import Card from "./Card.vue";

export default {
    name: 'RecentCourses',
    components: {
        Card,
    },
    props: {
        recentCoursesLinksArray: Array,
        recentCoursesArray: Array,
    }
}
</script>

<style scoped lang="scss">

section{
    padding: 70px 0;
    text-align: center;

    .container{

        h2{
            font-size: 40px;
            font-weight: bold;
        }

        nav{

            ul{
                margin-top: 40px;

                li{
                    margin-right: 20px;
                    text-transform: capitalize;

                }
            }
        }

        .row{
        margin: 50px 0;
        }
    }

    
}
</style>