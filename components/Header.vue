<template>
    <div class="w-full z-40 bg-black shadow-lg">
        <div class="max-w-screen-2xl px-3 md:px-10 py-3 md:py-9 border-slate-400 h-16 mx-auto flex items-center justify-between">
            
            <nuxt-link to='/'> <Logo class="drop-shadow-sm pl-2" /> </nuxt-link>
            
            <div>
                <ul class="flex space-x-4 items-center">
                    <!-- <li class="py-1.5 px-2.5 rounded-lg hover:bg-zinc-800 hidden md:block text-slate-300 lgtoxl hover:text-white transition hover:duration-300 font-normal">
                        <nuxt-link :to="{path: '/about'}" replace>About</nuxt-link>
                    </li>
                    <li class="py-1.5 px-2.5 rounded-lg hover:bg-zinc-800 hidden md:block text-slate-300 lgtoxl hover:text-white transition hover:duration-300 font-normal">
                        <nuxt-link :to="{path: '/recruit'}" replace>Recruit</nuxt-link>
                    </li> -->
                    <li class="py-1.5 px-2.5 rounded-lg hover:bg-zinc-800 hidden md:block text-slate-300 lgtoxl hover:text-white transition hover:duration-300 font-normal">
                        <a href="https://curriculum.cosadama.com/" target="blank">Curriculum</a>
                    </li>
                    <li class="py-1.5 px-2.5 rounded-lg hover:bg-zinc-800 hidden md:block text-slate-300 lgtoxl hover:text-white transition hover:duration-300 font-normal">
                        <a href="https://www.blog.cosadama.com/" target="blank">Blog</a>
                    </li>
                    <li class="py-1.5 px-2.5 rounded-lg hover:bg-zinc-800 hidden md:block text-slate-300 lgtoxl hover:text-white transition hover:duration-300 font-normal">
                        <a href="https://github.com/Team-COSADAMA" target="blank">GitHub</a>
                    </li>
                    <li class="group pl-3 pr-3 block md:hidden">
                    <a href="https://github.com/Team-COSADAMA" target="blank" class="">
                        <GithubLogo class="drop-shadow" />
                    </a>
                    </li>
                </ul>
            </div>


            <!-- <div class="md:hidden flex content-center">
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

            <aside class="p-5 transform top-0 left-0 w-64 bg-white fixed h-full overflow-auto ease-in-out transition-all duration-300 z-30" :class="isOpen ? 'translate-x-0' : '-translate-x-full'">
                
                <div class="close">
                <button class="absolute top-0 right-0 mt-4 mr-4" @click=" isOpen = false">
                    <Close />
                </button>
                </div>

                <div @click="isOpen = false" class="flex w-full pt-12 pb-8 items-center justify-center border-b">
                    <HeaderLogo />
                </div>

                <ul class="divide-y font-light">
                <li><nuxt-link :to="{path: '/about'}" replace @click="isOpen = false" class="text-gray-500 my-4 inline-block poppins">About</nuxt-link></li>
                <li><nuxt-link :to="{path: '/all-articles'}" replace @click="isOpen = false" class="text-gray-500 my-4 inline-block poppins">Articles</nuxt-link></li>
                <li><nuxt-link :to="{path: '/categories'}" replace @click="isOpen = false" class="text-gray-500 my-4 inline-block poppins">Categories</nuxt-link></li>
                <li><nuxt-link :to="{path: '/members'}" replace @click="isOpen = false" class="text-gray-500 my-4 inline-block poppins">Members</nuxt-link></li>
                <li><nuxt-link :to="{path: '/projects'}" @click="isOpen = false" class="text-gray-500 my-4 inline-block poppins">Projects</nuxt-link></li>
                </ul>

                <div class="flex items-center justify-center">
                <div class="social flex space-x-6 mt-6">
                    <a href="https://github.com/GDSC-CAU" target="blank">
                        <GithubLogo  class="w-6 h-6"/>
                    </a>
                    <a href="https://gdsc-cau.notion.site/GDSC-CAU-Member-Space-a8f22210d95a4e439dfae3a45b04ceb2" target="blank">
                        <NotionLogo class="w-6 h-6"/>
                    </a>
                </div>
                </div>

            </aside> -->


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
    font-size: 1.145rem;
}
</style>