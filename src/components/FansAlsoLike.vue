<template>
  <div class="fans-also-like d-flex flex-column position-absolute">
    <p class="section-title position-static d-flex mb-12">Fans Also Like</p>
    <div class="items d-flex flex-column position-static">
      <div
        class="artist-item d-flex flex-row align-items-center position-static"
      >
        <img src="../assets/images/artist.png" alt="" />
        <span class="artist-name d-flex align-items-centers">Syahreza</span>
      </div>
        <div
        class="artist-item d-flex flex-row align-items-center position-static"
      >
        <img src="../assets/images/artist.png" alt="" />
        <span class="artist-name d-flex align-items-center">Husna</span>
      </div>
        <div
        class="artist-item d-flex flex-row align-items-center position-static"
      >
        <img src="../assets/images/artist.png" alt="" />
        <span class="artist-name d-flex align-items-center">Pamungkas</span>
      </div>
        <div
        class="artist-item d-flex flex-row align-items-center position-static"
      >
        <img src="../assets/images/artist.png" alt="" />
        <span class="artist-name d-flex align-items-center">Sizy Hamilton</span>
      </div>
    </div>
  </div> 
</template>

<script>
export default {};
</script>

<style scoped>
.fans-also-like {
  align-items: flex-start;
  padding: 0px;
  width: 143px;
  height: 328px;
  left: 841px;
  top: 295px;
}
.section-title {
  width: 96px;
  height: 20px;
  left: 0px;
  top: 0px;

  font: Circular Std;
  font-style: normal;
  font-weight: bold;
  font-size: 13px;
  line-height: 20px;

  align-items: center;
  letter-spacing: 0.25px;

  color: #ffffff;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 12px 0px;
}
.items {
  align-items: flex-start;
  padding: 0px;

  width: 143px;
  height: 296px;
  left: 0px;
  top: 32px;
  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 12px 0px;
}
.artist-item {
  padding: 0px;
  width: 130px;
  height: 36px;
  left: 0px;
  top: 260px;

  flex: none;
  order: 5;
  flex-grow: 0;
  margin: 16px 0px;
  cursor: pointer;
}
img {
  position: static;
  width: 36px;
  height: 36px;
  left: 0px;
  top: 0px;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 14px;
}
.artist-name {
  position: static;
  width: 93px;
  height: 18px;
  left: 50px;
  top: 9px;

  font: Circular Std;
  font-style: normal;
  font-weight: bold;
  font-size: 12px;
  line-height: 18px;

  letter-spacing: 0.4px;

  color: #ffffff;
  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 14px;
}
</style>
