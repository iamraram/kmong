<template>
  <div class="blocks">
    <div class="block-child">

        <div class="block-children">
            <div class="top">
                <div class="subtitle">
                    한글부터 차근차근, 모국어로 쉽게 시작하세요
                </div>
                <div class="small">
                    <b>01</b> / 05
                </div>
            </div>
            <div class="videos">
                <div class="videos-child" v-for="(repeat, i) in 4" :key="i">
                    <div class="somenail-img"></div>
                    <div class="video-title">
                        {{your_lang[i].title}}
                    </div>
                    <div class="tutor-info">
                        <div class="parent">
                            <div class="tutor-views imgs"></div>
                            {{your_lang[i].views}}
                        </div>
                        <div class="parent">
                            <div class="tutor-likes imgs"></div>
                            {{your_lang[i].likes}}
                        </div>
                        <div class="parent">
                            <div class="tutor-goods imgs"></div>
                            {{your_lang[i].goods}}
                        </div>
                    </div>
                    <div class="tutor-stars">
                        <div class="star" v-for="(repeat, i) in 5" :key="i"></div>
                        {{your_lang[i].stars}}
                    </div>
                </div>
            </div>
        </div>

        <div class="block-children">
            <div class="top">
                <div class="subtitle">
                    다양한 콘텐츠를 '<div class="img-youtube" />' 에서 확인하세요
                </div>
                <div class="small">
                    <b>01</b> / 05
                </div>
            </div>
            <div class="videos">
                <div class="videos-child2" v-for="(repeat, i) in 4" :key="i">
                    <div class="somenail-img2"></div>
                    <div class="video-title">
                        {{youtube[i].title}}
                    </div>
                    <div class="you">
                        <div class="you-child">
                            조회수 {{youtube[i].views}}회
                        </div>
                        <div class="you-child">
                            2주 전
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </div>
  </div>
</template>

<style scoped>

.video-title {
    text-align: left;
    line-height: 25px;
    height: 45px;
}

.you {
    display: flex;
    font-size: 15px;
    color: rgb(160, 160, 160);
    margin-top: 12px;
}

.you-child:first-child {
    margin-right: 30px;
}

.tutor-info {
    padding-bottom: 10px;
    border-bottom: 1px solid rgb(187, 187, 187);
}

.block-children:last-child {
    margin-top: 95px;
}

.tutor-stars {
    display: flex;
    align-items: center;
}

.star {
    background-image: url('../assets/stars.png');
    width: 16px;
    height: 16px;
    background-size: 100%;
    background-repeat: no-repeat;
}

.star:last-child {
    margin-right: 5px;
}

.img-youtube {
    background-image: url('../assets/youtube.png');
    width: 120px;
    height: 28px;
    background-size: 100%;
    background-repeat: no-repeat;
    display: inline-block;
}

.somenail-img {
    background-image: url('../assets/somenail.png');
    width: 285.7px;
    height: 160px;
    background-size: 100%;
    background-repeat: no-repeat;
    border: 1px solid rgb(233, 233, 233);
    border-radius: 15px;
}

.somenail-img2 {
    background-image: url('../assets/somenail2.png');
    width: 285.7px;
    height: 160px;
    background-size: 100%;
    background-repeat: no-repeat;
    border: 1px solid rgb(233, 233, 233);
    border-radius: 15px;
}

.videos-child {
    width: 285px;
    height: 310px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
}

.videos-child2 {
    width: 285px;
    height: 270px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
}

.tutor-info {
    display: flex;
    justify-content: flex-start;
    font-size: 13px;
    font-weight: 600;
    text-align: center;
    color: rgb(133, 133, 133);
}

.parent {
    justify-content: center;
    display: flex;
}

.parent:nth-child(2) {
    margin-left: 10px;
    margin-right: 10px;
}

.tutor-views {
    background-image: url('../assets/views.png');
    width: 18px;
    height: 18px;
    background-size: 100%;
    background-repeat: no-repeat;
    position: relative;
    top: 1px;
}

.tutor-likes {
    background-image: url('../assets/likes.png');
    width: 18px;
    height: 18px;
    background-size: 100%;
    background-repeat: no-repeat;
    position: relative;
    top: 1px;
}

.tutor-goods {
    background-image: url('../assets/goods.png');
    width: 18px;
    height: 18px;
    background-size: 100%;
    background-repeat: no-repeat;
    position: relative;
    top: 1px;
}


.videos {
    margin-top: 40px;
    display: flex;
    width: 100%;
    justify-content: space-between;
}

a {
    text-decoration: none;
    color: black;
}

.top {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.blocks {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 1100px;
    position: relative;
}

.block-child {
    width: 1200px;
    height: 82%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.block-children {
    width: 1200px;
}

.subtitle {
    font-weight: 700;
    font-size: 33px;
}

@media screen and (max-width: 768px) {
    .subtitle {
        font-size: 18px;
        text-align: left;
        font-weight: 700;
        line-height: 45px;
    }

    .block-children {
        width: 100%;
    }

    .videos-child:first-child {
        margin-left: 0;
    }

    .blocks {
        height: 800px;
        justify-content: flex-start;
        align-items: flex-start;
    }

    .block-children:last-child {
        margin-top: 40px;
    }

    .videos {
        overflow: scroll;
    }

    ::-webkit-scrollbar {
        display: none;
    }

    .right-box {
        overflow-x: scroll;
    }

    .img-youtube {
        width: 90px;
        height: 22px;
        align-items: center;
    }

    .videos-child,
    .videos-child2 {
        margin-left: 8px;
        margin-right: 8px;
    }

    .videos {
        margin-top: 5px;
    }

    .top {
        width: 100%;
    }

    .videos {
        width: 100%;
    }

    .somenail-img,
    .somenail-img2 {
        width: 140px;
        height: 110px;
        background-size: 150%;
    }
    
    .small {
        display: none;
    }

    .block-child {
        padding: 20px;
        width: 100%;
    }

    .tutor-info {
        margin-top: 25px;
    }

    .you {
        font-size: 12px;
    }
}

</style>

<script>
export default {
  name: 'Videos',
  props: {
    msg: String
  },
  data() {
      return {
          your_lang: [
              {
                title: '[Korean_1/300] Introduction to the korean Alpabet',
                img_src: '/',
                views: 5500,
                likes: 50,
                goods: 30,
                stars: '5.0'
              },
              {
                title: '[Korean_1/300] Introduction to the korean Alpabet',
                img_src: '/',
                views: 33,
                likes: 33,
                goods: 33,
                stars: '5.0'
              },
              {
                title: '[Korean_1/300] Introduction to the korean Alpabet',
                img_src: '/',
                views: 11,
                likes: 11,
                goods: 11,
                stars: '5.0'
              },
              {
                title: '[Korean_1/300] Introduction to the korean Alpabet',
                img_src: '/',
                views: 5500,
                likes: 50,
                goods: 30,
                stars: '5.0'
              }
          ],
          youtube: [
              {
                title: '딱 1분만 집중해서 들어봐. 딱 1분만 집중해서 들어봐.',
                img_src: '/',
                views: 5500,
              },
              {
                title: '우리는 밥을 먹잖아? 우리는 밥을 먹잖아?',
                img_src: '/',
                views: 5500,
              },
              {
                title: '딱 1분만 집중해서 들어봐.',
                img_src: '/',
                views: 5500,
              },
              {
                title: '우리는 밥을 먹잖아?',
                img_src: '/',
                views: 5500,
              }
          ],
      }
  }
}
</script>