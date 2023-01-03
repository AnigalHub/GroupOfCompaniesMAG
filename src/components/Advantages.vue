<template>
    <div id="Advantages">
        <b-container>
            <b-row>
                <b-col>
                    <h2>Почему выбирают нас</h2>
                    <ul class="ul">
                        <li v-for="list in List" class="text">{{list.text}}</li>
                    </ul>
                    <b-button><a>Посмотреть лицензию</a></b-button>
                </b-col>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import AdvantagesSvg from "./svg/AdvantagesSvg";
    export default {
        name: "Advantages",
        data(){
            return{
                svg:AdvantagesSvg,
                List:[
                    {text:"Безупречная репутация",},
                    {text:"Лучший технадзор на рынке",},
                    {text:"Выполнение всех работ точно в срок",},
                    {text:"Личная сдача результата работы контролирующим органам",},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">

</style>
