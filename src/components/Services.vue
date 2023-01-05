<template>
    <div id="Services">
        <b-container>
            <b-row>
                <b-col>
                    <h2>Мы предоставляем услуги:</h2>
                    <ul>
                        <li v-for="list in List" class="text">{{list.text}}</li>
                    </ul>
                    <b-button><a>Узнать цены на виды работ</a></b-button>
                </b-col>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import ServicesSvg from "./svg/ServicesSvg"
    export default {
        name: "Services",
        data(){
            return{
                svg:ServicesSvg,
                List:[
                    {text:"Проектирование",},
                    {text:"Согласование проекта",},
                    {text:"Выполнение строительно-монтажных работ",},
                    {text:"Сдача объекта технадзору заказчика и контролирующим органам",},
                    {text:"Подготовка исполнительной документации",},
                ],
            }
        }
    }
</script>

<style scoped lang="scss">

</style>
