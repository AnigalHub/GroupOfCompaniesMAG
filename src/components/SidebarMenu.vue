<template>
    <div class="sidebar" :class="isOpened ? 'open' : ''">
        <div class="logo-details" style="margin: 6px 14px 0 14px;">
            <i class="bx" :class="isOpened ? 'bx-menu-alt-right' : 'bx-menu'" id="btn" @click="isOpened = !isOpened"/>
        </div>
        <div>
            <div id="my-scroll" style="margin: 6px 14px 0 14px;">
                <ul  class="nav-list" style="overflow: visible;">
                    <span v-for="(menuItem, index) in menuItems" :key="index">
                        <li>
                          <a :href="menuItem.link">
                            <i class="bx" :class="menuItem.icon || 'bx-square-rounded'"/>
                            <span class="links_name">{{ menuItem.name }}</span>
                          </a>
                        </li>
                  </span>
                </ul>
            </div>

        </div>
    </div>
</template>

<script>
    export default {
        name: 'SidebarMenuAkahon',
        props: {
            //! Menu settings
            isMenuOpen: {
                type: Boolean,
                default: true,
            },
            isPaddingLeft: {
                type: Boolean,
                default: true,
            },
            menuOpenedPaddingLeftBody: {
                type: String,
                default: '250px'
            },
            menuClosedPaddingLeftBody: {
                type: String,
                default: '78px'
            },
            //! Menu items
            menuItems: {
                type: Array,
                default: () => [
                    {
                        link: '#Home',
                        name: 'Главная',
                        icon: 'bx-grid-alt',
                    },
                    {
                        link: '#About',
                        name: 'О нас',
                        icon: 'bx-user',
                    },
                    {
                        link: '#Directions',
                        name: 'Направления',
                        icon: 'bx-pie-chart-alt-2',
                    },
                    {
                        link: '#Advantages',
                        name: 'Преимущества',
                        icon: 'bx-star',
                    },
                    {
                        link: '#Services',
                        name: 'Услуги',
                        icon: 'bx-food-menu',
                    },
                    {
                        link: '#Contacts',
                        name: 'Контакты',
                        icon: 'bx-message-dots',
                    },
                ],
            },
        },
        data() {
            return {
                isOpened: false
            }
        },
        watch: {
            isOpened() {
                window.document.body.style.paddingLeft = this.isOpened && this.isPaddingLeft ? this.menuOpenedPaddingLeftBody : this.menuClosedPaddingLeftBody
            }
        }
    }
</script>

<style>
    body {
        transition: all 0.5s ease;
    }
    .sidebar {
        display: flex;
        flex-direction: column;
        position: fixed;
        left: 0;
        top: 0;
        height: 100%;
        min-height: min-content;
        width: 78px;
        background: linear-gradient(#b7dfe9,#adc7e2, #a0a6d8);
        z-index: 99;
        transition: all 0.5s ease;
    }
    .sidebar.open {
        width: 250px;
    }
    .sidebar .logo-details {
        height: 60px;
        display: flex;
        align-items: center;
        position: relative;
    }

    .sidebar .logo-details #btn {
        position: absolute;
        top: 50%;
        right: 0;
        transform: translateY(-50%);
        font-size: 1.6rem;
        transition: all 0.4s ease;
        text-align: center;
        cursor: pointer;
    }
    .sidebar.open .logo-details #btn {
        text-align: right;
    }
    .sidebar i {
        color: black;
        height: 60px;
        min-width: 50px;
        font-size: 1.6rem;
        text-align: center;
        line-height: 60px;
    }
    .sidebar .nav-list {
        margin-left: -32px;
        margin-top: 20px;
    }
    .sidebar li {
        position: relative;
        margin: 8px 0;
        list-style: none;
    }
    .sidebar li a {
        display: flex;
        height: 100%;
        width: 100%;
        align-items: center;
        text-decoration: none;
        transition: all 0.4s ease;
        color: black;
    }

    .sidebar li i {
        height: 50px;
        line-height: 50px;
        font-size: 1.6rem;
        border-radius: 12px;
    }
    .my-scroll-active {
        overflow-y: auto;
    }
    #my-scroll {
        overflow-y: auto;
        height: calc(100% - 30px);
    }
    #my-scroll::-webkit-scrollbar{
        display:none;
    }
</style>