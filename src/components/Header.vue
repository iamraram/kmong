<template>
  <div class="header">
    <div class="header-content">
        <div class="left-content">
            <div class="logo-img" />
            <div class="header-menu">
                <a href="/" v-for="(repeat, i) in menu_value" :key="i" class="header-menu-content">
                    <li>
                        {{menu_value[i]}}
                    </li>
                </a>
            </div>
        </div>
        <div class="right-content">
            <div class="coin-value">
                {{coin_value}}
                <div class="coin-img">
                    P
                </div>
            </div>
            <div class="lang-set">
                <div class="profile-img" />
                <div class="lang-arrow">
                    한국어
                    <div class="down-img" />
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    menu: String
  },
  data() {
      return {
          menu_value: ['1:1수업', '미니 TOPIK', '모의 TOPIK', '강의'],
          coin_value: '1,444'
      }
  }
}
</script>

<style scoped>

a {
    text-decoration: none;
    color: black;
}

.header {
    display: flex;
    justify-content: center;
    flex-direction: row;
    height: 60px;
    width: 100%;
    padding: 5px;
    padding-left: 0;
    padding-right: 0;
}

.header-content {
    width: 1100px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    font-size: 14px;
}

.lang-arrow {
    width: 65px;
    justify-content: space-between;
    display: flex;
}

li {
    list-style: none;
}

.logo-img {
    background-image: url('../assets/logo.png');
    width: 140px;
    height: 45px;
    background-size: 100%;
    background-repeat: no-repeat;
}

.down-img {
    background-image: url('../assets/todown.png');
    width: 20px;
    height: 20px;
    border-radius: 20px;
    background-size: 100%;
    background-repeat: no-repeat;
    opacity: 0.7;
}

.lang-set {
    display: flex;
    width: 130px;
    justify-content: space-between;
    align-items: center;
}

.profile-img {
    background-image: url('../assets/profile.png');
    width: 40px;
    height: 40px;
    border-radius: 20px;
    background-size: 100%;
    background-repeat: no-repeat;
}

.header-menu {
    display: flex;
    justify-content: space-between;
    widows: 500px;
    flex-direction: row;
    height: 50px;
}

.lang-set {
    color: rgb(70, 70, 70);
}

.header-menu-content {
    width: 70px;
    padding: 15px;
    padding-left: 5px;
    padding-right: 5px;
    margin-left: 5px;
    margin-right: 5px;
}

.left-content {
    display: flex;
    flex-direction: row;
    width: 520px;
    justify-content: space-between;
}

.right-content {
    display: flex;
    flex-direction: row;
    width: 240px;
    justify-content: space-between;
    align-items: center;
}

.header-menu-content:first-child {
    font-weight: 600;
    border-bottom: 2px solid rgb(47, 190, 166);
}

.coin-value {
    width: 78px;
    border: 1px solid rgb(180, 180, 180);
    border-radius: 30px;
    display: flex;
    justify-content: space-around;
    padding-top: 3px;
    padding-bottom: 3px;
    align-items: center;
    padding-left: 5px;
}

.coin-img {
    display: flex;
    width: 22px;
    height: 22px;
    background-color: rgb(246, 225, 103);
    border: 1px solid rgb(228, 169, 7);
    border-radius: 15px;
    align-items: center;
    justify-content: center;
    color: white;
    font-weight: 600;
}


</style>
