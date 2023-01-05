<template>
  <div id="Home">
      <b-container>
          <b-row>
              <b-col cols="5">
                  <h1>ОАО "Группа компаний МАГ"</h1>
                  <p>Создаем идеальное современное место для вашей комфотной и счастливой жизни</p>
                  <b-button><a href="#About">О нас</a></b-button>
                  <b-button><a href="#Services">Услуги</a></b-button>
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

</style>
