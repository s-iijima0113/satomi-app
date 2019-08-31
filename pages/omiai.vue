<template>
  <div>
    <div class="header">
      探す
    </div>
    <div class="user-cards">
      <div v-for="(user,i) in users" :key="i" class="user-card">
        <img :src="`https://unsplash.it/174/174?image=${user.imageId}`">
        <div class="profile-panel">
          <div class="main-photo" />
          <div class="caption-under-photo">
            <div class="mach-percentage-icon">
              <div class="icon-match-persentage">
                <svg viewBox="0 0 40 40" class="sda-anime" width="40" height="40">
                  <circle class="blank" cx="20" cy="20" r="15.92" />
                  <circle class="fill" :stroke-dasharray="`${user.num},${100-user.num}`" cx="20" cy="20" r="15.92" />
                </svg>
                <div id="num">
                  {{ user.num }}
                  <span class="num-span">%</span>
                </div>
              </div>
            </div>
          </div>
          <div class="block-light">
            <div class="sub-photo-count">
              <span class="icon-camera" />
              <span id="photonum" />
              {{ user.photonum }}
            </div>
            <div class="like-received-count">
              <span class="icon-interest-pink" />
              <span class="likereceivednum" />
              {{ user.likereceivedcount }}
            </div>
          </div>
        </div>
        <div class="user-info">
          <div id="age.adress">
            <span class="icon-online" />
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
          job: '薬剤師',
          num: 100,
          photonum: '5',
          likereceivedcount: '100'
        },
        {
          imageId: 402,
          age: 28,
          address: '東京',
          job: '銀行証券・保険',
          num: 90,
          photonum: '2',
          likereceivedcount: '200'
        },
        {
          imageId: 200,
          age: 28,
          address: '神奈川',
          job: 'メーカー',
          num: 80,
          photonum: '3',
          likereceivedcount: '150'
        },
        {
          imageId: 102,
          age: 40,
          address: '東京',
          job: '薬剤師',
          num: 78,
          photonum: '10',
          likereceivedcount: '300'
        },
        {
          imageId: 100,
          age: 30,
          address: '東京',
          job: '不動産',
          num: 20,
          photonum: '3',
          likereceivedcount: '500'
        },
        {
          imageId: 101,
          age: 32,
          address: '神奈川',
          job: '人材',
          num: 60,
          photonum: '8',
          likereceivedcount: '800'
        },
        {
          imageId: 103,
          age: 34,
          address: '埼玉',
          job: '事務',
          num: 90,
          photonum: '3',
          likereceivedcount: '500'
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

.profile-panel{
  position: relative;
  padding: 0;
  margin: 0;
  cursor: pointer;
}

.caption-under-photo{
  position: relative;
  padding: 0;
}

.mach-percentage-icon{
  position: absolute;
  left: 6px;
  bottom: 10px;
  box-sizing: border-box;
  display: block;
}

.icon-match-persentage{
  width: 40px;
  height: 40px;
  box-sizing: border-box;
  display: block;
}

.sda-anime{
  position: absolute;
  left: 0;
}

svg .blank{
  stroke: #E3E3E3;
  fill: #FFFFFF;
  stroke-width: 2.5;
}

svg .fill{
  stroke: #FF8D8B;
  fill: transparent;
  stroke-width: 2.5;
  stroke-dashoffset: 25;
}

.num-span{
  font-size: 8px;
}

.block-light{
  position: absolute;
  right: 8px;
  bottom: 10px;
  box-sizing: border-box;
  display: block;
}

.sub-photo-count{
  margin-bottom: 6px;
  padding: 5px 8px;
  border-radius: 100px;
  background-color: rgba(255, 255, 255, 0.9);
  color: #A0A0A0;
  font-size: 12px;
  line-height: 0.9px;
  box-sizing: border-box;
}

.icon-camera{
  display: inline-block;
  width: 12px;
  height: 10px;
  background-image: url("~assets/camera.jpg");
  background-size: 100%;
  box-sizing: border-box;
}

.count{
  margin-left: 4px;
  box-sizing: border-box;
  color: #A0A0A0;
}

.like-received-count{
  margin-bottom: 6px;
  padding: 5px 8px;
  border-radius: 100px;
  background-color: rgba(255, 255, 255, 0.9);
  color: #FF8D8B;
  font-size: 12px;
  line-height: 0.9;
  box-sizing: border-box;
  display: block;
}

.icon-interest-pink{
  display: inline-block;
  width: 10px;
  height: 10px;
  background: url("~assets/like-it.jpeg");
  background-size: 100%;
  box-sizing: border-box;
}

.user-info {
  padding: 13px 0 17px;
  text-align: center;
}

.essential-line{
  margin: 0 4px;
  font-size: 16px;
}

.icon-online{
  background-color: #C0E452;
  margin: 0px 4px;
  width: 12px;
  height: 12px;
  display: inline-block;
  border-radius: 100%;
  box-sizing: border-box;
  animation: icon-flashing
}

.occupation-line{
  margin:8px 0px 0px
}

#num {
  position: relative;
  color: #FF8D8B;
  font-size: 12px;
  font-weight: bold;
  text-align: center;
  line-height: 40px;
  letter-spacing: -1px;
  box-sizing: border-box;
}

#photonum {
  margin-left: 4px;
  box-sizing: border-box;
  color: #A0A0A0;
  font-size: 12px;
  line-height: 0.9px;
}

#likereceivedcount {
  color: #FF8D8B;
  font-size: 12px;
  line-height: 0.9;
  box-sizing: border-box;
}

#age.adress {
  margin: 0 4px;
  font-size: 16px;
  box-sizing: border-box;
}

#job {
  font-size: 12px;
}
</style>
