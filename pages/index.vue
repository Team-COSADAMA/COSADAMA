<template>
<div class="w-full">
  <div class="z-0 bg-img section h-content" style="background-image: url(picture3.jpg)">

    <div class="mx-auto max-w-7xl px-10">
      <div class="text-white text-6xl pt-72 mb-8 font-medium drop-shadow-md">Welcome to the Community, <br /> Where We All Can Code.</div>
      <div class="text-slate-300 text-xl md:text-2xl mb-32 drop-shadow">코사다마는 중앙대학교의 비전공자 코딩 커뮤니티입니다.</div>

      <div class="text-4xl text-white mb-7 font-medium">Recruiting Now</div>
      <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-10 mb-24">
        <div class="rounded-lg h-96 section bg-img group" style="background-image: url(team1.jpg)">
          <div class="rounded-lg w-full h-full bg-gradient-to-t from-gray-700">
            <div class="px-11 py-10 absolute bottom-0 drop-shadow-2xl text-white text-4xl font-semibold leading-10 keep-all"> 코딩 자체를 <br/> 처음 접해보신다면
            <br/> <span class="text-lg text-white font-normal group-hover:underline">일반 멤버로 지원하기</span><span class="text-sm text-slate-300 font-normal"> (~ 03.05)</span> </div>
          </div>
          <!-- <div class="px-11 py-10 absolute bottom-0 drop-shadow-2xl text-white text-4xl font-semibold"> 코딩 자체를 <br/> 처음 접해보신다면 </div> -->
          <!-- <div class="h-1/3 w-full absolute bottom-0 bg-black opacity-50 px-6 py-4">
            <div class="text-white text-semibold text-2xl opacity-100">Zero Base</div>
          </div> -->
        </div>
        <div class="rounded-lg h-96 section bg-img" style="background-image: url(team3.jpeg)">
          <div class="rounded-lg w-full h-full bg-gradient-to-t from-gray-700 group">
            <div class="px-11 py-10 absolute bottom-0 drop-shadow-xl text-white text-4xl font-semibold keep-all"> 파이썬을 제외한 <br/> 언어에 능숙하시다면 
            <br/> <span class="text-lg text-white font-normal group-hover:underline">커리큘럼 개발 멤버로 지원하기</span><span class="text-sm text-slate-300 font-normal"> (상시모집)</span> </div>
          </div>
          <!-- <div class="px-11 py-10 absolute bottom-0 drop-shadow-xl text-white text-4xl font-semibold"> 파이썬을 제외한 <br/> 언어에 능숙하시다면  </div> -->
          <!-- <div class="h-1/3 w-full absolute bottom-0 bg-black opacity-50 px-6 py-4">
            <div class="text-white text-semibold text-2xl opacity-100">Zero Base</div>
          </div> -->
        </div>
      </div>
    </div>

<!-- Carousel  -->

      <div class="mx-auto max-w-7xl mb-24 px-10">
        <div class="text-4xl text-white mb-7 font-medium">Reviews</div>
        <div>
            <VueSlickCarousel v-bind="settings">
              <div v-for="review of memberReviews" :key="review">
                <div class="flex justify-center mb-10 pt-8">
                  <div class="lead-box h-28 w-28">
                    <img :src="require(`~/assets/image/members/${review.img}`)" alt="" class="profile">
                  </div>
                </div>

                <div class="text-white text-center text-lg px-14 keep-all mb-4">{{review.review}}</div>

                <div class="text-base text-slate-400 text-center">{{review.status}}, {{review.name}}님</div>

              </div>
            </VueSlickCarousel>
        </div>

      </div>




    <div class="mx-auto max-w-7xl px-10">

<!-- Keynotes  -->
      <div class="text-4xl text-white mb-7 font-medium">Keynotes</div>
      <div class="flex grid-cols-2 gap-x-8 mb-24">
        <iframe class="rounded-lg w-1/2 h-96" src="https://www.youtube.com/embed/L3i_Rng3i5s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <iframe class="rounded-lg w-1/2 h-96" src="https://www.youtube.com/embed/kQ_cynq0Yik" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>

<!-- Community -->
      <div class="text-4xl text-white mb-14 font-medium">Values</div>
      <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 gap-x-8 pb-24">
        <div class="h-content">
          <div class="text-2xl text-white font-semibold mb-3">함께하는 성장</div>
          <div class="text-lg text-slate-400 keep-all">혼자만의 성장이 아닌, 함께하는 성장을 지향합니다. 앎을 나누고, 함께 결과물을 만들어가는 과정에서 모두가 가파른 성장을 이뤄낼 수 있습니다.</div>
        </div>
        <div class="h-content">
          <div class="text-2xl text-white font-semibold mb-3">자율적인 참여</div>
          <div class="text-lg text-slate-400 keep-all">코사다마는 커뮤니티입니다. 어떠한 강제도 없이, 오롯이 본인이 배움의 속도를 조절합니다. 힘이 넘칠 때는 빠르게, 지칠 때는 조금씩 쉬어가도 좋습니다.</div>
        </div>
        <div class="h-content">
          <div class="text-2xl text-white font-semibold mb-3">모두를 위한 개발</div>
          <div class="text-lg text-slate-400 keep-all">Write Codes for Rights! 초기 코사다마의 슬로건입니다. 누구도 소외되지 않는, 모두를 위한 개발을 목표로 합니다.  </div>
        </div>
      </div>

      <!-- <div class="text-4xl text-white mb-7 font-medium">Our Moments</div>
      <div class="flex grid-cols-2 gap-x-8 mb-24">
        <div class="border border-slate-300 rounded-lg w-1/2 h-96">Thing1</div>
        <div class="border border-slate-300 rounded-lg w-1/2 h-96">Thing2</div>
      </div>

      <div class="text-4xl text-white mb-7 font-medium">Our Moments</div>
      <div class="flex grid-cols-2 gap-x-8 pb-24">
        <div class="border border-slate-300 rounded-lg w-1/2 h-96">Thing1</div>
        <div class="border border-slate-300 rounded-lg w-1/2 h-96">Thing2</div>
      </div> -->

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