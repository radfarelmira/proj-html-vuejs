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
            Header middel
        </div>
      </div>
      <!-- Header Bottom -->
      <div class="header-bottom">
        <div class="container">
            Header bottom
        </div>
      </div>
  </header>
</template>

<script>
export default {
    name: 'Header',
    props: {
        headerToplinksArray: Array,
        headerTopIconsArray: Array
    },
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

header{

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
        // test
        background-color: honeydew;
    }

    .header-bottom{
        background-color: $secondary_color;
        color: #ffffff
    }
}
</style>