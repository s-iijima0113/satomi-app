<template>
  <div>
    <div class="header">
      探す
    </div>
    <div class="user-cards">
      <div v-for="(user,i) in users" :key="i" class="user-card">
        <img :src="`https://unsplash.it/174/174?image=${user.imageId}`">
        <div class="caption-underphoto">
          <div class="mach-percentage-icon">
          </div>
          <div class="block-light">
            <div class="sub-photo-count">
            </div>
            <div class="like-received-count">
            </div>
          </div>
        </div>
        <div class="caption-on-caption">
          <div class="essential-line">
          </div>
          <span class="icon-online">
          </span>
        </div>
        <div class="user-info">
          <div id="age.adress">
            {{ user.age }}歳 {{ user.address }}
          </div>
          <div class="occupation-line">
            <div id="job">
              {{ user.job }}
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
        },
        {
          imageId: 102,
          age: 40,
          address: '東京',
          job: '薬剤師'
        },
        {
          imageId: 100,
          age: 30,
          address: '東京',
          job: '不動産'
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

.user-info {
  padding: 13px 0 17px;
  text-align: center;
}

.essential-line{
  font-size: 16px;
}

.occupation-line{
  margin:8px 0px 0px
}

#age.adress {
  margin: 0 4px;
  font-size: 16px;
}

#job {
  font-size: 12px;
}
</style>
