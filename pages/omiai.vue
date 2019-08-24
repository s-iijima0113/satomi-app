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
                  <circle class="fill" stroke-dashrray="74,26" cx="20" cy="20" r="15.92" />
                </svg>
                <div class="num">
                  74
                  <span>%</span>
                </div>
              </div>
            </div>
          </div>
          <div class="block-light">
            <div class="sub-photo-count">
              <span class="icon-camera" />
              <span class="count">1</span>
            </div>
            <div class="like-received-count">
              <span class="icon-interest-pink" />
              <span>~5</span>
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
  box-sizing: border-box;
}

.num span{
  font-size: 8px;
}

.block-light{
  position: absolute;
  right: 8px;
  bottom: 2px;
  box-sizing: border-box;
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
  background-image: url("https://www.google.com/search?biw=1302&bih=894&tbm=isch&sa=1&ei=wcpfXc_CBY_N-QbhgpvYBQ&q=%E3%82%AB%E3%83%A1%E3%83%A9%E3%81%AE%E3%82%A2%E3%82%A4%E3%82%B3%E3%83%B3&oq=%E3%82%AB%E3%83%A1%E3%83%A9%E3%81%AE%E3%82%A2%E3%82%A4%E3%82%B3%E3%83%B3&gs_l=img.3..0j0i24l6.1553.11516..11906...9.0..4.574.6392.2j25j6j1j0j1......0....1..gws-wiz-img.....0..35i39j0i4j0i4i24.ZtFNsiStuxM&ved=0ahUKEwiPp6Pc7pjkAhWPZt4KHWHBBlsQ4dUDCAY&uact=5#imgrc=_");
  background-size: 100%;
  box-sizing: border-box;
}

.count{
  margin-left: 4px;
  box-sizing: border-box;
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
}

.icon-interest-pink{
  display: inline-block;
  width: 10px;
  height: 10px;
  background: transparent url(/omiai/img/icon/interest_pink.svg) center no-repeat;
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
}

.occupation-line{
  margin:8px 0px 0px
}

.sub-photo-count{
  margin-bottom: 6px;
  padding: 5px 8px;
  border-radius: 100px;
  background-color: rgba(255, 255, 255, 0.9);
  color: #aa00aa;
  font-size: 12px;
  line-height: 0.9;
  box-sizing: border-box;
  display: block;
}

#age.adress {
  margin: 0 4px;
  font-size: 16px;
}

#job {
  font-size: 12px;
}
</style>
