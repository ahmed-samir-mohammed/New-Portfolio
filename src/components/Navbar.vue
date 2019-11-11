<template>
    <div>
        <b-navbar toggleable="lg" variant="info" class="fixed-top">
            <b-navbar-brand @click="show = false">
                <router-link class="brand" :to="{name: 'Home'}">
                    Ahmed && ALi
                </router-link>
            </b-navbar-brand>

            <b-navbar-nav class="ml-auto">
                <button @click="show = !show" class="menu-btn">
                    <span></span>
                    <span></span>
                    <span></span>
                </button>
            </b-navbar-nav>
        </b-navbar>

        <transition name="fade">
            <div class="menu-page" v-if="show">
                <ul class="list-item list-unstyled">
                    <li @click="show = !show">
                        <router-link :to="{name: 'Home'}">Home</router-link>
                    </li>
                    <li @click="show = !show">
                        <router-link :to="{name: 'About'}">About</router-link>
                    </li>
                    <li @click="show = !show">
                        <router-link :to="{name: 'Projects'}">Projects</router-link>
                    </li>
                    <li @click="show = !show">
                        <router-link :to="{name: 'Contact'}">Contact</router-link>
                    </li>
                </ul>
            </div>  
        </transition>
    </div>
</template>

<script>
export default {
    name: 'Home',
    data() {
        return {
            show: false
        }
    }
}
</script>

<style lang="scss">
    .navbar {
        height: 7vh;
        background: #1f1f1f !important;
        a.brand {
            display: flex;
            align-items: center;
            text-decoration: none;
            color: #fff;
            &:hover {
                text-decoration: none;
            }
        }
        .menu-btn {
            background: none;
            border: 0;
            display: flex;
            flex-direction: column;
            align-items: flex-end;
            padding: .5rem;
            outline: 0;
            span {
                background-color: #fff;
                height: 2px;
                margin-bottom: .3rem;
                transition: all .3s ease-in-out;
                &:first-of-type {
                    width: 1rem;
                }
                &:nth-of-type(2) {
                    width: 1.5rem
                } 
                &:last-of-type {
                    width: 1.2rem;
                    margin-bottom: 0;
                }
            }
            &:hover {
                span {
                    width: 2rem
                }
            }
        }
    }
    .menu-page {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        width: 100%;
        height: 100vh;
        background-color: #1f1f1f;
        position: fixed;
        top: 0;
        left: 0;
        bottom: 0;
        z-index: 2;
        ul {
            display: flex;
            align-items: flex-start;
            justify-content: center;
            flex-direction: column;
            li {
                margin-bottom: 2rem;
                animation-duration: .8s;
                a {
                    color: #fff;
                    text-decoration: none;
                    font-size: 3rem;
                    position: relative;
                    &::after {
                        content: '';
                        background: #fff;
                        width: 0;
                        height: 2px;
                        transition: all .3s ease-in-out;
                        position: absolute;
                        left: 0;
                        bottom: 0;
                    }
                    &:hover {
                        &::after {
                            width: 100%;
                        }
                    }
                }
                &:first-of-type {
                   animation-name: RightToLeft_1;
                   animation-delay: .1s 
                }
                &:nth-of-type(2) {
                    animation-name: RightToLeft_2;
                    animation-delay: .1s 
                }
                &:nth-of-type(3) {
                    animation-name: RightToLeft_3;
                    animation-delay: .1s 
                }
                &:last-of-type {
                   animation-name: RightToLeft_4;
                   animation-delay: .1s;
                }
            }
        }
    }
    .fade-enter-active, 
    .fade-leave-active {
        transition: all .3s ease-in-out;
    }
    
    .fade-enter, 
    .fade-leave-to {
        width: 0%;
        opacity: 0;
        li {
            opacity: 0;
        }
    }

    @keyframes RightToLeft_1 {
        0% {
            opacity: 0;
            transform: translateX(-5rem);
            
        }
        100% {
            transform: translateX(0);
            opacity: 1;
        }
    }
    @keyframes RightToLeft_2 {
        0% {
            opacity: 0;
            transform: translateX(-10rem);
        }
        100% {
            transform: translateX(0);
            opacity: 1;
        }
    }
    @keyframes RightToLeft_3 {
        0% {
            opacity: 0;
            transform: translateX(-15rem);
        }
        100% {
            transform: translateX(0);
            opacity: 1;
        }
    }
    @keyframes RightToLeft_4 {
        0% {
            opacity: 0;
            transform: translateX(-20rem);
        }
        100% {
            transform: translateX(0);
            opacity: 1;
        }
    }
    
</style>