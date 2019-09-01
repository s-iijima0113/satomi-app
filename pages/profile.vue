<template>
  <div>
    <div class="header">
      詳細プロフィール
    </div>
    <div>{{ profile.content }}</div>
  </div>
</template>

<script>
export default {
  computed: {
    profile () {
      return this.profiles[0]
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
