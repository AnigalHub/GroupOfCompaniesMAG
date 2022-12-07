<template>
    <div id="Employees">
        <b-container>
            <b-row>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>Сотрудники<span>, которым доверяют</span></h2>
                    <ul v-for="list in List" class="ul">
                        <li class="text">
                           <span>{{list.name}}</span>
                            <br/>
                            {{list.text}}
                        </li>
                    </ul>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import AboutSvg from "./svg/AboutSvg";
    export default {
        name: "Employees",
        data() {
            return {
                svg: AboutSvg,
                List:[
                    {name:"Работники с высшим образованием",text:"У нас работают сотрудники только с высшим образованием"},
                    {name:"Аттестация каждые полгода",text:"Каждые полгода все сотрудники проходят подготовку и аттестацию в учебном центре"},
                    {name:"Только славяне",text:"В компании работают только славяне. Каждый из них дорожит своей репутацией и имеет профессиональную подготовку"},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">
    #Employees{
        padding: 0 3% 4%;
        .ul {
            padding:0;
            list-style: none;
        }
        .ul li:before {
            padding-right:10px;
            font-size: 2rem;
            font-weight: bold;
            color: #77AEDB;
            content: "\2606";
            transition-duration: 0.5s;
        }
        .ul li:hover:before {
            color: #337AB7;
            content: "\2605";
        }
        h2 span{
            text-shadow: none;
            text-transform: lowercase;
        }
        li span{
            font-weight: 600;
        }
    }
</style>