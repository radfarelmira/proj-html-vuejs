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
            <div class="input-group mb-3">
                <label for="category">category</label>
                <input type="text" class="form-control" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="button-addon2">
                <button class="btn btn-outline-secondary" type="button" id="button-addon2">Button</button>
            </div>
            <div class="membership">
                membership
            </div>
            <div class="log-in">
                log in
            </div>
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
        padding: 20px 0;
        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;

            .input-group{

                width: 600px;

                label{
                    margin-right: 10px;
                    text-transform: uppercase;
                }

                input{
                    background-color: #f0f2f5;
                    border-color: #f0f2f5;
                    box-shadow: none;
                }

                button{
                    background-color: #457992;
                    border-color: #457992;
                    color:white;
                }
            }
        }
    }

    .header-bottom{
        background-color: $secondary_color;
        color: #ffffff
    }
}
</style>