<template>
  <div class="latest-section d-flex flex-column position-absolute">
    <p class="section-title position-static d-flex">Latest Release</p>
    <div class="song-info d-flex position-static">
  
      <div class="song-cover position-static">
        <img src="../assets/images/Song Cover.png" alt="">
      </div>
      <div class="song-name d-flex position-static flex-column">
        <p class="latest-name">Album / Song Name</p>
        <p class="latest-date">DEC 24, 2022</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.latest-section {
  align-items: flex-start;
  padding: 0px;
  width: 228px;
  height: 106px;
  left: 192px;
  top: 298px;
  background: #0a0a0a;
}
.song-info {
  align-items: center;
  padding: 0px;
  width: 228px;
  height: 78px;
  left: 0px;
  top: 28px;
  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 8px 0px;
  border: none !important;
  
}
.song-name {
  align-items: flex-start;
  padding: 0px;
  width: 136px;
  height: 40px;
  left: 92px;
  top: 19px;

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 14px;
  cursor: pointer;
}
.song-cover {
  width: 78px;
  height: 78px;
  left: 0px;
  top: 0px;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 0px;
  cursor: pointer;
}
.latest-date {
  position: static;
  width: 80px;
  height: 16px;
  left: 0px;
  top: 24px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 10.5px;
  line-height: 16px;

  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 1.5px;

  color: #ffffff;

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 4px 0px;
}
.latest-name {
  position: static;
  width: 136px;
  height: 20px;
  left: 0px;
  top: 0px;

  font: Circular Std;
  font-style: normal;
  font-weight: bold;
  font-size: 13px;
  line-height: 20px;

  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 0.25px;

  color: #ffffff;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 4px 0px;
}
.section-title{
width: 97px;
height: 20px;
left: 0px;
top: 0px;

font: Circular Std;
font-style: normal;
font-weight: bold;
font-size: 14px;
line-height: 20px;

position: static;
align-items: center;
letter-spacing: 0.25px;

color: #FFFFFF;

flex: none;
order: 0;
flex-grow: 0;
margin: 0px 0px;
}
</style>
