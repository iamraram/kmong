<template>
  <div class="img">
      <div class="main-title">
          나를 위한 시간 30분 <br/> 1:1 한국어 수업!
      </div>
      <br />
      <div class="sub-title">
          일상 한국어부터 TOPIK 시험 대비, 논문 첨삭, 주제 토론까지 <br /> YalliYalli에서 모두 경험하세요.
      </div>
  </div>
</template>

<script>
export default {
  name: 'Mainimg',
  props: {
    msg: String
  },
  data() {
      return {

      }
  }
}
</script>

<style scoped>

.main-title {
    font-size: 33px;
    font-weight: 700;
    line-height: 48px;
}

.sub-title {
    line-height: 28px;
}

.img {
    background-image: url('../assets/main-img.png');
    width: 100%;
    height: 350px;
    background-size: 100%;
    background-repeat: no-repeat;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    line-height: 30px;
    position: relative;
}

@media screen and (max-width: 768px) {
    .img {
        padding: 20px;
        height: 270px;
        justify-content: center;
        align-items: flex-start;
        text-align: left;
    }

    .main-title {
        font-size: 25px;
        line-height: 35px;
    }

    .sub-title {
        width: 220px;
        font-size: 16px;
        line-height: 25px;
    }
}

</style>
