<template>
<div class="w-full">
  <div class="z-0 bg-img section h-content" style="background-image: url(picture3.jpg)">

    <div class="mx-auto max-w-7xl px-6 md:px-10 fadeinupcom">
      <div class="mt-36 md:mt-60 text-sm md:text-base top-gradient font-medium">A B O U T</div>
      <div class="text-white text-4xl md:text-6xl pt-3 mb-7 font-medium drop-shadow-md">Welcome to the Community, <br class="hidden sm:inline md:inline" /> Where We All Can Code.</div>
      <div class="text-slate-300 text-base md:text-xl md:text-2xl mb-20 md:mb-32 drop-shadow">코사다마는 중앙대학교의 <br class="inline md:hidden" /> 비전공자 코딩 커뮤니티입니다.</div>

      <div class="pb-2.5 text-sm md:text-base recruiting-gradient font-medium">R E C R U I T</div>
      <div class="text-2xl md:text-3xl pb-5 md:pb-7 text-white font-medium">Now Recruiting</div>
      <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-8 mb-12 md:mb-24">
        <div class="rounded-lg h-80 md:h-96 section bg-img group" :style="{ backgroundImage: `url(/${recruits[0].img})` }" >
          <nuxt-link :to="{path: `/recruit/${recruits[0].slug}`}" class="block rounded-lg w-full h-full bg-gradient-to-t from-gray-700">
            <div class="px-6 md:px-11 py-6 md:py-10 absolute bottom-0 drop-shadow-xl text-white">
              <div class="text-2xl md:text-3xl font-semibold keep-all">{{recruits[0]["promotion"]}}</div>
              <div class="pt-2">
                <span class="text-base md:text-lg text-white font-normal group-hover:underline keep-all">{{recruits[0]["title"]}}로 지원하기</span>
                <span class="text-xs md:text-sm text-slate-300 font-normal pl-0.5 keep-all"> {{recruits[0]["status"]}}</span> 
              </div>
            </div>
          </nuxt-link>
        </div>
        <div class="rounded-lg h-80 md:h-96 section bg-img" :style="{ backgroundImage: `url(/${recruits[1].img})` }">
          <nuxt-link :to="{path: `/recruit/${recruits[0].slug}`}" class="block rounded-lg w-full h-full bg-gradient-to-t from-gray-700 group">
            <div class="px-6 md:px-11 py-6 md:py-10 absolute bottom-0 drop-shadow-xl text-white">
              <div class="text-2xl md:text-3xl font-semibold keep-all">{{recruits[1]["promotion"]}}</div>
              <div class="pt-2">
                <span class="text-base md:text-lg text-white font-normal group-hover:underline keep-all">{{recruits[1]["title"]}}로 지원하기</span>
                <span class="text-xs md:text-sm text-slate-300 font-normal pl-0.5 keep-all"> {{recruits[1]["status"]}}</span> 
              </div>
            </div> 
          </nuxt-link>
        </div>
        <div class="bg-black rounded-lg block md:hidden border border-white drop-shadow-md hover:bg-zinc-800">
          <nuxt-link class="flex items-center h-12" :to="{path: '/recruit'}">
            <div class="text-slate-50 text-base font-medium mx-auto">더 많은 공고 보기</div>
          </nuxt-link>
        </div>
      </div>
    </div>

      <div class="mx-auto max-w-7xl mb-12 md:mb-24 px-6 md:px-10 fadeinupcom">
        <div class="pb-2.5 text-sm md:text-base review-gradient font-medium">F E E D B A C K</div>
        <div class="text-2xl md:text-3xl mb-5 md:mb-7 font-medium text-white">Members' Review</div>
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




    <div class="mx-auto max-w-7xl px-6 md:px-10 fadeinupcom">

<!-- Keynotes  -->
      <div class="pb-2.5 text-sm md:text-base videos-gradient font-medium">V I D E O S</div>
      <div class="text-2xl md:text-3xl text-white mb-5 md:mb-7 font-medium">Keynotes</div>
      <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-6 mb-16 md:mb-24">
        <iframe class="rounded-lg w-full md:w-content h-60 sm:h-80 md:h-96" src="https://www.youtube.com/embed/L3i_Rng3i5s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <iframe class="rounded-lg w-full md:w-content h-60 sm:h-80 md:h-96" src="https://www.youtube.com/embed/kQ_cynq0Yik" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>

<!-- Values -->
      <div class="pb-2.5 text-sm md:text-base value-gradient font-medium">V A L U E S</div>
      <div class="text-2xl md:text-3xl text-white mb-6 md:mb-14 font-medium">What We Value</div>
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
    async asyncData({ $content }) {
        const memberReviews = await $content('memberReviews')
        .sortBy('order')
        .fetch();
        const recruits = await $content('recruit')
        .sortBy('order')
        .limit(2)
        .fetch();
        return { memberReviews, recruits }
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

<style>
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
.top-gradient{
    position: relative;
    display: inline-block;
    align-items: center;
    justify-content: center;
    color: #79c0ff;
    font-weight: 600;
    line-height: 1;
    background: linear-gradient(92.7deg,#56d364 -1.37%,#79c0ff 78.71%);
    -webkit-background-clip: text;
    background-clip: text;
    border-radius: 6px;
    transition: .25s;
    -webkit-text-fill-color: transparent;
}
.recruiting-gradient{
    position: relative;
    display: inline-block;
    align-items: center;
    justify-content: center;
    color: #79c0ff;
    font-weight: 500;
    line-height: 1;
    background: linear-gradient(90deg, rgb(255, 248, 85) 0.04%, rgb(70, 227, 183) 100.04%);
    -webkit-background-clip: text;
    background-clip: text;
    border-radius: 6px;
    transition: .25s;
    -webkit-text-fill-color: transparent;
}
.review-gradient{
    position: relative;
    display: inline-block;
    align-items: center;
    justify-content: center;
    color: #79c0ff;
    font-weight: 500;
    line-height: 1;
    background: linear-gradient(285.49deg, rgb(245, 55, 249) -14.61%, rgb(247, 190, 43) 106.06%);
    -webkit-background-clip: text;
    background-clip: text;
    border-radius: 6px;
    transition: .25s;
    -webkit-text-fill-color: transparent;
}
.videos-gradient{
    position: relative;
    display: inline-block;
    align-items: center;
    justify-content: center;
    color: #79c0ff;
    font-weight: 500;
    line-height: 1;
    background: linear-gradient(124.31deg, rgb(70, 227, 183) 0.18%, rgb(82, 124, 172) 89.2%);
    -webkit-background-clip: text;
    background-clip: text;
    border-radius: 6px;
    transition: .25s;
    -webkit-text-fill-color: transparent;
}
.value-gradient{
    position: relative;
    display: inline-block;
    align-items: center;
    justify-content: center;
    color: #79c0ff;
    font-weight: 500;
    line-height: 1;
    background: linear-gradient(285.49deg, rgb(148, 151, 157) -14.61%, rgb(118, 124, 175) 106.06%);
    -webkit-background-clip: text;
    background-clip: text;
    border-radius: 6px;
    transition: .25s;
    -webkit-text-fill-color: transparent;
}

.fadeinupcom {
  animation: fadeinup 0.8s;
}

@keyframes fadeinup {
  0% {
    opacity: 0;
    -webkit-transform: translateY(100px);
    transform: translateY(100px);
  }
  100% {
      opacity: 1;
      -webkit-transform: translateY(0);
      transform: translateY(0);
  }
}
</style>