<template>
  <div>
    <div class="header">
      詳細プロフィール
    </div>
    <body class="style" />
    <div class="model-content">
      <div class="row">
        <div id="modal-member-detail-main-photo">
          <div class="inner">
            <div class="match-percentage-icon">
              <div class="match-percentage-large">
                <svg viewbox="0 0 40 40" class="sda-anime" width="70" height="70">
                  <circle class="blank" cx="20" cy="20" r="15.92" />
                  <circle class="fill" stroke-dasharray="86,14" cx="20" cy="20" r="15.92" />
                </svg>
                <div class="num">
                  <span class="text">マッチ度</span>
                  "86"
                  <span class="symbol">%</span>
                </div>
              </div>
            </div>
            <div class="sub-photo-area">
              <div class="sub-photo-line" />
              <div class="photo-first" />
            </div>
            <div class="main">
              <div>
                <span id="basis-nickname" class="nicname">T.K</span>
                <span id="basis-age">34歳</span>
                <span id="basis-area">東京</span>
              </div>
              <div class="statas-area">
                <ul />
              </div>
            </div>
            <div class="tab-content">
              <div id="tab-profile" class="tab-pane-active">
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
  </div>
  </div>
  </div>
</template>

<script>
export default {
  computed: {
    profile () {
      return this.profiles[+this.$route.query.userId]
    }
  },
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
  }
}
</script>

<style scoped>
.header {
  background: white;
  color: black;
}

.style{
  background-color: #EEEEEE;
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

.row{
  padding-top: 20px;
  padding-left: 20px;
  padding-right: 20px;
  padding: 0;
  margin: 0;
}

.modal-member-detail-main-photo{
  max-width: 395px;
  border-radius: 5px;
  position: relative;
  padding-left: 0;
  padding-right: 0;
  height: auto;
  background-color: #fAF9f7;
  background-position: center center;
  background-repeat: no-repeat;
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
}

.sda-anime{
  position: absolute;
  overflow: hidden;
  box-sizing: border-box;
}

svg .blank{
  stroke: #E3E3E3;
  fill: #FFFFFF;
  stroke-width: border-box;
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
}

</style>
