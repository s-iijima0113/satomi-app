<template>
  <div class="style">
    <div class="header">
      詳細プロフィール
    </div>
    <div id="container" class="container-serch">
      <div class="bottom-area">
        <div class="model-content">
          <div class="content-row">
            <div class="modal-member-detail-main-photo">
              <div class="inner">
                <div class="match-percentage-icon">
                  <div class="match-percentage-large">
                    <svg viewBox="0 0 40 40" class="sda-anime" width="40" height="40">
                      <circle class="blank" cx="20" cy="20" r="15.92" />
                      <circle class="fill" stroke-dasharray="86,14" cx="20" cy="20" r="15.92" />
                    </svg>
                    <div class="num">
                      <span class="text">マッチ度</span>
                      86
                      <span class="symbol">%</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="sub-photo-area">
              <div class="sub-photo-center" />
              <div class="photo-first" />
            </div>
          </div>
          <div class="main">
            <div>
              <span id="basis-nickname" class="nicname">T.K</span>
              <span id="basis-age">34歳 / </span>
              <span id="basis-area">東京</span>
            </div>
            <div class="statas-area">
              <ul class="status">
                <li class="online-status">
                  <span class="icon-online" />
                  <span class="online-text">オンライン</span>
                </li>
                <li class="age-confirmed">
                  <span class="age-confirmed-icon" />
                  <span>認証済み</span>
                </li>
                <li class="interest">
                  <span class="interest-pink" />
                  <span>いいね！ : 212  </span>
                </li>
              </ul>
            </div>
          </div>
          <div class="tab-content">
            <div id="tab-pane-active" class="tab-profile">
              <h2 id="introduction-title" class="title-with-background">
                <span class="inner-text">自己紹介文</span>
              </h2>
              <p id="detail-introduction" class="self-introduction-text" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      profiles: [
        {
          userId: 0,
          content: `
はじめまして！聡美です！
東京でエンジニア目指してます！
`
        },
        {
          userId: 1,
          content: `
こんにちは！初めまして！
神奈川でデザイナーやってます！
`
        },
        {
          userId: 2,
          content: `
こんにちは＾＾
東京でエンジニアやってます！
`
        },
        {
          userId: 3,
          content: `
こんにちは。栃木で教員をしています！
よろしくお願いします！
`
        },
        {
          userId: 3,
          content: `
はじめまして。神奈川で不動産関係の仕事をしています。
よろしくお願いします！
`
        },
        {
          userId: 4,
          content: `
はじめまして！
都内でプログラミング教師をしています！
`
        },
        {
          userId: 5,
          content: `
こんにちは。
神奈川で英語の教師をしています！
`
        }
      ]
    }
  },
  computed: {
    profile () {
      return this.profiles[+this.$route.query.userId]
    }
  }
}
</script>

<style scoped>
.header {
  background: white;
  color: black;
}

.bottom-area{
  padding-bottom: 100px;
  background-color: #FFFFFF;
  box-sizing: border-box;
  display: block;
}

.container-serch{
  width: 500px;
  margin-left: auto;
  margin-right: auto;
  box-sizing: border-box;
}

.style{
  background-color: plum;
  font-size: 16px;
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.42857;
  color: #333333;
  margin: 0;
  box-sizing: 0;
  display: block;
}

.model-content{
  box-sizing: border-box;
  display: block;
}

.content-row{
  padding-top: 20px;
  padding-left: 20px;
  padding-right: 20px;
  box-sizing: border-box;
  display: block;
  height:400px;
}

.content-row::before{
  content: " ";
  display: table;
  box-sizing: border-box;
}

.row::after{
  clear: both;
}

.modal-member-detail-main-photo{
  max-width: 395px;
  border-radius: 5px;
  position: relative;
  padding-left: 0;
  padding-right: 0;
  height: 368px;
  background-position: center center;
  background-repeat: no-repeat;
  width: 80%;
  background-color: yellow;
  float: left;
}

.modal-member-detail-main-photo::before{
  display: block;
  padding-top: 100%;
  content: "";
  box-sizing: border-box;
}

.inner{
  border-radius: 5px;
  display: inline-block;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-position: center center;
  background-repeat: no-repeat;
  background-size: contain;
  box-sizing: border-box;
  background-image: url("~assets/human.png");
}

.match-percentage-icon{
  display: inline-block;
  position: absolute;
  bottom: 15px;
  right: 15px;
  cursor: pointer;
  box-sizing: border-box;
  font-size: 16px;
}

