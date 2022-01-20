<template>
  <header>
      <!-- Header Top -->
      <div class="header-top">
        <div class="container">
            <div class="lang">
                <select name="" id="xyz">
                    <option value="en">English</option>
                    <option value="it">Italiano</option>
                    <option value="es">Spanol</option>
                </select>
            </div>
            <nav>
              <div class="menu">
                  <ul>
                      <li v-for="(link, index) in headerToplinksArray" :key="index">
                          <a :href="link.url">{{link.text}}</a>
                      </li>
                  </ul>
              </div>
              <div class="icons">
                 <ul>
                    <li v-for="(icon, index) in  headerTopIconsArray" :key="index">
                        <a :href="icon.url" target="_blank">
                            <i :class="icon.class"></i>
                        </a>
                    </li>
                 </ul>
              </div>
            </nav>
        </div>
      </div>
      <!-- Header Middel -->
      <div class="header-middel">
        <div class="container">
            <div class="logo">
                <img src="../assets/img/MasterStudy.svg" alt="Master Study Logo">
            </div>
            <div class="input-content">
                <a href="#">
                    <i class="fas fa-bars"></i>
                    category
                </a>
                
                <input type="text" placeholder="Search courses">
                <button type="button">
                    <i class="fas fa-search"></i>
                </button> 
            </div>
            
            <div class="colaboration">
                <a href="#">
                    <i class="fas fa-bullhorn"></i>
                    Become an instructor
                </a>

                <a href="#">
                    <i class="fas fa-briefcase"></i>
                    For Enterprise
                </a>
            </div>
            <div class="log-in">
                <a href="#">
                    <i class="far fa-user"></i>
                    Log in
                </a>

                <a class="btn-general" href="#">
                    sign up
                </a>

                <a class="bookmark" href="#">
                    <i class="far fa-bookmark"></i>
                </a>
            </div>
        </div>
      </div>
      <!-- Header Bottom -->
      <div class="header-bottom">
        <div class="container">
            <ul>
                <li v-for="(link, index) in headerBottomLinksArray" :key="index">
                    <a :href="link.url">
                        <i :class="link.class"></i>
                        {{link.text}}
                    </a>
                </li>
            </ul>
        </div>
      </div>
  </header>
</template>

<script>
export default {
    name: 'Header',
    props: {
        headerToplinksArray: Array,
        headerTopIconsArray: Array,
        headerBottomLinksArray: Array
    },
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

header{
    width: 100%;
    font-size: 14px;
    .header-top{
        border-bottom: 1px solid lightgray;
        padding: 15px 0;
        color: lightgray;

        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;

            .lang{

                select#xyz {
                    border:0px;
                    outline:0px;
                    color: lightgray;
                }

                select#xyz:hover {
                    color: #457992;
                }

            }

            nav {
                display: flex;
                justify-content: space-between;
                align-items: center;

                .menu{

                    ul{

                        li{
                            margin: 0 20px;

                            a{
                                text-transform: capitalize;
                            }
                        }
                    }
                }

                .icons{

                    ul{

                        li{
                            margin: 0 5px;
                            transition: transform .1s; 
                        }

                        li:hover{
                            transform: scale(1.2)
                        }
                    }
                }

            }
        }
    }

    .header-middel{
        color: gray;
        padding: 20px 0;
        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;

            img{
                min-width: 200px;
            }

            .input-content{
                display: flex;
                justify-content: space-between;
                align-items: center;
                flex-wrap: wrap;

                a{
                    margin-right: 15px;
                    text-transform: uppercase;
                }

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

            .colaboration{

                a{
                    margin-right: 10px;
                }
            }

            .log-in{
                a{
                    margin-right: 10px;  
                }

                .bookmark{
                    font-size: 20px;
                }
            }
        }
    }

    .header-bottom{
        background-color: $secondary_color;
        color: #ffffff;
        padding: 20px 0;

        ul{
            display: flex;
            justify-content: center;

            li{
                margin-right: 25px;
                text-transform: capitalize;

                i{
                    margin-right: 5px;
                }
            }
        }
    }
}
</style>