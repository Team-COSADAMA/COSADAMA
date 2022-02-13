<template>
<div class="w-full">
  <div class="z-0 bg-img section h-content" style="background-image: url(picture3.jpg)">

    <div class="mx-auto max-w-7xl px-6 md:px-10">
      <div class="text-white text-4xl md:text-6xl pt-40 md:pt-72 mb-8 font-medium drop-shadow-md">Welcome to the Community, <br class="hidden sm:inline md:inline" /> Where We All Can Code.</div>
      <div class="text-slate-300 text-base md:text-xl md:text-2xl mb-20 md:mb-32 drop-shadow">코사다마는 중앙대학교의 <br class="inline md:hidden" /> 비전공자 코딩 커뮤니티입니다.</div>

      <div class="text-3xl md:text-4xl text-white mb-5 md:mb-7 font-medium">Now Recruiting</div>
      <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-8 mb-12 md:mb-24">
        <div class="rounded-lg h-80 md:h-96 section bg-img group" style="background-image: url(team3.jpeg)">
          <nuxt-link :to="{path: '/recruit/member-2022-01'}" replace class="block rounded-lg w-full h-full bg-gradient-to-t from-gray-700">
            <div class="px-6 md:px-11 py-6 md:py-10 absolute bottom-0 drop-shadow-2xl text-white text-3xl md:text-4xl font-semibold leading-9 md:leading-10 keep-all"> 코딩 자체를 <br/> 처음 접해보신다면
            <br/> <span class="text-base md:text-lg text-white font-normal group-hover:underline">일반 멤버로 지원하기</span><span class="text-xs md:text-sm text-slate-300 font-normal pl-0.5"> 3월 4일까지</span> </div>
          </nuxt-link>
        </div>
        <div class="rounded-lg h-80 md:h-96 section bg-img" style="background-image: url(team4.jpg)">
          <nuxt-link :to="{path: '/recruit/curriculum-member'}" replace class="block rounded-lg w-full h-full bg-gradient-to-t from-gray-700 group">
            <div class="px-6 md:px-11 py-6 md:py-10 absolute bottom-0 drop-shadow-xl text-white text-3xl md:text-4xl font-semibold keep-all"> 파이썬을 제외한 <br/> 언어에 능숙하시다면 
            <br/> <span class="text-base md:text-lg text-white font-normal group-hover:underline">커리큘럼 개발 멤버로 지원하기</span><span class="text-xs md:text-sm text-slate-300 font-normal pl-0.5"> 추후 모집 예정</span> </div>
          </nuxt-link>
        </div>
        <div class="bg-black rounded-lg block md:hidden border border-white drop-shadow-md hover:bg-zinc-800">
          <nuxt-link class="flex items-center h-12" :to="{path: '/recruit'}" replace>
            <div class="text-slate-50 text-base font-medium mx-auto">더 많은 공고 보기</div>
          </nuxt-link>
        </div>
      </div>
    </div>

<!-- Carousel  -->

      <div class="mx-auto max-w-7xl mb-12 md:mb-24 px-6 md:px-10">
        <div class="text-3xl md:text-4xl text-white mb-5 md:mb-7 font-medium">Reviews</div>
        <div>
            <VueSlickCarousel v-bind="settings">
              <div v-for="review of memberReviews" :key="review">
                <div class="flex justify-center mb-5 md:mb-10 pt-3 md:pt-8">
                  <div class="lead-box h-20 md:h-28 w-20 md:w-28">
                    <img :src="require(`~/assets/image/members/${review.img}`)" alt="" class="profile">
                  </div>
                </div>

                <div class="text-white text-center text-base md:text-lg px-2 md:px-14 keep-all mb-2 md:mb-4">{{review.review}}</div>

                <div class="text-sm md:text-base text-slate-400 text-center">{{review.status}}, {{review.name}}님</div>

              </div>
            </VueSlickCarousel>
        </div>

      </div>




    <div class="mx-auto max-w-7xl px-6 md:px-10">

<!-- Keynotes  -->
      <div class="text-3xl md:text-4xl text-white mb-5 md:mb-7 font-medium">Keynotes</div>
      <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-6 mb-16 md:mb-24">
        <iframe class="rounded-lg w-full md:w-content h-60 sm:h-80 md:h-96" src="https://www.youtube.com/embed/L3i_Rng3i5s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <iframe class="rounded-lg w-full md:w-content h-60 sm:h-80 md:h-96" src="https://www.youtube.com/embed/kQ_cynq0Yik" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>

<!-- Values -->
      <div class="text-3xl md:text-4xl text-white mb-6 md:mb-14 font-medium">Values</div>
      <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 gap-x-8 gap-y-6 pb-16 md:pb-24">
        <div class="h-content">
          <div class="text-xl md:text-2xl text-white font-semibold mb-2 md:mb-3">함께하는 성장</div>
          <div class="text-base md:text-lg text-slate-400 keep-all">혼자만의 성장이 아닌, 함께하는 성장을 지향합니다. 앎을 나누고, 함께 결과물을 만들어가는 과정에서 모두가 가파른 성장을 이뤄낼 수 있습니다.</div>
        </div>
        <div class="h-content">
          <div class="text-xl md:text-2xl text-white font-semibold mb-2 md:mb-3">자율적인 참여</div>
          <div class="text-base md:text-lg text-slate-400 keep-all">코사다마는 커뮤니티입니다. 어떠한 강제도 없이, 오롯이 본인이 배움의 속도를 조절합니다. 힘이 넘칠 때는 빠르게, 지칠 때는 조금씩 쉬어가도 좋습니다.</div>
        </div>
        <div class="h-content">
          <div class="text-xl md:text-2xl text-white font-semibold mb-2 md:mb-3">모두를 위한 개발</div>
          <div class="text-base md:text-lg text-slate-400 keep-all">Write Codes for Rights! 초기 코사다마의 슬로건입니다. 누구도 소외되지 않는, 모두를 위한 개발을 목표로 합니다.  </div>
        </div>
      </div>

    </div>

    <!-- <iframe class="max-w-3xl mx-auto rounded-xl mb-10" src="https://open.spotify.com/embed/playlist/37i9dQZF1DWWsrfifmSJ1r?utm_source=generator" width="100%" height="380" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"></iframe> -->
  </div>
</div>
</template>

<script>
  import VueSlickCarousel from 'vue-slick-carousel'
  import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  // optional style for arrows & dots
  import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
  export default {
    name: 'Slider',
    components: { VueSlickCarousel },
    async asyncData({ $content, params }) {
        const memberReviews = await $content('memberReviews', params.id)
        .sortBy('order')
        .fetch();
        return { memberReviews }
    },
  data() {
    return {
      settings: {
      "dots": false,
      "arrows": false,
      "dotsClass": "slick-dots custom-dot-class",
      "edgeFriction": 0.35,
      "infinite": true,
      "speed": 1000,
      "slidesToShow": 1,
      "slidesToScroll": 1,
      "autoplay" : true,
      "autoplaySpeed" : 5000
    }
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