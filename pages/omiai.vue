<template>
  <div>
    <div class="header">
      探す
    </div>
    <div class="user-cards">
      <div v-for="(user,i) in users" :key="i" class="user-card">
        <img :src="`https://unsplash.it/174/174?image=${user.imageId}`">
        <div class="user-info">
          <div>{{ user.age }}歳 {{ user.address }}</div>
          <div>{{ user.job }}</div>
        </div>
      </div>

      <div class="user-card">
        <img src="https://unsplash.it/174/174?image=903">
        <div class="user-info">
          <div>40才 東京</div>
          <div>薬剤師</div>
        </div>
      </div>

      <div class="user-card">
        <img src="https://unsplash.it/174/174?image=402">
        <div class="user-info">
          <div>30才 東京</div>
          <div>銀行証券・保険</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      users: [
        {
          imageId: 903,
          age: 29,
          address: '東京',
          job: '薬剤師'
        },
        {
          imageId: 402,
          age: 28,
          address: '東京',
          job: '銀行証券・保険'
        },
        {
          imageId: 200,
          age: 28,
          address: '神奈川',
          job: 'メーカー'
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

.user-card {
  display: inline-block;
  background: white;
  color: black;
  text-align: center;
  margin: 10px;
}

</style>
