<template>
    <div id="Directions">
        <b-container>
            <h2>Основные направления работы компании:</h2>
            <b-row>
                <b-col>
                    <div class="wrapper">
                        <div class="text" v-for="list in List">
                            <ul v-if="!list.svg && list.text !== ''">
                                <li>{{list.text}}</li>
                            </ul>
                            <component  v-if="list.text === ''" :is="list.svg"/>
                        </div>
                    </div>
                </b-col>
                <b-col cols="3">
                    <component  :is="svg"/>
                </b-col>
                <b-col>
                    <div class="wrapper">
                        <div class="text" v-for="list in List2">
                            <ul v-if="!list.svg && list.text !== ''">
                                <li>{{list.text}}</li>
                            </ul>
                            <component  v-if="list.text === ''" :is="list.svg"/>
                        </div>
                    </div>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import DirectionsSvg from "@/components/svg/DirectionsSvg";

    export default {
        name: "Directions",
        data(){
            return{
                svg: DirectionsSvg,
                List:[
                    {text:"Оповещения населения (ГОиЧС)",},
                    {text:"Оповещения и управления эвакуацией (СОУЭ)",},
                    {text:"Пожарные сигнализации (СПС, АПС)",},
                    {text:"Проводного радиовещания (РСО, РАСЦО)",},
                    {text:"Каналов связи (оптические, электрические, беспроводные)",},
                    {text:"Видеонаблюдения (СОТ, Безопасный регион, Безопасный город)",},
                ],
                List2:[
                    {text:"Дератизационные системы (ОЗДС) ",},
                    {text:"Охранные комплексы и различный мониторинг",},
                    {text:"Контроля учета электроэнергии (АСКУЭ)",},
                    {text:"Контроля и управления доступом (СКУД)",},
                    {text:"Управления и диспетчеризация инженерных систем (АСУД)",},
                    {text:"Электрические сети и установки (Бытовые и промышленные до 220КВ)",},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">
    #Directions{
        .col{
            padding: 0 !important;
        }
        .col-3 {
            width: 20% !important;
        }
        ul {
            border-radius: 20px;
            margin-bottom: 1.5% !important;
            font-size: 1.2rem;
            list-style: none !important;
            background: linear-gradient(to left, rgba(160, 166, 216, 0.05), rgba(173, 199, 226, 0.1), rgba(160, 166, 216, 0.05));
        }
        li:before {
            padding-right:10px;

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