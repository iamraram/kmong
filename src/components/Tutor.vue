<template>
  <div class="tutor-content">
    <div class="main-content">
        <div class="left-box">
            <div class="title">
                이 튜터 어때요? <br/>
                최근 많은 튜티들이<br/>
                예약했어요.
            </div>
            <div class="title2">
                이 튜터 어때요? 최근 많은 튜티들이 예약했어요.
            </div>
            <div class="len">
                <b>01</b> / 05
            </div>
            <a href="/" class="none_2">
                <div class="border">
                    튜터 만나러 가기
                    <div class="arrow-img"></div>
                </div>
            </a>
        </div>
        <div class="right-box">
            <div class="tutor-box" v-for="(repeat, i) in 3" :key="i">
                <div class="top">
                    <div class="top-content">
                        <img :src="require('../assets/profile_img/profile.png')" class="tutor-img">
                        <div class="tutor-name">
                            {{tutor[i].name}}
                        </div>
                        <div class="tutor-level">
                            Specialty Level: {{tutor[i].specialty}}
                        </div>
                        <div class="tutor-stars">
                            <div class="star" v-for="(repeat, i) in 5" :key="i"></div>
                            {{tutor[i].stars}}
                        </div>
                    </div>
                </div>
                <div class="bottom">
                    <div class="bottom-content">
                        <div class="tutor-intoduce">
                            {{tutor[i].introduce}}
                        </div>
                        <div class="tutor-info">
                            <div class="parent">
                                <div class="tutor-views imgs"></div>
                                {{tutor[i].views}}
                            </div>
                            <div class="parent">
                                <div class="tutor-likes imgs"></div>
                                {{tutor[i].likes}}
                            </div>
                            <div class="parent">
                                <div class="tutor-goods imgs"></div>
                                {{tutor[i].goods}}
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <a href="/" class="none_1">
            <div class="border">
                튜터 만나러 가기
                <div class="arrow-img"></div>
            </div>
        </a>
        <div class="arrow-img2"></div>
    </div>
  </div>
</template>

<style scoped>

.tutor-img {
    width: 60px;
    height: 60px;
    border-radius: 40px;
}

.parent {
    display: flex;
}

.parent:nth-child(2) {
    margin-left: 10px;
    margin-right: 10px;
}

.imgs {
    margin-right: 3px;
}

