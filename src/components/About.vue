<template>
    <div id="About">
        <b-container>
            <b-row>
                <b-col cols="4">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>О нас</h2>
                    <p><b>ОАО "Группа компаний МАГ"</b> занимается строительно-монтажными и пуско-наладочными работами систем.</p>
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
    export default {
        name: 'About',
        data(){
            return{
                svg:AboutSvg,
                Companies:[
                    {name:"ООО \"МРС\"",text:"- оператор связи и проектирование;"},
                    {name:"ООО \"Аваконт\"",text:"- строительно-монтажные работы;"},
                    {name:"ООО \"Гостехносервис\"",text:"- локальные и международные поставки."},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">

</style>
