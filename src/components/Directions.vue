<template>
    <div id="Directions">
        <b-container>
            <h2>Основные направления работы компании</h2>
            <b-row>
                <b-col v-for="directions in Directions">
                    <div>
                        <component :is="directions.svg"/>
                        <div class="wrapper">
                            <div>
                                <ul>
                                    <li v-for="item in directions.values">{{item.text}}</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import MonitoringSvg from "./newSvg/Directions/MonitoringSvg";
    import EvacuationSvg from "./newSvg/Directions/EvacuationSvg";
    import ElectricitySvg from "./newSvg/Directions/ElectricitySvg";
    export default {
        name: "Directions",
        data(){
            return{
                Directions:[
                    {
                        svg:EvacuationSvg,
                        values:[
                            {text:"Оповещения населения (ГОиЧС)",},
                            {text:"Оповещения и управления эвакуацией (СОУЭ)",},
                            {text:"Пожарные сигнализации (СПС, АПС)",},
                            {text:"Проводное радиовещание (РСО, РАСЦО)",},
                        ]
                    },
                    {
                        svg:MonitoringSvg,
                        values:[
                            {text:"Каналы связи (оптические, электрические, беспроводные)",},
                            {text:"Видеонаблюдения (СОТ, Безопасный регион, Безопасный город)",},
                            {text:"Дератизационные системы (ОЗДС)",},
                            {text:"Охранные комплексы и различный мониторинг",},
                        ]
                    },
                    {
                        svg:ElectricitySvg,
                        values: [
                            {text:"Контроль учета электроэнергии (АСКУЭ)",},
                            {text:"Контроль и управления доступом (СКУД)",},
                            {text:"Управления и диспетчеризация инженерных систем (АСУД)",},
                            {text:"Электрические сети и установки (Бытовые и промышленные до 220КВ)",},
                        ]
                    }

                ],
            }
        }
    }
</script>

<style scoped lang="scss">

</style>