<template>
  <div id="Home">
      <b-container>
          <b-row>
              <b-col cols="5">
                  <h1>ОАО "Группа компаний МАГ"</h1>
                  <p>
                      Создаем идеальное современное место для вашей комфотной и счастливой жизни
                  </p>
                      <b-button><a href="#About">О нас</a></b-button>
                      <b-button><a  href="#Services">Услуги</a></b-button>
              </b-col>
              <b-col>
                  <component :is="svg"/>
              </b-col>
          </b-row>
      </b-container>
  </div>
</template>

<script>
    import HomeSvg from "./svg/HomeSvg";
    export default {
      name: 'Home',
      data(){
        return{
          svg:HomeSvg,
        }
      }
    }
</script>

<style scoped lang="scss">
    #Home{
        padding: 4% 3% 4%;
        h1{
            margin-top: 4%;
            font-size: 3.5rem;
            line-height: 4rem;
            width: 110%;
            font-weight: 600;
        }
        p{
            margin: 4% 0;
            font-size: 1.35rem;
            line-height: 2.25rem;
        }
        button{
            width: 48%;
            margin: 3% 1.5%;
            padding: 2%;
            font-size: 1.5rem;
            border-radius: 30px;
            border: none;
            background: linear-gradient(to left, #b7dfe9,#adc7e2, #a0a6d8);
            &:last-child{
                margin-top: 2%;
            }
            a{
                color:white;
                text-decoration: none;
            }
        }
        svg{
            margin-top: 2%;
            width: 95%;
        }
    }
</style>
