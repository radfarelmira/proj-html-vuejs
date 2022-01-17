<template>
  <header>
      <!-- Header Top -->
      <div class="header-top">
        <div class="container">
            <div class="lang">
                <select name="" id="">
                    <option value="english">English</option>
                    <option value="italian">Italian</option>
                    <option value="spanish">Spanish</option>
                </select>
            </div>
            <nav>
              <div class="menu">
                  Header top menu
              </div>
              <div class="icons">
                  icons
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
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

header{
    // test
    background-color: antiquewhite;

    .header-top{
        border-bottom: 1px solid lightgray;
        padding: 15px 0;
        color: lightgray;

        .container{
            display: flex;
            justify-content: space-between;
            text-align: center;

            nav {
                display: flex;
                justify-content: space-between;

                .lang{

                    select {
                    border: 0px;
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