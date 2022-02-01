<template>
        <div class="px-5 md:px-10 py-0 md:py-2">
            <div class="border-b border-slate-400 h-16 mx-auto flex items-center justify-between">
                    <div class="flex">
                        <div class="md:hidden flex content-center">
                            <button @click="drawer">
                            <Menu class="mr-1"/>
                            </button>
                        </div>
                        <nuxt-link to='/'> <Logo class="drop-shadow-sm pl-2" /> </nuxt-link>
                    </div>
                    <div class="group pr-3">
                        <a href="https://github.com/Team-COSADAMA" target="blank" class="">
                            <GithubLogo />
                        </a>
                    </div>
            </div>
            <transition
                enter-class="opacity-0"
                enter-active-class="ease-out transition-medium"
                enter-to-class="opacity-100"
                leave-class="opacity-100"
                leave-active-class="ease-out transition-medium"
                leave-to-class="opacity-0"
            >
                <div @keydown.esc="isOpen = false" v-show="isOpen" class="z-10 fixed inset-0 transition-opacity">
                    <div @click="isOpen = false" class="absolute inset-0 bg-black opacity-50" tabindex="0"></div>
                </div>
            </transition>

            <aside class="p-5 transform top-0 left-0 w-64 bg-white fixed h-full overflow-auto ease-in-out transition-all duration-300 z-30" :class="isOpen ? 'translate-x-0' : '-translate-x-full'">
                
                <div class="close">
                <button class="absolute top-0 right-0 mt-4 mr-4" @click=" isOpen = false">
                    <Close />
                </button>
                </div>

            </aside>
        </div>
</template>

<script>
    export default {
    data() {
        return {
        isOpen: false
        };
    },
    methods: {
        drawer() {
        this.isOpen = !this.isOpen;
        }
    },
    watch: {
        isOpen: {
        immediate: true,
        handler(isOpen) {
            if (process.client) {
            if (isOpen) document.body.style.setProperty("overflow", "hidden");
            else document.body.style.removeProperty("overflow");
            }
        }
        }
    },
    mounted() {
        document.addEventListener("keydown", e => {
        if (e.keyCode == 27 && this.isOpen) this.isOpen = false;
        });
    }
    };
</script>