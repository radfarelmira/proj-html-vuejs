<template>
  <header>
      <!-- Header Top -->
      <div class="header-top">
        <div class="container">
            <div class="lang">
                <span>English</span>
                <i class="fas fa-chevron-down"></i>
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
            <div class="input">
                <a href="#">
                    <i class="fas fa-bars"></i>
                    category
                </a>

                <div class="input-group">
                    <input type="text" class="form-control" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="button-addon2">
                    <button class="btn btn-outline-secondary" type="button" id="button-addon2">
                        <i class="fas fa-search"></i>
                    </button>
                </div>
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

                i{
                    margin-left: 5px;
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

            .input{
                display: flex;
                align-items: center;

                a{
                    margin-right: 15px;
                    text-transform: uppercase;
                }

                .input-group{
                    width: 400px;
                    input{
                        background-color: #f0f2f5;
                        border-color: #f0f2f5;
                    }

                    button{
                        background-color: #457992;
                        border-color: #457992;
                        color:white;
                    }
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