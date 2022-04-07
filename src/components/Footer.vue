<template>
<div style="position: relative;" class="top">
  <div class="footer">
    <div class="footer-children">
      <div class="footer-child">
        <div class="footer-link">
          고객센터
        </div>
        <div class="footer-link">
          이용약관
        </div>
        <div class="footer-link">
          개인정보 처리방침 
        </div>
        <div class="footer-link">
          회사 소개
        </div>
      </div>
    </div>
  </div>

  <div class="footer2">
    <div class="footer-children">
      <div class="footer-child">
        <div class="footer-name">
          (주)이브릿지월드
        </div>
      </div>
    </div>
    <div class="small">
      <div class="footer-children non-visible">
        대표이사: {{ceo}}, 주소지: {{address}}, 사업자등록번호: {{num}},
        교육서비스업신고번호: {{num2}}, 사무실 주소: {{office}}, 개인정보보호책임자: {{res}},
        전화: {{phone}}, 팩스: {{fax}}, Email: {{email}}
      </div>
      <div class="footer-children visible">
        <div class="footer-child">
          <div class="footer-link2">
            대표이사: {{ceo}}
          </div>
          <div class="footer-link2">
            주소지: {{address}}
          </div>
          <div class="footer-link2">
            사업자등록번호: {{num}}
          </div>
          <div class="footer-link2">
            교육서비스업신고번호: {{num2}}
          </div>
        </div>
      </div>
      <div class="footer-children visible">
        <div class="footer-child">
          <div class="footer-link2">
            사무실 주소: {{office}}
          </div>
          <div class="footer-link2">
            개인정보보호책임자: {{res}}
          </div>
          <div class="footer-link2">
            전화: {{phone}}
          </div>
          <div class="footer-link2">
            팩스: {{fax}}
          </div>
          <div class="footer-link2">
            Email: {{email}}
          </div>
        </div>
      </div>
      </div>
      <div class="footer-children">
        <div class="footer-child">
          <div class="footer-link2 copyright">
            copyright ⓒ 2021 YalliYalli by eBridge World Inc. All rights reserved.
          </div>
        </div>
      </div>
      <div class="footer-children">
        <div class="footer-child">
          <div class="footer-link3">
            <a href="/">
              <div class="img img1"></div>
            </a>
          </div>
          <div class="footer-link3">
            <a href="/">
              <div class="img img2"></div>
            </a>
          </div>
          <div class="footer-link3">
            <a href="/">
              <div class="img img3"></div>
            </a>
          </div>
          
        </div>
      </div>
  </div>
</div>
</template>

<style scoped>

.img {
  width: 40px;
  height: 40px;
  background-size: 100%;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
}

.top {
  margin-top: 150px;
}

.footer {
  width: 100%;
  display: flex;
  height: 50px;
  justify-content: center;
  align-items: center;
  border-top: 1px solid rgb(190, 190, 190);
  border-bottom: 1px solid rgb(190, 190, 190);
}

.img1 {
  background-image: url('../assets/facebook.png');
}

.img2 {
  background-image: url('../assets/instagram.png');
}

.img3 {
  background-image: url('../assets/youtube-icon.png');
}

.footer2 {
  width: 100%;
  display: flex;
  height: 250px;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  margin-bottom: 50px;
}

.footer2 > .footer-children {
  margin-top: 10px;
  margin-bottom: 10px;
}

.small {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 45px;
}

.footer-children {
  width: 1180px;
  height: 30px;
  display: flex;
  align-items: center;
}

.footer-child {
  display: flex;
}

.footer-link {
  padding-left: 15px;
  padding-right: 15px;
  font-size: 14px;
  font-weight: 500;
  color: rgb(66, 66, 66);
}

.footer-name {
  font-size: 14px;
  padding-left: 10px;
  font-weight: 500;
  color: rgb(100, 100, 100);
}

.footer-link2 {
  padding-left: 10px;
  padding-right: 10px;
  font-size: 12.5px;
  font-weight: 500;
  color: rgb(148, 148, 148);
  border-left: 1px solid rgb(220, 220, 220);
  display: flex;
  align-items: center;
  height: 12px;
}

.footer-link3 {
  padding-left: 5px;
  padding-right: 5px;
}

.footer-link2:first-child {
  border: none;
}


.copyright {
  color: rgb(210, 210, 210)
}

.non-visible {
  display: none;
}


@media screen and (max-width: 768px) {
  .footer-link:first-child {
    padding-left: 20px;
  }

  .footer-link {
    font-size: 13px;
    color: gray;
    padding-left: 8px;
    padding-right: 8px;
  }

  .footer-children {
    width: 100%;
    padding: 20px;
  }

  .non-visible {
    display: flex;
    justify-content: flex-start;
    text-align: left;
    margin-left: 10px;
    font-size: 13px;
    color: rgb(180, 180, 180);
    width: 95%;
    margin-top: 7px;
    margin-bottom: 7px;
    line-height: 20px;
  }

  .copyright {
    margin-top: 15px;
    text-align: left;
  }

  .visible {
    display: none;
  }

  .top {
    height: 350px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    margin-top: 20px;
  }
}


</style>

<script>
export default {
  name: 'Footer',
  props: {
    msg: String
  },
  data() {
    return {
      ceo: '김영찬',
      address: '충청남도 천안시 서북구 직산로 136, 1층 비아이 5호',
      num: '515-85-16296',
      num2: '2021-충남천안-1557',
      office: '서울시 강남구 테헤란로 501, 5층',
      res: '오진환',
      phone: '02-2088-6232',
      fax: '02-6964-7155',
      email: 'contact@ebrige-world.com',
    }
  }
}
</script>