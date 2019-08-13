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
            <div class="icon-match-persentage">
              <svg viewBox="0 0 40 40" class="sda-anime" width="40" height="40" />
              <circle class="blank" cx="20" cy="20" r="15.92" />
              <circle class="fill" stroke-dashrray="74,26" cx="20" cy="20" r="15.92" />
              <div class="num">
                74
                <span>%</span>
              </div>
            </div>
          </div>
          <div class="block-light">
            <div class="sub-photo-count" />
            <div class="like-received-count" />
          </div>
        </div>
        <div class="caption-on-caption">
          <div class="essential-line" />
          <span class="icon-online" />
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

.mach-percentage-icon{
  position: absolute;
  left: 6px;
  bottom: 5px;
}

.icon-match-persentage{
  width: 40px;
  height: 40px;
}

.blank{
  stroke: #E3E3E3;
  fill: #FFFFFF;
  stroke-width: 2.5;
}

.fill{
  stroke: #FF8D8B;
  fill: transparent;
  stroke-width: 2.5;
  stroke-dashoffset: 25;
}

.num{
  position: relative;
  color: violet;
  font-size: 12px;
  font-weight: bold;
  text-align: center;
  line-height: 40px;
  letter-spacing: -1px;
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
