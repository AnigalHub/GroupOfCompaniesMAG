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
                    {text:"Дератизационные системы (ОЗДС)",},
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

</style>