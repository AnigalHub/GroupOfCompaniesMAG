<template>
    <div id="Contacts">
        <b-container>
            <b-row>
                <b-col cols="4">
                    <component :is="svg"/>
                </b-col>
                <b-col>
                    <h2>Контактная информация</h2>
                    <p>Свяжитесь с нами любым удобным для вас способом.<br/>
                     Мы проконсультируем вас по нашим услугам, подберем мастеров, согласуем удобное для вас
                        время для проведения работ, и ответим на любой ваш вопрос.
                    </p>
                    <div class="nameContact text" v-for="value in Contacts">
                        <a :href="value.href" :target="value.target">
                            <b-row>
                                <b-col cols="1">
                                    <component :is="value.svg"/>
                                </b-col>
                                <b-col>
                                    <div class="contacts">
                                        <span>{{value.name}}</span>
                                        <br/>{{value.description}}
                                    </div>
                                </b-col>
                            </b-row>
                        </a>
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
                        description:'+7(968)-824-80-96',
                        svg:CallSvg,
                        href:'tel:' + '+7 968 824-80-96',
                        target:'_self',
                    },
                    {
                        name:'Почта:',
                        description:'mag@mail.ru',
                        svg:MailSvg,
                        href:'mailto:' + 'mag@mail.ru',
                        target:'_self',
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

</style>