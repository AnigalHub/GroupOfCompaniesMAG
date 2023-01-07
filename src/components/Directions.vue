<template>
    <div id="Directions">
        <b-container>
            <h2>Основные направления работы компании:</h2>
            <b-row>
                <b-col>
                    <DirectionsItems :items="Directions1"></DirectionsItems>
                </b-col>
                <b-col cols="3">
                    <component  :is="svg"/>
                </b-col>
                <b-col>
                    <DirectionsItems :items="Directions2"></DirectionsItems>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import DirectionsSvg from "@/components/svg/DirectionsSvg";
    import DirectionsItems from "@/components/mixins/DirectionsItems";
    export default {
        name: "Directions",
        components:{
            DirectionsItems
        },
        data(){
            return{
                svg: DirectionsSvg,
                Directions1:[
                    {text:"Оповещения населения (ГОиЧС)",},
                    {text:"Оповещения и управления эвакуацией (СОУЭ)",},
                    {text:"Пожарные сигнализации (СПС, АПС)",},
                    {text:"Проводного радиовещания (РСО, РАСЦО)",},
                    {text:"Каналов связи (оптические, электрические, беспроводные)",},
                    {text:"Видеонаблюдения (СОТ, Безопасный регион, Безопасный город)",},
                ],
                Directions2:[
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