<template>
  <div class="blocks">
    <div class="blocks-content">
        <div class="blocks-left">
            <div class="blocks-four">
                <div class="blocks-box" v-for="(repeat, i) in blocks" :key="i">
                    <a :href="blocks_link[i]">
                    <div class="blocks-box-child">
                        <img :src="require(`../assets/icon/${blocks_img[i]}`)" class="blocks-img" />
                        <br />
                        {{blocks[i]}}
                    </div>
                    </a>
                </div>
            </div>
        </div>
        <div class="blocks-right">
            <div class="subtitle">
                무료로 TOPIK 시험 준비하세요
            </div>
            <div class="sec-block">
                <div class="desc" v-for="(repeat, i) in desc" :key="i">
                    <div class="align">
                        <div class="subtitle-img"></div>
                        {{desc[i]}}
                    </div>
                </div>
            </div>
            <a href="/">
                <div class="border">
                    무료 토픽 풀기
                    <div class="arrow-img"></div>
                </div>
            </a>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    msg: String
  },
  data() {
      return {
            desc: [
                '실전 TOPIK 문제를 무제한으로 풀어보세요',
                '듣기/읽기/쓰기 부족한 영역만 선택해서 풀 수 있어요',
                '시험 결과 분석을 바탕으로 튜터를 추천해 드려요'
                ],
            blocks: [
                '미니 TOPIK',
                '모의 TOPIK',
                '시험 분석',
                'TUTOR 매칭'
            ],
            blocks_img: [
                '미니TOPIK_icon.png',
                '모의TOPIK_icon.png',
                '시험분석_icon.png',
                'TUTOR매칭_icon.png'
            ],
            blocks_link: [
                '/',
                '/',
                '/',
                '/',
            ]
        }
  }
}
</script>

<style scoped>

a {
    text-decoration: none;
    color: black;
}

.blocks {
    width: 100%;
    display: flex;
    justify-content: center;
    text-align: center;
}

.blocks-img {
    width: 45px;
    height: 45px;
}

.blocks-content {
    width: 950px;
    display: flex;
    height: 420px;
    justify-content: space-between;
    align-items: center;
}

.blocks-box {
    display: inline-block;
    width: 130px;
    height: 130px;
    margin: 15px;
    border-radius: 25px;
    border: 1px solid rgb(230, 230, 230);
    box-shadow: 5px 10px 20px 5px rgb(230, 230, 230);
}

.subtitle-img {
    background-image: url('../assets/check.png');
    width: 28px;
    height: 28px;
    background-size: 100%;
    background-repeat: no-repeat;
}

.blocks-box-child {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    font-size: 13px;
}

.blocks-left {
    width: 350px;
    height: 350px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.blocks-right {
    width: 450px;
    height: 250px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    text-align: left;
}

.subtitle {
    font-weight: 700;
    font-size: 33px;
}

.align {
    display: flex;
    align-items: center;
}

.arrow-img {
    background-image: url('../assets/todown.png');
    width: 15px;
    height: 15px;
    background-size: 100%;
    background-repeat: no-repeat;
    margin-left: 10px;
}

.subtitle-img {
    display: inline-block;
    margin-right: 5px;
}

.desc {
    display: flex;
    flex-direction: row;
    align-items: center;
}

.sec-block {
    font-size: 15px;
    font-weight: 500;
    color: gray;
}

.border {
    border: 1px solid rgb(167, 167, 167);
    border-radius: 25px;
    width: 180px;
    display: flex;
    align-items: center;
    justify-content: center;
    padding-top: 12px;
    padding-bottom: 12px;
}

</style>
