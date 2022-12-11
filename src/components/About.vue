<template>
    <div id="About">
        <b-container>
            <b-row>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>О нас</h2>
                    <p><b>ОАО "Группа компаний МАГ"</b> занимается строительно-монтажными и пуско-наладочными работами систем.</p>
                    <p><u>Наша компания состоит из:</u></p>
                    <ul>
                        <li><b>ООО "МРС"</b> - оператор связи и проектирование;</li>
                        <li><b>ООО "Аваконт"</b> - строительно-монтажные работы;</li>
                        <li><b>ООО "Гостехносервис"</b> - локальные и международные поставки.</li>
                    </ul>
                </b-col>
            </b-row>
            <h3>Основные направления компании:</h3>
            <div class="parent">
                <div class="text" v-for="list in List">
                    {{list.text}}
                    <component v-if="!list.text" :is="list.svg"/>
                </div>
            </div>
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
                List:[
                    {text:"Оповещения населения (ГОиЧС)",},
                    {text:"Дератизационные системы (ОЗДС) ",},
                    {text:"Пожарные сигнализации (СПС, АПС)",},
                    {text:"Контроля и управления доступом (СКУД)",},
                    {svg:AboutSvg},
                    {text:"Контроля учета электроэнергии (АСКУЭ)",},
                    {text:"Охранные комплексы и различный мониторинг",},
                    {text:"Проводного радиовещания (РСО, РАСЦО)",},
                    {svg:AboutSvg},
                    {text:"Оповещения и управления эвакуацией (СОУЭ)",},
                    {text:"Каналов связи (оптические, электрические, беспроводные)",},
                    {text:"Управления и диспетчеризация инженерных систем (АСУД)",},
                    {text:"Видеонаблюдения (СОТ, Безопасный регион, Безопасный город)",},
                    {text:"Электрические сети и установки (Бытовые и промышленные до 220КВ)",},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">
    .parent {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-template-rows: repeat(5, 1fr);
        div{
            padding: 2%;
            margin: 1%;
            border-radius: 12px;
            align-items: center;
            justify-content: center;
            svg{
                width: 30px !important;
                height: 30px !important;
            }
            &:first-child{
                grid-area: 1 / 1 / 2 / 2;
            }
            &:nth-child(2){
                grid-area: 1 / 2 / 2 / 3;
            }
            &:nth-child(3){
                grid-area: 1 / 3 / 2 / 4;
            }
            &:nth-child(4){
                grid-area: 2 / 1 / 3 / 2;
            }
            &:nth-child(5){
                grid-area: 2 / 2 / 3 / 4;
            }
            &:nth-child(6){
                grid-area: 3 / 1 / 4 / 2;
            }
            &:nth-child(7){
                grid-area: 3 / 2 / 4 / 3;
            }
            &:nth-child(8){
                grid-area: 3 / 3 / 4 / 4;
            }
            &:nth-child(9){
                grid-area: 4 / 1 / 5 / 2;
            }
            &:nth-child(10){
                grid-area: 4 / 2 / 5 / 3;
            }
            &:nth-child(11){
                grid-area: 4 / 3 / 5 / 4;
            }
            &:nth-child(12){
                grid-area: 5 / 1 / 6 / 2;
            }
            &:nth-child(13){
                grid-area: 5 / 2 / 6 / 3;
            }
            &:nth-child(14){
                grid-area: 5 / 3 / 6 / 4;
            }
        }
    }

    #About{

        padding: 4% 3% 4%;
        h2{
            margin-top: 7%;
        }
        .ul {
            padding:0;
            //list-style: none;
            margin-bottom: .5rem !important;
            font-size: 1.2rem;
        }
        .col{
            ul {
                list-style: none !important;
            }
            li:before {
                padding-right:10px;
                margin-left: -3%;
                font-size: 2rem;
                color: #77AEDB;
                content: "\2727";
            }
            li:hover:before {
                color: #337AB7;
                content: "\2726";
            }
        }
        svg{
            width: 100%;
            margin-bottom: 3%;
        }
    }
</style>
