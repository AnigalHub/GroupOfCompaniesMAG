<template>
    <div id="Contacts">
        <b-container>
            <b-row>
                <b-col cols="5">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>Наши контакты:</h2>
                    <p>Свяжитесь с нами и мы ответим на любой ваш вопрос:</p>
                    <div class="nameContact text" v-for="value in Contacts">
                        <b-row>
                            <b-col cols="1">
                                <component :is="value.svg"/>
                            </b-col>
                            <b-col>
                                <div class="contacts">
                                    <span>{{value.name}}</span>
                                    <br/>
                                    <a>{{value.description}}</a>
                                </div>
                            </b-col>
                        </b-row>
                    </div>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import ContactsSvg from "./svg/ContactsSvg";
    import CallSvg from "./svg_contacts/call";
    import MailSvg from "./svg_contacts/mail";
    import LocationSvg from "./svg_contacts/location";
    export default {
        name: "Contacts",
        data() {
            return {
                svg: ContactsSvg,
                Contacts: [
                    {
                        name:'Телефон:',
                        description:'+7 (968) - 824 -80-96',
                        svg:CallSvg,
                    },
                    {
                        name:'Почта:',
                        description:'mag@mail.ru',
                        svg:MailSvg,
                    },
                    {
                        name:'Адрес:',
                        description:'Новорязанское шоссе, дом 6, подъезд 9-10, этаж 2.',
                        svg:LocationSvg,
                    },
                ],
            }
        }
    }
</script>

<style scoped lang="scss">
    #Contacts{
        .contacts{
            padding-left: 2%;
        }
        span{
            text-decoration: underline;
        }
        a{
            margin-top: 5%;
            text-decoration: none;
        }
        .nameContact{
            padding: 1.5%;
            border-radius: 20px;
            svg{
                width: 2.5rem;
                margin-top: 40%;
                margin-right: 3%;
            }
        }
        svg{
            width: 95%;
        }
    }
</style>