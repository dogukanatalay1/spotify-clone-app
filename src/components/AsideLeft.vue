<template>
  <div class="aside-left position-absolute">
    <div class="playlist-menu d-flex flex-column p-0 position-absolute">
      <!-- top menu -->
      <div class="al-nav-menu-top d-flex flex-column p-0 position-static">
        <span class="top-item order-0 home">
          <img class="icon" src="../assets/images/home.png" alt="" /> Home
        </span>
        <span class="top-item order-1 browse">
          <img class="icon" src="../assets/images/ellipse1.png" alt="" /> Browse
        </span>
        <span class="top-item order-2 radio">
          <img class="icon" src="" alt="" /> Radio
        </span>
      </div>
      <!-- middle menu -->
      <div class="al-nav-menu-mid d-flex flex-column p-0 position-static">
        <span class="mid-header">YOUR LIBRARY</span>
        <div class="mid-menu-item d-flex flex-row position-static">
          <span>Made For You</span>
        </div>
        <div class="mid-menu-item d-flex flex-row position-static">
          <span>Recently Played</span>
        </div>
        <div class="mid-menu-item d-flex flex-row position-static">
          <span>Like Songs</span>
        </div>
        <div class="mid-menu-item d-flex flex-row position-static">
          <span>Albums</span>
        </div>
        <div class="mid-menu-item d-flex flex-row position-static">
          <span>Made For You</span>
        </div>
        <div class="mid-menu-item d-flex flex-row position-static">
          <span>Artists</span>
        </div>
        <div class="mid-menu-item d-flex flex-row position-static">
          <span>Podcasts</span>
        </div>
      </div>

      <!-- bottom menu -->
      <div class="al-nav-menu-bottom d-flex flex-column p-0 position-static">
        <div class="bottom-header d-flex flex-row position-static">
          <span>Playlists </span>
        </div>
        <div class="bottom-item d-flex flex-row position-static">
          <span>Just For Us</span>
        </div>
        <div class="bottom-item d-flex flex-row position-static">
          <span>Nostalgia</span>
        </div>
        <div class="bottom-item d-flex flex-row position-static">
          <span>Just For Us</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.aside-left {
  width: 164px;
  left: 0px;
  top: 0px;
  bottom: 0px;
  height: 768px;

  background: #070707;
}
.playlist-menu {
  width: 164px;
  height: 552px;
  top: 44px;
  align-items: flex-start;
  left: 0px;
}
.al-nav-menu-top {
  align-items: flex-start;
  width: 164px;
  height: 108px;
  left: 0px;
  top: 0px;

  /* Inside auto layout ? */
  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 32px 0px;
}
.al-nav-menu-mid {
  width: 164px;
  height: 254px;
  top: 140px;
  align-items: flex-start;
  left: 0px;
  top: 140px;

  /* Inside auto layout */
  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 32px 0px;
}
.al-nav-menu-bottom {
  width: 164px;
  align-items: flex-start;
  height: 126px;
  left: 0px;
  top: 426px;

  flex: none;
  order: 2;
  flex-grow: 0;
  margin: 32px 0px;
}
.top-item {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 8px, 20px, 8px, 20px;
  cursor: pointer;
  position: static;
  width: 164px;
  left: 0px;
  top: 0px;
}
.order-0 {
  order: 0;
}
.order-1 {
  order: 1;
  top: 36px;
}
.order-2 {
  order: 2;
  top: 72px;
}
.al-nav-menu-top .home {
  width: 90px;
  height: 20px;
  top: 8px;
  left: 54px;

  font: Circular Std;
  font-weight: 700;
  font-style: normal;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.25px;
  color: #ffffff;

  flex: none;
  order: 1;
  flex-grow: 1;
  margin: 0px 14px;
}

.al-nav-menu-top .browse {
  position: static;
  width: 90px;
  height: 20px;
  left: 54px;
  top: 8px;

  font: Circular Std;
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  letter-spacing: 0.25px;

  color: #ffffff;

  /* Inside auto layout */
  cursor: pointer;
  flex: none;
  order: 1;
  flex-grow: 1;
  margin: 0px 14px;
}

.al-nav-menu-top .radio {
  position: static;
  width: 90px;
  height: 20px;
  left: 54px;
  top: 8px;

  font: Circular Std;
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  letter-spacing: 0.25px;

  color: #ffffff;

  /* Inside auto layout */
  cursor: pointer;
  flex: none;
  order: 1;
  flex-grow: 1;
  margin: 0px 14px;
}
.icon {
  height: 13.3px;
  width: 13.3px;
  left: 3.3px;
  top: 3.3px;
  border-radius: 0px;
  position: static;
  left: 16.67%;
  right: 16.67%;
  top: 16.67%;
  bottom: 16.67%;
  cursor: pointer;
  color: #ffffff;
}
.mid-header {
  position: static;
  width: 124px;
  height: 18px;
  left: 20px;
  top: 6px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 18px;
  /* identical to box height, or 180% */

  letter-spacing: 0.4px;
  color: #ababab;
  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 1;
  margin: 0px 14px;
}
.mid-menu-item {
  align-items: center;
  padding: 6px 20px;

  width: 164px;
  height: 32px;
  left: 0px;
  top: 30px;

  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 0px;
  cursor: pointer;
}
.mid-menu-item span {
  position: static;
  width: 124px;
  height: 20px;
  left: 20px;
  top: 6px;

  font: Circular Std;
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  letter-spacing: 0.25px;

  color: #ababab;

  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 1;
  margin: 0px 14px;
  cursor: pointer;
}
.bottom-header {
  align-items: center;
  padding: 6px 20px;

  width: 164px;
  height: 30px;
  left: 0px;
  top: 0px;

  /* Inside auto layout */

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 0px;
}
.bottom-header span {
  position: static;
  width: 124px;
  height: 18px;
  left: 20px;
  top: 6px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 10px;
  line-height: 18px;
  /* identical to box height, or 180% */

  letter-spacing: 0.4px;
  text-transform: uppercase;

  color: #ababab;

  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 1;
  margin: 0px 14px;
}
.bottom-item {
  align-items: center;
  padding: 6px 20px;
  width: 164px;
  height: 32px;
  left: 0px;
  top: 30px;

  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 0px;
  cursor: pointer;
}
.bottom-item {
  position: static;
  width: 124px;
  height: 20px;
  left: 20px;
  top: 6px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  letter-spacing: 0.25px;

  color: #ababab;

  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 1;
  margin: 0px 14px;

  cursor: pointer;
}
</style>