.tutor-info {
    display: flex;
    justify-content: center;
    font-size: 13px;
    font-weight: 600;
    text-align: center;
    color: rgb(133, 133, 133);
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

.tutor-level {
    color: rgb(95, 125, 233)
}

a {
    text-decoration: none;
    color: black;
}

.title {
    text-align: left;
    font-weight: 700;
    font-size: 33px;
    line-height: 45px;
}

.tutor-intoduce {
    font-size: 13px;
}

.tutor-name {
    font-weight: 600;
}

.tutor-stars {
    display: flex;
}

.star {
    background-image: url('../assets/stars.png');
    width: 16px;
    height: 16px;
    background-size: 100%;
    background-repeat: no-repeat;
}

 

.tutor-box {
    display: inline-block;
    height: 100%;
    width: 100%;
    border: 1px solid rgb(230, 230, 230);
    background-color: rgb(249, 249, 250);
    border-radius: 15px;
    margin-left: 10px;
    margin-right: 10px;
    box-shadow: 1px 1px 10px 1px rgb(230, 230, 230);
    text-align: center;
}

.top {
    width: 100%;
    height: 210px;
    border-radius: 15px 15px 0px 0px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

.top-content {
    height: 160px;
    width: 160px;
    font-size: 14px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
}

.bottom {
    height: 128px;
    width: 100%;
    background-color: white;
    border-radius: 0px 0px 15px 15px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.bottom-content {
    width: 170px;
    color: rgb(150, 150, 150);
    line-height: 18px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 90px;
}

.left-box {
    text-align: left;
    width: 250px;
    height: 300px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
}

.right-box {
    display: flex;
    width: 860px;
    height: 340px;
    justify-content: center;
    align-items: center;
}

.tutor-content {
    width: 100%;
    height: 550px;
    display: flex;
    background-color: rgb(247, 248, 251);
    justify-content: center;
    align-items: center;
    position: relative;
}

.main-content {
    width: 1200px;
    height: 350px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.arrow-img {
    background-image: url('../assets/todown.png');
    width: 15px;
    height: 15px;
    background-size: 100%;
    background-repeat: no-repeat;
    margin-left: 10px;
}

.arrow-img2 {
    background-image: url('../assets/todown.png');
    width: 20px;
    height: 20px;
    background-size: 100%;
    background-repeat: no-repeat;
}

.border {
    margin-top: 20px;
    border: 1px solid rgb(167, 167, 167);
    border-radius: 25px;
    width: 180px;
    display: flex;
    align-items: center;
    justify-content: center;
    padding-top: 12px;
    padding-bottom: 12px;
}

.title2 {
    display: none;
    font-size: 18px;
    text-align: left;
    font-weight: 700;
    line-height: 45px;
}

.none_1 {
    display: none;
}

.flex {
    display: inline-block;
    width: 22px;
    height: 22px;
}

@media screen and (max-width: 768px) {
    .arrow-img2 {
        display: none;
    }

    .main-content {
        flex-direction: column;
        width: 100%;
        padding: 20px;
        height: 520px;
    }

    .right-box {
        width: 100%;
        overflow-x: scroll;
        height: 400px;
        justify-content: flex-start;
        align-items: center;
        display: flex;
        flex-direction: row;
    }

    ::-webkit-scrollbar {
        display: none;
    }

    .right-box {
        overflow-x: scroll;
    }

    .tutor-box,
    .top,
    .bottom {
        width: 260px;

    }
    .tutor-box {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        box-shadow: none;
    }
    .top,.bottom {
        box-shadow: 1px 1px 10px 1px rgb(230 230 230);
    }
    .bottom {
        height: 145px;
    }

    .title {
        display: none;
    }

    .len {
        display: none;
    }

    .none_2 {
        display: none;
    }

    .none_1 {
        display: flex;
        width: 100%;
    }

    .border {
       width: 100%;
    }

    .left-box {
        height: 60px;
    }

    .tutor-content {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        padding: 30px 0;
    }

    .title2 {
        display: flex;
        margin-bottom: 15px;
    }

    .left-box {
        width: 100%;
    }

}

</style>

<script>
export default {
  name: 'Tutor',
  props: {
    msg: String
  },
  data() {
      return {
          tutor: [
              {
                  id: 1,
                  name: 'Donald Trump',
                  specialty: 'level 1~2, level 3~4',
                  stars: '4.6',
                  introduce: '국회는 국민의 보통·평등·직접·비밀선거에 의하여 선출된 국회의원으로 구성한다...',
                  views: 5500,
                  likes: 50,
                  goods: 30,
                  profile_img: 'profile.png'
              },
              {
                  id: 2,
                  name: 'Tim cook',
                  specialty: 'level 1~2, level 3~4, level 5~6',
                  stars: '5.0',
                  introduce: '국회는 국민의 보통·평등·직접·비밀선거에 의하여 선출된 국회의원으로 구성한다...',
                  views: 5500,
                  likes: 50,
                  goods: 30,
                  profile_img: 'profile.png'
              },
              {
                  id: 3,
                  name: 'steve jobs',
                  specialty: 'level 1~2, level 3~4, level 5~6',
                  stars: '5.0',
                  introduce: '국회는 국민의 보통·평등·직접·비밀선거에 의하여 선출된 국회의원으로 구성한다...',
                  views: 5500,
                  likes: 50,
                  goods: 30,
                  profile_img: 'profile.png'
              }
          ]
      }
  }
}
</script>
