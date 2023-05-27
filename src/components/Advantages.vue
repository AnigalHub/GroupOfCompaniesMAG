<template>
    <div id="Advantages">
        <b-container>
            <b-row>
                <b-col>
                    <h2>Почему выбирают нас</h2>
                    <ul class="ul">
                        <li v-for="advantage in Advantages" class="text">{{advantage.text}}</li>
                    </ul>
                </b-col>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import AdvantagesSvg from "./newSvg/Main/AdvantagesSvg";
    export default {
        name: "Advantages",
        data(){
            return{
                svg:AdvantagesSvg,
                Advantages:[
                    {text:"Безупречная репутация",},
                    {text:"Лучший технадзор на рынке",},
                    {text:"Выполнение всех работ точно в срок",},
                    {text:"Личная сдача результата работы контролирующим органам",},
                    {text:'Все выполняемые работы и оказывающие услуги лицензированы',}
                ],
            }
        },
    }
</script>

<style scoped lang="scss">

</style>

