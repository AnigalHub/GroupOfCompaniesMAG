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
                <iframe :src="pdfSource" width="100%" height="100%"></iframe>
            </b-modal>
        </b-container>
    </div>
</template>

<script>
    import axios from 'axios';
    import AdvantagesSvg from "./svg/AdvantagesSvg";
    export default {
        name: "Advantages",
        data(){
            return{
                pdfSource:'',
                modalShow: false,
                svg:AdvantagesSvg,
                Advantages:[
                    {text:"Безупречная репутация",},
                    {text:"Лучший технадзор на рынке",},
                    {text:"Выполнение всех работ точно в срок",},
                    {text:"Личная сдача результата работы контролирующим органам",},
                ],
            }
        },
        created() {
            axios({
                url: '/mag/documents/license.pdf',
                method: 'GET',
                responseType: 'blob',
            }).then((response) => {
                const href = URL.createObjectURL(response.data);
                this.pdfSource = href
                return this.pdfSource;
            });
        },
    }
</script>

