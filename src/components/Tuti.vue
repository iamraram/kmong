<template>
  <div class="tuti">
    <div class="tuti-content">
      <div class="tuti-children">
        <div class="tuti-title">
            튜티들의 솔직한 후기를 들어보세요
        </div>
        <div class="tuti-block-parent">
          <div class="tuti-block" v-for="(repeat, i) in 3" :key="i">
            <div class="tuti-block-title">
              <img :src="require('../assets/profile_img/profile.png')" class="tutor-img">
              <div class="real-title">
                {{tuti[i].tutor}}
              </div>
            </div>
            <div class="tuti-block-desc">
              {{tuti[i].desc}}
            </div>
            <div class="tuti-block-info">
              {{tuti[i].tuti}} {{tuti[i].date}}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Tuti',
  props: {
    msg: String
  },
  data() {
    return {
      tuti: [
        {
          id: 1,
          profile_img: '/',
          tutor: '임시 데이터 튜터',
          desc: '국회는 국민의 보통·평등·직접·비밀선거에 의하여 선출된 국회의원으로 구성한다. 국회는 국민의 보통·평등·직접·비밀선거에 의하여 선출된 국회의원으로 구성한다.',
          tuti: 'hello*****',
          date: '22.04.01'
        },
        {
          id: 2,
          profile_img: '/',
          tutor: '임시 데이터 튜터',
          desc: '국회는 국민의 보통·평등·직접·비밀선거에 의하여 선출된 국회의원으로 구성한다. 국회는 국민의 보통·평등·직접·비밀선거에 의하여 선출된 국회의원으로 구성한다.',
          tuti: 'hello*****',
          date: '22.04.01'
        },
        {
          id: 3,
          profile_img: '/',
          tutor: '임시 데이터 튜터',
          desc: '국회는 국민의 보통·평등·직접·비밀선거에 의하여 선출된 국회의원으로 구성한다. 국회는 국민의 보통·평등·직접·비밀선거에 의하여 선출된 국회의원으로 구성한다.',
          tuti: 'hello*****',
          date: '22.04.01'
        }
      ]
    }
  }
}
</script>

<style scoped>

.tutor-img {
  width: 34px;
  height: 34px;
  border-radius: 40px;
  margin-right: 15px;
}

.tuti-block-info {
  font-size: 13px;
  color: rgb(158, 158, 158);
}

.tuti-block-desc {
   color: rgb(82, 82, 82);
   font-size: 13px;
   line-height: 18px;
}


.tuti-block-title {
  display: flex;
  align-items: center;
  width: 250px;
}

.real-title {
  font-weight: 600;
  font-size: 14px;
}

.tuti {
  position: relative;
}

.tuti-content {
  background-image: url('../assets/back.png');
  width: 100%;
  height: 300px;
  background-size: 100%;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
}

.tuti-title {
  font-size: 33px;
  font-weight: 700;
}

.tuti-block-parent {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: space-between;
}

.tuti-block-parent {
  align-items: center;
  display: flex;
}

.tuti-children {
  display: flex;
  flex-direction: column;
  width: 1200px;
  align-items: space-between;
  justify-content: space-between;
  position: relative;
  top: 60px;
}

.tuti-block {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  width: 380px;
  padding: 30px;
  padding-left: 40px;
  padding-right: 40px;
  text-align: left;
  height: 200px;
  background-color: white;
  border: 1px solid rgb(237, 237, 237);
  box-shadow: 1px 1px 10px 1px rgb(230, 230, 230);
  border-radius: 20px;
}
@media screen and (max-width: 768px) {
  .tuti-title {
    font-size: 18px;
    text-align: left;
    font-weight: 700;
    line-height: 45px;
  }

  .tuti-children {
    top: 0;
    width: 100%;
    padding: 20px;
    height: 100%;
    padding-right: 0;
    position: relative;
  }

  .tuti-block:first-child {
    margin-left: 0;
  }

  .tuti {
    position: relative;
  }

  .tuti-block {
    width: 250px;
    margin-left: 10px;
    margin-right: 10px;
    height: 220px;
  }

  .tuti-content {
    align-items: flex-start;
    justify-content: flex-start;
    position: relative;
    width: 100%;
  }

  .tuti-block-parent {
    width: 100%;
    overflow: scroll;
  }

  ::-webkit-scrollbar {
    display: none;
  }
}

</style>
