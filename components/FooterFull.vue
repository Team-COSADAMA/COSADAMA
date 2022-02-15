<template>
    <footer class="w-full bg-zinc-900 py-11 md:py-14 md:pt-20 md:pb-24 px-2 md:px-5">
        
        <div class="max-w-7xl mx-auto block md:flex relative px-0 md:px-4">

            <div class="justify-around md:justify-start px-8 md:px-0 items-start flex">
                <ul class="w-25 md:w-36 md:ml-0 md:m-0">
                    <li class="mb-3 font-medium text-gray-300">코사다마</li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline"><nuxt-link :to="{path: '/about'}" replace>소개</nuxt-link></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline"> <nuxt-link :to="{path: '/recruit'}" replace>영입</nuxt-link> </li>
                </ul>

                <ul class="w-25 md:w-36 md:ml-0 md:m-0">
                    <li class="mb-3 font-medium text-gray-300">관련 사이트</li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline"><a href="https://curriculum.cosadama.com">커리큘럼</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline"><a href="https://www.blog.cosadama.com">블로그</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline"><a href="https://github.com/Team-COSADAMA">깃헙</a></li>
                </ul>

                <ul class="w-25 md:w-36 md:ml-0 md:m-0">
                    <li class="mb-3 font-medium text-gray-300">문의</li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline"><a href="mailto:mail@cosadama.com">이메일</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline"><a href="#">채널톡</a></li>
                    <li class="mb-1.5 font-normal text-gray-500 hover:underline"><a href="https://pf.kakao.com/_MYkvK?trk=public_post_share-update_update-text">카카오톡</a></li>
                </ul>
            </div>

            <nuxt-link to="/" class="hidden md:block flex justify-center md:absolute md:top-0 md:right-0 md:items-center md:m-0">
                <div class=""><FooterLogo/></div>
            </nuxt-link>

            <ul class="flex justify-center md:absolute md:bottom-0 md:right-0 md:block mt-10 md:mt-0">
                <li class="text-xs md:text-sm font-normal text-gray-500">Designed & Developed by 
                    <a class="underline" href="https://github.com/thepenielcho">Peniel Cho</a></li>
            </ul>

        </div>

    </footer>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
</style>