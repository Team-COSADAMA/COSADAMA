<template>
    <div class="w-full bg-black relative">

    <div class="bg-img section w-full py-36 sm:py-48 md:py-60 2xl:py-80 recruit-img" :style="{ backgroundImage: `url(/${recruit.img})` }">
    </div>

    <div class="max-w-7xl mx-auto pt-8 md:pt-16 pb-7 md:pb-12 px-6 md:px-10">
        <div class="text-white text-3xl md:text-4xl font-semibold keep-all">{{recruit.title}}</div>
    </div>

    <div class="block md:hidden text-white px-6 pb-7">
            <ul class="divide-y pb-4">
                <li class="pb-3 pt-1 text-slate-400 text-base px-1"> <span class="w-1/3 inline-block">활동 형태</span>  <span class="text-white">{{recruit.type}}</span> </li>
                <li class="py-3 text-slate-400 text-base px-1"> <span class="w-1/3 inline-block">활동 기간</span> <span class="text-white">{{recruit.period}}</span> </li>
                <li class="py-3 text-slate-400 text-base px-1"> <span class="w-1/3 inline-block">모집 현황</span> <span class="text-white">{{recruit.status}}</span> </li>
            </ul>
            <a :href="`${recruit.applyLink}`" class="w-full rounded-lg bg-zinc-800 text-center flex items-center justify-center py-3.5 hover:bg-zinc-700 transition hover:duration-300">
            지원하기
            </a>
    </div>

    <div class="max-w-7xl mx-auto px-6 md:px-10 justify-between flex">
        <div class="pr-0 md:pr-8 w-full md:w-2/3 pb-16">
            <div class="text-white font-medium text-lg pb-2">코사다마 소개</div>
            <div class="text-slate-400 pb-8">코사다마(COSADAMA)는 2020년 1월 13일부터 시작된 중앙대학교의 비전공자 코딩 커뮤니티입니다. 
                모임명은 코딩과 호사다마(好事多魔)의 합성어로, 
                힘든 난관들을 헤쳐나가면 끝내 성공적으로 코딩 천재가 될 수 있으리라는 의미를 담고 있습니다.
            </div>

            <div class="text-white font-medium text-lg pb-2">아래 조건을 만족하셔야 지원하실 수 있어요.</div>
            <ul class="space-y-2 text-slate-400 pb-8">
                <li v-if="`${recruit.qualification[0]}` == undefined || `${recruit.qualification[0]}` == null || `${recruit.qualification[0]}` == 'null' || `${recruit.qualification[0]}` == 'undefined'"></li>
                <li v-else>· {{recruit.qualification[0]}}</li>
                <li v-if="`${recruit.qualification[1]}` == undefined || `${recruit.qualification[1]}` == null || `${recruit.qualification[1]}` == 'null' || `${recruit.qualification[1]}` == 'undefined'"></li>
                <li v-else>· {{recruit.qualification[1]}}</li>
                <li v-if="`${recruit.qualification[2]}` == undefined || `${recruit.qualification[2]}` == null || `${recruit.qualification[2]}` == 'null' || `${recruit.qualification[2]}` == 'undefined'"></li>
                <li v-else>· {{recruit.qualification[2]}}</li>
                <li v-if="`${recruit.qualification[3]}` == undefined || `${recruit.qualification[3]}` == null || `${recruit.qualification[3]}` == 'null' || `${recruit.qualification[3]}` == 'undefined'"></li>
                <li v-else>· {{recruit.qualification[3]}}</li>
                <li v-if="`${recruit.qualification[4]}` == undefined || `${recruit.qualification[4]}` == null || `${recruit.qualification[4]}` == 'null' || `${recruit.qualification[4]}` == 'undefined'"></li>
                <li v-else>· {{recruit.qualification[4]}}</li>
            </ul>

            <div class="text-white font-medium text-lg pb-2">이런 분이시면 더 좋아요!</div>
            <ul class="space-y-2 text-slate-400 pb-8">
                <li v-if="`${recruit.toThose[0]}` == undefined || `${recruit.toThose[0]}` == null || `${recruit.toThose[0]}` == 'null' || `${recruit.toThose[0]}` == 'undefined'"></li>
                <li v-else>· {{recruit.toThose[0]}}</li>
                <li v-if="`${recruit.toThose[1]}` == undefined || `${recruit.toThose[1]}` == null || `${recruit.toThose[1]}` == 'null' || `${recruit.toThose[1]}` == 'undefined'"></li>
                <li v-else>· {{recruit.toThose[1]}}</li>
                <li v-if="`${recruit.toThose[2]}` == undefined || `${recruit.toThose[2]}` == null || `${recruit.toThose[2]}` == 'null' || `${recruit.toThose[2]}` == 'undefined'"></li>
                <li v-else>· {{recruit.toThose[2]}}</li>
                <li v-if="`${recruit.toThose[3]}` == undefined || `${recruit.toThose[3]}` == null || `${recruit.toThose[3]}` == 'null' || `${recruit.toThose[3]}` == 'undefined'"></li>
                <li v-else>· {{recruit.toThose[3]}}</li>
                <li v-if="`${recruit.toThose[4]}` == undefined || `${recruit.toThose[4]}` == null || `${recruit.toThose[4]}` == 'null' || `${recruit.toThose[4]}` == 'undefined'"></li>
                <li v-else>· {{recruit.toThose[4]}}</li>
            </ul>

            <div class="text-white font-medium text-lg pb-2">모집 일정</div>
            <div class="text-slate-400 pb-8">
                <div class="pb-2">· 접수 : {{recruit.date[0]}} | {{recruit.date[1]}}</div>
                <div class="pb-2">· 발표 : {{recruit.date[2]}} | {{recruit.date[3]}}</div>
                <div class="">· 온보딩 : {{recruit.date[4]}} | {{recruit.date[5]}}</div>
            </div>

            <div class="text-white font-medium text-lg pb-2">모집 인원</div>
            <div class="text-slate-400 pb-8">
                <div>약 {{recruit.expectedNum}}분을 모집할 예정입니다. <br> <span class="text-sm text-slate-500">모집 인원은 추후 운영 상황에 따라 변동될 수 있습니다.</span></div>
            </div>

            <div v-if="`${recruit.benefit}` == undefined || `${recruit.benefit}` == null || `${recruit.benefit}` == 'null' || `${recruit.benefit}` == 'undefined'">
            </div>
            <div v-else>
                <div class="text-white font-medium text-lg pb-2">혜택 안내</div>
                <ul class="space-y-2 text-slate-400 pb-8">
                    <li v-if="`${recruit.benefit[0]}` == undefined || `${recruit.benefit[0]}` == null || `${recruit.benefit[0]}` == 'null' || `${recruit.benefit[0]}` == 'undefined'"></li>
                    <li v-else>· {{recruit.benefit[0]}}</li>
                    <li v-if="`${recruit.benefit[1]}` == undefined || `${recruit.benefit[1]}` == null || `${recruit.benefit[1]}` == 'null' || `${recruit.benefit[1]}` == 'undefined'"></li>
                    <li v-else>· {{recruit.benefit[1]}}</li>
                    <li v-if="`${recruit.benefit[2]}` == undefined || `${recruit.benefit[2]}` == null || `${recruit.benefit[2]}` == 'null' || `${recruit.benefit[2]}` == 'undefined'"></li>
                    <li v-else>· {{recruit.benefit[2]}}</li>
                    <li v-if="`${recruit.benefit[3]}` == undefined || `${recruit.benefit[3]}` == null || `${recruit.benefit[3]}` == 'null' || `${recruit.benefit[3]}` == 'undefined'"></li>
                    <li v-else>· {{recruit.curriculum[3]}}</li>
                </ul>
            </div>

            <div v-if="`${recruit.curriculum}` == undefined || `${recruit.curriculum}` == null || `${recruit.curriculum}` == 'null' || `${recruit.curriculum}` == 'undefined'">
            </div>
            <div v-else>
                <div class="text-white font-medium text-lg pb-2">커리큘럼 안내</div>
                <ul class="space-y-2 text-slate-400 pb-8">
                    <li v-if="`${recruit.curriculum[0]}` == undefined || `${recruit.curriculum[0]}` == null || `${recruit.curriculum[0]}` == 'null' || `${recruit.curriculum[0]}` == 'undefined'"></li>
                    <li v-else>1. {{recruit.curriculum[0]}} : {{recruit.curriculum[1]}}</li>
                    <li v-if="`${recruit.curriculum[2]}` == undefined || `${recruit.curriculum[2]}` == null || `${recruit.curriculum[2]}` == 'null' || `${recruit.curriculum[2]}` == 'undefined'"></li>
                    <li v-else>2. {{recruit.curriculum[2]}} : {{recruit.curriculum[3]}}</li>
                    <li v-if="`${recruit.curriculum[4]}` == undefined || `${recruit.curriculum[4]}` == null || `${recruit.curriculum[4]}` == 'null' || `${recruit.curriculum[4]}` == 'undefined'"></li>
                    <li v-else>3. {{recruit.curriculum[4]}} : {{recruit.curriculum[5]}}</li>
                    <li v-if="`${recruit.curriculum[6]}` == undefined || `${recruit.curriculum[6]}` == null || `${recruit.curriculum[6]}` == 'null' || `${recruit.curriculum[6]}` == 'undefined'"></li>
                    <li v-else>4. {{recruit.curriculum[6]}} : {{recruit.curriculum[7]}}</li>
                    <li v-if="`${recruit.curriculum[8]}` == undefined || `${recruit.curriculum[8]}` == null || `${recruit.curriculum[8]}` == 'null' || `${recruit.curriculum[8]}` == 'undefined'"></li>
                    <li v-else>5. {{recruit.curriculum[8]}} : {{recruit.curriculum[9]}}</li>
                    <li class="text-sm text-slate-500">커리큘럼은 추후 운영 상황에 따라 변동될 수 있습니다.</li>
                </ul>
            </div>

            <div v-if="`${recruit.type}` == '멤버'">
                <div class="text-white font-medium text-lg pb-2">활동 안내</div>
                <div class="text-slate-400 pb-8">
                    <div class="pb-2">· 공지 및 스터디 안내, 질의 응답은 Slack을 통해 이루어집니다.</div>
                    <div class="pb-2">· 스터디 가이드는 합류 후 제공되는 Notion 페이지에서 확인 가능합니다.</div>
                    <div class="pb-2">· 매주 정해진 분량을 스스로 공부합니다.</div>
                    <div class="pb-2">· 방학에는 의무적으로 하나 이상의 프로젝트에 참여합니다.</div>
                    <div class="">· 2학기 이상 활동 시 프로젝트, 스터디, 휴식 중 하나를 선택해 활동할 수 있습니다.</div>
                </div>
            </div>
            <div v-else></div>

            <div class="text-white font-medium text-lg pb-2">회비 안내</div>
            <div class="text-slate-400 pb-8">
                <div v-if="`${recruit.type}` == '멤버'">
                    <div class="pb-2">· 첫 학기 : 1.5만원</div>
                    <div class="pb-2">· 이후 : 0.5만원</div>
                    <div class="text-sm text-slate-500">회비는 커리큘럼 개발, 운영비 등으로 사용됩니다. <br> 중도 하차 혹은 퇴출 시 환불되지 않습니다.</div>
                </div>
                <div v-else>
                    STAFF는 회비를 제출하지 않습니다.
                </div>
            </div>

            <div class="text-white font-medium text-lg">그동안의 성과</div>
            <div class="w-full grid grid-cols-1 space-y-4 mt-4 text-sm md:text-base pb-8">
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🏆 &nbsp; 정부혁신제안 끝장개발대회 커뮤니티상 수상!</div>
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🏆 &nbsp; 산림복지 데이터 시각화 공모전 우수상 수상!</div>
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🏆 &nbsp; DACON 국회 입법활동 빅데이터 경진대회 입상!</div>
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🏆 &nbsp; COMPAS 광양시 분석 경진대회 입상!</div>
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🎓 &nbsp; 중앙대학교 HIKE LAB(지식그래프, AI 등) 합격!</div>
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🎓 &nbsp; 중앙대학교 MoTS LAB 합격!</div>
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🎓 &nbsp; 성균관대학교 솜SIC LAB(텍스트 마이닝 등) 합격!</div>
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🎉 &nbsp; NAVER CONNECT 재단 인턴 합격!</div>
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🎉 &nbsp; Upstage AI 인턴 합격!</div>
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🎉 &nbsp; SBS 마부작침 데이터 저널리스트 인턴 합격!</div>
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🎉 &nbsp; YTN 데이터 저널리스트 인턴 합격!</div>
                <div class="rounded-md bg-zinc-900 text-center py-4 text-slate-400">🎉 &nbsp; 정부 공공 빅데이터 인턴십 합격! (3인)</div>
            </div>

            <div class="text-white font-medium text-lg pb-2">문의</div>
            <div class="text-slate-400 pb-8">
                <div class="pb-2">· 이메일 : <a class="underline" href="mailto:mail@cosadama.com">mail@cosadama.com</a></div>
                <div class="pb-2">· 카카오톡 : <a class="underline" href="https://pf.kakao.com/_MYkvK" target="blank">COSADAMA</a> </div>
                <div class="text-sm text-slate-500"> <a class="underline" href="https://www.instagram.com/cosadama/" target="blank">인스타그램</a>을 팔로우하시면 보다 빠르게 코사다마의 소식을 받아보실 수 있습니다.</div>
            </div>

            <div class="bg-transparent block md:inline-block hover:bg-zinc-900 rounded-lg py-4 pl-5 pr-6 transition hover:duration-200">
                <nuxt-link :to="{path: '/recruit'}" class="text-white text-base flex items-center justify-center">
                    <Left class="w-5 h-5" /> <span class="pl-1">모집 공고 리스트로 돌아가기</span>
                </nuxt-link>
            </div>

        </div>

