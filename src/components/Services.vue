<template>
    <div id="Services">
        <b-container>
            <b-row>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>Мы предоставляем услуги</h2>
                    <ul>
                        <li v-for="(service, index) in Services" :key="index" class="text">{{service.text}}</li>
                    </ul>
                    <b-button><a href="./documents/Цены на виды работ.xlsx" download>Узнать цены на виды работ</a></b-button>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import ServicesSvg from "./newSvg/Main/ServicesSvg"
    export default {
        name: "Services",
        data(){
            return{
                svg:ServicesSvg,
                Services:[
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
