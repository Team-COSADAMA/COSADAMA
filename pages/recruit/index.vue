<template>
<div class="bg-black w-full">
    <div class="max-w-7xl mx-auto px-6">

<!-- 상단 -->
        <div class="pt-36 md:pt-52 pb-8 md:pb-20 px-1 md:px-3 fadeinupcom">
            <div class="pb-3 text-sm md:text-base recruiting-gradient font-medium">R E C R U I T</div>
            <div class="text-white text-3xl md:text-4xl font-semibold">더 많은 사람이 <br/> 더 발전할 수 있도록</div>
            <div class="text-slate-400 pt-3 md:pt-5 text-base md:text-lg">코사다마는 비전공자를 위한 코딩 커뮤니티라는 목표 하에, <br class="hidden md:inline"/> 보다 많은 분들이 코딩을 접하실 수 있도록 노력하고 있습니다.</div>
            <div class="pt-2 md:pt-5 text-white text-base md:text-lg hover:underline"> <nuxt-link :to="{path: '/'}">코사다마의 목표 알아보기</nuxt-link> </div>
        </div>

<!-- 모집 리스트 -->

        <div class="pb-16 md:pb-28">

            <div v-for="recruit of recruits" :key="recruit" class="fadeinupcom px-0 py-3 md:px-5 md:py-5 bg-transparent hover:bg-zinc-800 rounded-xl transition hover:duration-200">
                <nuxt-link :to="{path: `/recruit/${recruit.slug}`}">
                    <div class="block md:flex items-center md:justify-between px-4 md:px-6">
                        <div class="text-white text-lg md:text-xl font-medium w-full md:w-3/6">{{recruit.title}} <span class="text-slate-400 pl-2 text-base hidden md:inline">{{recruit.period}}</span></div>
                        <div class="text-slate-400 text-base w-2/6 text-left hidden md:block"> {{recruit.tag[0]}} · {{recruit.tag[1]}} · {{recruit.tag[2]}}</div>
                        <div class="text-slate-400 text-sm md:text-base w-auto md:w-1/6 text-left md:text-right">  <span class="text-slate-400 text-sm inline md:hidden">{{recruit.period}} · </span> {{recruit.status}}</div>
                    </div>
                </nuxt-link>
            </div>

        </div>

    </div>
</div>
</template>

<script>
    export default {
    async asyncData({ $content, params }) {
        const recruits = await $content('recruit', params.id)
        .sortBy('order', 'asc')
        .fetch();
        return { recruits }
    },
    head() {
        return {
            title: '코사다마 영입 | COSADAMA',
            htmlAttrs: {
            lang: 'ko'
            },
            meta: [
            { charset: 'utf-8' },
            { name: 'viewport', content: 'width=device-width, initial-scale=1' },
            {
                hid: 't-type',
                name: 'twitter:card',
                content: 'summary_large_image'
            },
            {
            hid: 'og-type',
            property: 'og:type',
            content: 'website'
            },
            {
            hid: 'og:title',
            property: 'og:title',
            content: '코사다마 영입 | COSADAMA'
            },
            {
            hid: 'og:description',
            property: 'og:description',
            content: '중앙대학교 비전공자 코딩 커뮤니티 코사다마의 영입 페이지입니다.'
            },
            {
            hid: 'og:image',
            property: 'og:image',
            // content: this.article.img
            content: 'https://raw.githubusercontent.com/Team-COSADAMA/COSADAMA/main/static/og_image.png'
            },
            {
            hid: 'og:image:secure_url',
            property: 'og:image:secure_url',
            content: 'https://raw.githubusercontent.com/Team-COSADAMA/COSADAMA/main/static/og_image.png'
            },
            {
            hid: 'og:image:alt',
            property: 'og:image:alt',
            content: 'article image'
            },
            {
            hid: 'og:url',
            name: 'og:url',
            content: 'https://cosadama.com/recuit'
            },
            ],
        }
    },
}
</script>

<style scoped>
.bg-img {
        background-position: center;
        background-repeat:  no-repeat;
        /* background-attachment: fixed; */
        background-size:  cover;
        background-color: #000000;
}
.section {
    position: relative;
}
.inner {
    box-sizing: border-box;
    position: relative;
}
.keep-all {
    word-break: keep-all;
}
.lead-box {
    border-radius: 70%;
    overflow: hidden;
}
.profile {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>