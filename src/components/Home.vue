<template>
  <div id="Home">
      <b-container>
          <b-row>
              <b-col cols="5">
                  <h1>{{name}}</h1>
                  <h2>Надежно!   Практично!  Современно!</h2>
                  <p>Комплексные услуги по проектированию и строительству многоквартирных домов и иных объектов недвижимости на территории РФ.</p>
                  <div class="buttonGroup">
                      <b-button><a href="#About">О нас</a></b-button>
                      <b-button><a href="#Services">Услуги</a></b-button>
                  </div>
              </b-col>
              <b-col>
                  <component :is="svg"/>
              </b-col>
          </b-row>
      </b-container>
  </div>
</template>

<script>
    import HomeSvg from "./newSvg/Main/HomeSvg";
    import information from '../../public/documents/information.json';
    export default {
      name: 'Home',
      data(){
        return{
          svg:HomeSvg,
          name: information.name_company
        }
      }
    }
</script>

<style scoped lang="scss">

</style>
