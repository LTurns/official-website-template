<template>
    <div class="u-header">
        <div class="layout clearfix">
            <u-icon name="logo" to="/" scale="0.15" class="u-header-logo"></u-icon>
            <div class="u-header-nav">
                <ul class="u-header-content">
                    <li v-for="item in navs" :key="item.name" :class="['u-header-content-item',{'disable': item.disable}]">
                        <u-link v-if="item.url" :to="item.url">{{item.name}}</u-link>
                        <p v-else ><span class="hasmenu">{{item.name}}</span><i class="arraw down"></i></p>
                        <div class="cat" v-if="item.name==='PRODUCTS'">
                            <div class="cat-box">
                                <s-first-menu />
                            </div>
                        </div>
                        <div class="cat" v-if="item.name==='NEWS'">
                            <div class="cat-box">
                                <s-second-menu />
                            </div>
                        </div>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
import SFirstMenu from '~/components/index/s-first-menu.vue'
import SSecondMenu from '~/components/index/s-next-menu.vue'

export default {
    components: {
        SFirstMenu,
        SSecondMenu
    },
    data() {
        return {
            navs: [
                {
                    name: 'PRODUCTS'
                },
                {
                    name: 'NEWS'
                },
                {
                    name: 'ABOUT US',
                    url: '/about'
                },
                {
                    name: 'WHERE TO BUY',
                    url: '/buy'
                }, 
                {
                    name: 'CONTACT US',
                    url: '/contact'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.u-header {
    width: 100%;
    font-size: 16px;
    position: absolute;
    top: 0;
    left: 0;
    box-sizing: border-box;
    color: black;
    z-index: 100;
    // transition: background 0.3s ease;

    .layout {
        min-width: $content-width;
        width: auto;
        position: relative;
    }

    &:hover {
        background-color: #282727;
    }

    &-logo {
        float: left;
        position: relative;
        top: 6px;
        display: inline-block;
        margin-left: 30px;
    }

    &-nav {
        float: right;
        margin-right: 5%;

        .u-header-content-item {
            float: left;
            text-align: center;
            padding: 20px 26px;
            cursor: pointer;

            &.disable {
                color: black;
                cursor: default;

                .u-link {
                    cursor: default;
                }
            }

            &:first-child {
                margin-left: 45px;
            }

            &:hover {
                background-color: $black;
                color: white;

                .cat-box {
                    transform: scaleY(1);
                }

                .arraw {
                    transform: rotate(225deg);
                }
            }

            .hasmenu {
                margin-right: 6px;
            }

            .arraw {
                position: relative;
                top: -3px;
                transition: transform 0.3s ease;
                transform-origin: 50% 75%;
            }
        }
    }

    .cat-box {
        color: #fff;
        box-sizing: border-box;
        padding-left: 20px;
        font-size: 15px;
        background-color: $black;
        position: absolute;
        width: 100%;
        top: 59px;
        left: 0;
        text-align: center;
        transition: transform 0.3s ease-out;
        transform: scaleY(0);
        transform-origin: center top;
        cursor: default;
        background-color: black;
    }
}
</style>
