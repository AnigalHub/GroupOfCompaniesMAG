<template>
    <div id="Directions">
        <b-container>
            <h2>Основные направления работы компании</h2>
            <b-row>
                <b-col>
                    <div>
                        <component :is="svgDim"/>
                        <DirectionsItems :items="Directions1"></DirectionsItems>
                    </div>
                </b-col>
                <b-col>
                    <div>
                        <component :is="svgMonitor"/>
                        <DirectionsItems :items="Directions2"></DirectionsItems>
                    </div>
                </b-col>
                <b-col>
                    <div>
                        <component :is="svgEl"/>
                        <DirectionsItems :items="Directions3"></DirectionsItems>
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
    import DirectionsItems from "@/components/mixins/DirectionsItems";
    export default {
        name: "Directions",
        components:{
            DirectionsItems
        },
        data(){
            return{
                Directions1:[
                    {text:"Оповещения населения (ГОиЧС)",},
                    {text:"Оповещения и управления эвакуацией (СОУЭ)",},
                    {text:"Пожарные сигнализации (СПС, АПС)",},
                    {text:"Проводное радиовещание (РСО, РАСЦО)",},
                ],
                Directions2:[
                    {text:"Каналы связи (оптические, электрические, беспроводные)",},
                    {text:"Видеонаблюдения (СОТ, Безопасный регион, Безопасный город)",},
                    {text:"Дератизационные системы (ОЗДС)",},
                    {text:"Охранные комплексы и различный мониторинг",},
                ],
                Directions3:[
                    {text:"Контроль учета электроэнергии (АСКУЭ)",},
                    {text:"Контроль и управления доступом (СКУД)",},
                    {text:"Управления и диспетчеризация инженерных систем (АСУД)",},
                    {text:"Электрические сети и установки (Бытовые и промышленные до 220КВ)",},
                ],
                svgMonitor: MonitoringSvg,
                svgDim: EvacuationSvg,
                svgEl:ElectricitySvg,
            }
        }
    }
</script>

<style scoped lang="scss">

</style>