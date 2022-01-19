<template>
    <section>
        <div class="container">
           <h2>Recent Courses</h2>
           <nav>
               <ul>
                   <li  v-for="(cours, index) in recentCoursesLinksArray" :key="index" >
                       <a @click="getActivelink(index)" :class="{'active-link' : index === activeLink}" href="#" >
                           {{cours}}
                        </a>
                   </li>
               </ul>
            </nav> 

            <div class="row row-cols-1 row-cols-md-6 g-4">
                <Card v-for="(cours, index) in recentCoursesArray" :key="index" :detailes="cours"/>
            </div>

            <a class="btn-general" href="#">show all</a>

            <div class="side-bar-icons">
                <ul>
                    <li>
                        <a href="#">
                            <i class="fas fa-tv"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <i class="fab fa-centos"></i>
                        </a>
                        
                    </li>
                    <li>
                        <a href="#">
                            <i class="fas fa-wrench"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <i class="fas fa-shopping-cart"></i>
                        </a>  
                    </li>
                    <li>
                        <a href="#">
                            <i class="fas fa-mobile-alt"></i>
                        </a> 
                    </li>
                </ul>
            </div>
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
    },
    data: function (){
        return{
            activeLink: 0,
        };
    },
    methods: {
        getActivelink: function(index){
            this.activeLink = index;
        },
    }
}
</script>

<style scoped lang="scss">

section{
    padding: 70px 0;
    text-align: center;
    position: relative;

    .container{

        h2{
            font-size: 40px;
            font-weight: bold;
        }

        nav{

            ul{
                margin-top: 30px;

                li{
                    margin-right: 20px;
                    text-transform: capitalize;

                }
            }
        }

        .row{
        margin: 30px 0 50px 0;
        }

        .side-bar-icons{
            width: 50px;
            color: gray;
            padding: 15px 0;
            box-shadow: 0 4px 8px 0 rgba(85, 84, 84, 0.2), 0 6px 20px 0 rgba(95, 95, 95, 0.19);
            position: absolute;
            right: 0;
            bottom: 70px;
            ul{
                display: flex;
                flex-direction: column;

                li{
                    margin: 5px 0;
                }
            }
        }
    }

    
}
</style>