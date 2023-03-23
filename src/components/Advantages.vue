<template>
    <div id="Advantages">
        <b-container>
            <b-row>
                <b-col>
                    <h2>Почему выбирают нас</h2>
                    <ul class="ul">
                        <li v-for="advantage in Advantages" class="text">{{advantage.text}}</li>
                    </ul>
                    <b-button @click="modalShow = !modalShow"><a>Посмотреть лицензию</a></b-button>
                </b-col>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
            </b-row>
            <b-modal v-model="modalShow" size="lg">
                <img :src="license1.src" :alt="license1.alt"/>
                <img :src="license2.src" :alt="license2.alt"/>
            </b-modal>
        </b-container>
    </div>
</template>

<script>
    import AdvantagesSvg from "./svg/AdvantagesSvg";
    export default {
        name: "Advantages",
        data(){
            return{
                modalShow: false,
                svg:AdvantagesSvg,
                license1:{
                    src:'./documents/license-1.png',
                    alt:'Лицензия'
                },
                license2:{
                    src:'./documents/license-2.png',
                    alt:'Лицензия'
                },
                Advantages:[
                    {text:"Безупречная репутация",},
                    {text:"Лучший технадзор на рынке",},
                    {text:"Выполнение всех работ точно в срок",},
                    {text:"Личная сдача результата работы контролирующим органам",},
                ],
            }
        },
    }
</script>

