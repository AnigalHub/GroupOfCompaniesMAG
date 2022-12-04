<template>
    <div id="Contacts">
        <b-container>
            <b-row>
                <b-col>
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>Наши контакты:</h2>
                    <p>
                        Свяжитесь с нами и мы ответим на любой ваш вопрос:
                    </p>
                    <div class="text">
                        <div class="nameContact">
                            <b-row>
                                <b-col cols="1">
                                    <component :is="call"/>
                                </b-col>
                                <b-col>
                                    <div class="contacts">
                                        <span>Телефон:</span>
                                        <br/>
                                        <a>+7 (968) - 824 -80-96</a>
                                    </div>

                                </b-col>
                            </b-row>
                        </div>
                        <div class="nameContact">
                            <b-row>
                                <b-col cols="1">
                                    <component :is="mail"/>
                                </b-col>
                                <b-col>
                                    <div class="contacts">
                                        <span>Почта:</span>
                                        <br/>
                                        <a>mag@mail.ru</a>
                                    </div>

                                </b-col>
                            </b-row>
                        </div>
                        <div class="nameContact">
                            <b-row>
                                <b-col cols="1">
                                    <component :is="location"/>
                                </b-col>
                                <b-col>
                                    <div class="contacts">
                                        <span>Адрес:</span>
                                        <br/>
                                        <a>Новорязанское шоссе, дом 6, подъезд 9-10, этаж 2.</a>
                                    </div>

                                </b-col>
                            </b-row>
                        </div>
                    </div>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>

<script>
    import AboutSvg from "./svg/AboutSvg";
    import CallSvg from "./svg_contacts/call";
    import MailSvg from "./svg_contacts/mail";
    import LocationSvg from "./svg_contacts/location";
    export default {
        name: "Contacts",
        data() {
            return {
                svg: AboutSvg,
                call:CallSvg,
                mail:MailSvg,
                location:LocationSvg
            }
        }
    }
</script>

<style scoped lang="scss">
    #Contacts{
        padding: 4% 3% 4%;
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


    }
</style>