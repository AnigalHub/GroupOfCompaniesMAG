<template>
    <div id="Employees">
        <b-container>
            <b-row>
                <b-col cols="4">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>Сотрудники<span>, которым доверяют</span></h2>
                    <ul>
                        <li class="text" v-for="employee in Employees">
                           <span>{{employee.name}}</span>
                            <br/>
                            {{employee.text}}
                        </li>
                    </ul>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import AboutSvg from "./svg/EmployeesSvg";
    export default {
        name: "Employees",
        data() {
            return {
                svg: AboutSvg,
                Employees:[
                    {name:"Работники с высшим образованием",text:"У нас работают сотрудники только с высшим образованием"},
                    {name:"Аттестация каждые полгода",text:"Каждые полгода все сотрудники проходят подготовку и аттестацию в учебном центре"},
                    {name:"Только славяне",text:"В компании работают только славяне. Каждый из них дорожит своей репутацией и имеет профессиональную подготовку"},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">

</style>