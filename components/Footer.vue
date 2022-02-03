<template>
    <footer class="w-full bg-black">
        <div class="max-w-7xl mx-auto pt-11 pb-14 md:pt-11 md:pb-24 px-2 md:px-0 border-t border-gray-300 flex flex-col md:flex-row items-center justify-start md:justify-between">
            
            <div class="flex md:hidden justify-center items-center pb-9">
                <nuxt-link to="/">
                    <Logo class="h-4"/>
                </nuxt-link>
            </div>

            <ul class="flex flex-col md:flex-row text-sm space-y-2 md:space-y-0">
                <li class="text-gray-500 mr-0 md:mr-3 flex justify-center"><nuxt-link to="/" class="hover:underline">Curriculum</nuxt-link></li>
                <li class="text-gray-500 mr-0 md:mr-3 flex justify-center"><a target="blank" href="#" class="hover:underline">Blog</a></li>
                <li class="text-gray-500 mr-0 md:mr-3 flex justify-center"><a target="blank" href="#" class="hover:underline">GitHub</a></li>
                <li class="text-gray-500 mr-0 md:mr-3 flex justify-center"><a href="mailto:cosadamasocio@gmail.com" class="hover:underline">Email</a></li>
            </ul>

            <div class="hidden md:flex justify-center items-center">
                <nuxt-link to="/">
                    <Logo />
                </nuxt-link>
            </div>

            <div class="text-xs md:text-sm text-gray-500 mt-8 md:mt-0 mb-3">
                Designed and Developed by <a href="https://github.com/thepenielcho" target="blank" class="underline">Peniel Cho</a>
            </div>

        </div>
    </footer>
</template>