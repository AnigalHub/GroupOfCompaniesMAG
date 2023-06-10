<template>
    <div id="About">
        <b-container>
            <b-row>
                <b-col cols="3">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>О компании</h2>
                    <p>Группа {{short_name_company}} представляет собой многопрофильную группу компаний, специализирующихся на строительно-монтажных и
                        пусконаладочных работах систем.</p>
                    <p>На сегодняшний день в группе компаний работает свыше 2000 квалифицированных сотрудников разных специализаций.</p>
                    <p>В структуру группы {{short_name_company}} входят компании:</p>
                    <ul v-for="company in Companies" class="text">
                        <li>{{company.name}}{{company.text}}</li>
                    </ul>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import AboutSvg from "./newSvg/Main/AboutSvg";
    import information from '../../public/documents/information.json';

    export default {
        name: 'About',
        data(){
            return{
                svg:AboutSvg,
                short_name_company: information.short_name_company,
                Companies:information.Companies,
            }
        }
    }
</script>

<style scoped lang="scss">

</style>
