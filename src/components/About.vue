<template>
    <div id="About">
        <b-container>
            <b-row>
                <b-col cols="4">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>О нас</h2>
                    <p><b>{{name}}</b> занимается строительно-монтажными и пуско-наладочными работами систем.</p>
                    <p><u>Наша компания состоит из:</u></p>
                    <ul>
                        <li v-for="company in Companies" class="text"><b>{{company.name}}</b>{{company.text}}</li>
                    </ul>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import AboutSvg from "./svg/AboutSvg";
    import information from '../../public/documents/information.json';

    export default {
        name: 'About',
        data(){
            return{
                svg:AboutSvg,
                name: information.name_company,
                Companies:information.Companies,
            }
        }
    }
</script>

<style scoped lang="scss">

</style>
