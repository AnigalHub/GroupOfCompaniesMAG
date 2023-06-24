<template>
    <div id="Employees">
        <b-container>
            <h2>Сотрудники, которым доверяют</h2>
            <div class="flex-container">
                <div class="text employee" v-for="(employee, index) in Employees" :key="index">
                    <span>{{employee.name}}</span>
                    <b-row>
                        <b-col>
                            {{employee.text}}
                        </b-col>
                        <b-col cols="2">
                            <component :is="employee.svg"/>
                        </b-col>
                    </b-row>
                </div>
                <div class="svgEmployees">
                    <component :is="svg"/>
                </div>
            </div>
        </b-container>
    </div>
</template>

<script>
    import AboutSvg from "./newSvg/Main/EmployeesSvg";
    import SlavsSvg from "./newSvg/Employees/SlavsSvg";
    import CertificationSvg from "./newSvg/Employees/CertificationSvg";
    import EducationSvg from "./newSvg/Employees/EducationSvg";
    export default {
        name: "Employees",
        data() {
            return {
                svg: AboutSvg,
                Employees:[
                    {svg:EducationSvg, name:"Работники с высшим образованием",text:"У нас работают сотрудники только с высшим образованием"},
                    {svg:CertificationSvg, name:"Аттестация каждые полгода",text:"Каждые полгода все сотрудники проходят подготовку и аттестацию в учебном центре"},
                    {svg:SlavsSvg, name:"Только славяне",text:"В компании работают только славяне. Каждый из них дорожит своей репутацией и имеет профессиональную подготовку"},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">

</style>