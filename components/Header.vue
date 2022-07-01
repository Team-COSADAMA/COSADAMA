<template>
    <div class="w-full z-40 bg-black shadow-lg">
        <div class="max-w-screen-2xl px-3 md:px-7 py-3 md:py-9 border-slate-400 h-16 mx-auto flex items-center justify-between">
            
            <nuxt-link to='/'> <Logo class="drop-shadow-sm pl-2" /> </nuxt-link>
            
            <div>
                <ul class="flex space-x-3 items-center">
                    <li class="py-1.5 px-2.5 rounded-lg hover:bg-zinc-800 hidden md:block text-slate-300 lgtoxl hover:text-white transition hover:duration-300 font-normal">
                        <nuxt-link :to="{path: '/about'}" replace>A B O U T</nuxt-link>
                    </li>
                    <li class="py-1.5 px-2.5 rounded-lg hover:bg-zinc-800 hidden md:block text-slate-300 lgtoxl hover:text-white transition hover:duration-300 font-normal">
                        <nuxt-link :to="{path: '/recruit'}" replace>R E C R U I T</nuxt-link>
                    </li>
                    <li class="py-1.5 px-2.5 rounded-lg hover:bg-zinc-800 hidden md:block text-slate-300 lgtoxl hover:text-white transition hover:duration-300 font-normal">
                        <a href="https://curriculum.cosadama.com/" target="blank" class="flex items-center"> <span class="mr-1.5">C U R R I C U L U M</span> <External class="w-4" /> </a>
                    </li>
                    <li class="py-1.5 px-2.5 rounded-lg hover:bg-zinc-800 hidden md:block text-slate-300 lgtoxl hover:text-white transition hover:duration-300 font-normal">
                        <a href="https://www.blog.cosadama.com/" target="blank" class="flex items-center"> <span class="mr-1.5">B L O G</span> <External class="w-4" /> </a>
                    </li>
                    <!-- <li class="py-1.5 px-2.5 rounded-lg hover:bg-zinc-800 hidden md:block text-slate-300 lgtoxl hover:text-white transition hover:duration-300 font-normal">
                        <a href="https://github.com/Team-COSADAMA" target="blank" class="flex items-center"> <span class="mr-1.5">G I T H U B</span> <External class="w-4" /> </a>
                    </li> -->
                </ul>
            </div>


            <div class="md:hidden flex content-center">
                <button @click="drawer">
                <Menu class="mr-0.5"/>
                </button>
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

            <aside class="p-5 transform top-0 left-0 w-64 bg-black fixed h-full overflow-auto ease-in-out transition-all duration-300 z-30" :class="isOpen ? 'translate-x-0' : '-translate-x-full'">
                
                <div class="close">
                <button class="absolute top-0 right-0 mt-4 mr-4" @click=" isOpen = false">
                    <Close />
                </button>
                </div>

                <ul class="mt-10">
                <li><nuxt-link :to="{path: '/about'}" replace @click="isOpen = false" class="text-slate-300 my-3 inline-block w-full text-center">A B O U T</nuxt-link></li>
                <li><nuxt-link :to="{path: '/recruit'}" replace @click="isOpen = false" class="text-slate-300 my-3 inline-block w-full text-center">R E C R U I T</nuxt-link></li>
                <li><a href="https://curriculum.cosadama.com" @click="isOpen = false" class="text-slate-300 my-3 inline-block w-full text-center">C U R R I C U L U M</a></li>
                <li><a href="https://www.blog.cosadama.com" @click="isOpen = false" class="text-slate-300 my-3 inline-block w-full text-center">B L O G</a></li>
                <li><a href="https://github.com/Team-COSADAMA" @click="isOpen = false" class="text-slate-300 my-3 inline-block w-full text-center">G I T H U B</a></li>
                </ul>

                <div @click="isOpen = false" class="flex w-full pt-6 pb-8 items-center justify-center">
                    <LogoAside class="h-7" />
                </div>

            </aside>


        </div>
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

<style scoped>
.lgtoxl{
    font-size: 0.9rem;
}
</style>