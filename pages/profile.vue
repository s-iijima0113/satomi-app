<template>
  <div>
    <div class="header">
      詳細プロフィール
    </div>
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
                  86
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
                <ul></ul>
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
</style>
