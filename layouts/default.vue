<template>
  <div class="rel">
    <Header class="fix" />
    <Nuxt />
    <FooterFull />
  </div>
</template>

<style>
  /* @import url('https://cdn.jsdelivr.net/gh/orioncactus/pretendard/dist/web/static/pretendard.css'); */
  /* * { font-family: Pretendard, -apple-system, BlinkMacSystemFont, system-ui, Roboto, 'Helvetica Neue', 'Segoe UI', 'Apple SD Gothic Neo', 'Noto Sans KR', 'Malgun Gothic', sans-serif;; } */
  @import url(~/assets/css/pretendard-subset.css);
  * { 
    /* font-family: 'Inter', 'Spoqa Han Sans Neo', 'sans-serif'; */
    font-family: Pretendard, 'Pretendard', -apple-system, 'sans-serif';
    word-wrap: break-word;
    word-break: keep-all;
    }
  .rel{
    position: relative;
  }
  .fix{
    position: fixed;
  }
</style>

<script>
</script>