.match-percentage-large{
  width: 70px;
  height: 70px;
  box-sizing: border-box;
  display: block;
  box-sizing: border-box;
}

.sda-anime{
  width: 70px;
  height: 70px;
  position: absolute;
  overflow: hidden;
  box-sizing: border-box;
}

svg .blank{
  stroke: #E3E3E3;
  fill: #FFFFFF;
  stroke-width: 2.5px;
}

svg .fill{
  stroke: #FF8D8B;
  fill: transparent;
  stroke-width: 2.5;
  stroke-dashoffset: 25;
  box-sizing: border-box;
}

.num{
  display: table-cell;
  position: relative;
  width: 70px;
  height: 70px;
  vertical-align: middle;
  color: #FF8D8B;
  font-size: 20px;
  font-weight: bold;
  text-align: center;
  line-height: 1.0;
  letter-spacing: -1px;
  box-sizing: border-box
}

.text{
  display: block;
  margin-bottom: 0;
  font-size: 9px;
  box-sizing: border-box;
}

.symbol{
 font-size: 13px;
 box-sizing: border-box;
}

.sub-photo-area{
  width: 20%;
  float: left;
  position: relative;
  min-height: 1px;
  height: 368px;
  box-sizing: border-box;
  padding-left: 15px;
  }

.sub-photo-center{
  background-color: aquamarine;
  height: 100%;
  padding-left: 20px;
}

.main{
  margin-top: 25px;
  margin-bottom: 25px;
  font-size: 18px;
  text-align: center;
  box-sizing: border-box;
}

.status{
  font-size: 13px;
  margin: 20px 0;
  padding: 0;
  box-sizing: border-box;
  display: block;
  list-style-type: disc;
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  padding-inline-start: 40px;
}

.online-status{
  display: inline-block;
  list-style: none;
  flex-grow: 1;
  padding-right: 10px;
  box-sizing:border-box;
}

.icon-online{
  width: 14px;
  height: 14px;
  background-color: #C0E452;
  display: inline-block;
  border-radius: 100%;
  margin-bottom: -1px;
}

.icon-online{
  animation: icon-online 2s infinite;
}

.online-text{
  box-sizing: border-box;
}

@keyframes icon-online{
  50%{
    opacity: 0;
  }
}

.age-confirmed{
  padding-left: 10px;
  border-left: 1px solid #E3E3E3;
  display: inline-block;
  list-style: none;
  flex-grow: 1;
  padding-right: 10px;
  box-sizing: border-box;
}

.age-confirmed-icon{
  display: inline-block;
  width: 17px;
  height: 14px;
  background-size: 70%;
  box-sizing: border-box;
  background-image: url("~assets/age-confirm.jpg");
}

.interest{
  padding-left: 10px;
  border-left: 1px;
  display: inline-block;
  list-style: none;
  flex-grow: 1;
  padding-right: 10px;
  box-sizing: border-box;
}

.interest-pink{
  width: 14px;
  height: 14px;
  display: inline-block;
  background-size: 100%;
  box-sizing: border-box;
  background-image: url("~assets/like-it.jpeg");
}

.nicname{
  margin: 0 8px;
  font-size: 26px;
  box-sizing: border-box;
  text-align: center;
}

.basis-age{
  box-sizing: border-box;
  font-size: 18px;
  text-align: center;
}

.basis-area{
  box-sizing: border-box;
  font-size: 18px;
  text-align: center;
}

.statas-area{
  box-sizing: border-box;
  display: block;
}

.tab-content{
  box-sizing: border-box;
  display: block;
}

.tab-profile{
  display: block;
  box-sizing: border-box;
}

.title-with-background{
  margin-top: -1px;
  position: relative;
  height: 50px;
  margin: 0;
  border-top: 1px solid #E3E3E3;
  border-bottom: 1px solid #E3E3E3;
  background: #FAF9F7;
  font-size: 30px;
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
  box-sizing: border-box;
  display: block;
  margin-block-start: 0.83em;
  margin-block-end: 0.83em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
}

.inner-text{
  left: 20px;
  position: absolute;
  bottom: 10px;
  color: #2D2E2D;
  font-size: 16px;
  font-weight: bold;
  box-sizing: border-box;
  font-family: inherit;
  line-height: 1.1;
}

.self-introduction-text{
  padding: 15px 23px 10px;
  font-size: 16px;
  line-height: 24px;
  word-wrap: break-word;
  margin: 0 0 10px;
  box-sizing: border-box;
  display: block;
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
}

</style>