<!-- 지원 탭  -->
        <aside class="hidden md:block text-white w-1/3 pl-3">
            <ul class="divide-y pb-6">
                <li class="pb-3 pt-1 text-slate-400 text-lg px-1"> <span class="w-1/3 inline-block">활동 형태</span>  <span class="text-white">{{recruit.type}}</span> </li>
                <li class="py-3 text-slate-400 text-lg px-1"> <span class="w-1/3 inline-block">활동 기간</span> <span class="text-white">{{recruit.period}}</span> </li>
                <li class="py-3 text-slate-400 text-lg px-1"> <span class="w-1/3 inline-block">모집 현황</span> <span class="text-white">{{recruit.status}}</span> </li>
            </ul>
            <a :href="`${recruit.applyLink}`" class="w-full rounded-lg bg-zinc-800 text-center flex items-center justify-center py-3.5 hover:bg-zinc-700 transition hover:duration-300">
            지원하기
            </a>
        </aside>
    </div>

    </div>
</template>

<script>
export default {
    async asyncData({ $content, params }) {
        const recruit = await $content('recruit', params.slug)
        .fetch();

        return { recruit }
    },

    head() {
        return {
            title: `${this.recruit.title} | COSADAMA`,
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
            content: `${this.recruit.title} | COSADAMA`
            },
            {
            hid: 'og:description',
            property: 'og:description',
            content: this.recruit.status
            },
            {
            hid: 'og:image',
            property: 'og:image',
            // content: this.article.img
            content: `https://raw.githubusercontent.com/Team-COSADAMA/COSADAMA/main/static/${this.recruit.img}`
            },
            {
            hid: 'og:image:secure_url',
            property: 'og:image:secure_url',
            content: `https://raw.githubusercontent.com/Team-COSADAMA/COSADAMA/main/static/${this.recruit.img}`
            },
            {
            hid: 'og:image:alt',
            property: 'og:image:alt',
            content: 'article image'
            },
            {
            hid: 'og:url',
            name: 'og:url',
            content: `https://cosadama.com/recuit/${this.$route.params.slug}`
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
.square-box {
    overflow: hidden;
}
.profile {
    object-fit: cover;
    /* overflow: hidden; */
}
</style>