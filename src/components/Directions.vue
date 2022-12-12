<template>
    <div id="Directions">
        <b-container>
            <h2>Основные направления компании:</h2>
            <div class="parent">
                <div class="text" v-for="list in List">
                    <ul v-if="!list.svg">
                        <li>{{list.text}}</li>
                    </ul>
                    <component v-if="!list.text" :is="list.svg"/>
                </div>
            </div>
        </b-container>
    </div>
</template>

<script>
    import AboutSvg from "@/components/svg/AboutSvg";

    export default {
        name: "Directions",
        data(){
            return{
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
    #Directions{
        padding: 0% 3% 4%;
        .parent {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            grid-template-rows: repeat(5, 1fr);
            div{
                border-radius: 12px;
                align-items: center;
                justify-content: center;
                svg{
                    width: 100%;
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
        ul {
            padding: 0 3% 2% 3%;
            margin-bottom: 1.5% !important;
            font-size: 1.2rem;
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
</style>