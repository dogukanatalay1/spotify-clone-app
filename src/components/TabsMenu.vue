<template>
  <div class="tabs-menu position-absolute">
    <div class="tabs d-flex flex-row position-absolute">
      <div class="tab-0 d-flex flex-column align-items-center position-static">
        <div class="tab-0-child">
          <p>OVERVİEW</p>
          <hr class="indicator" />
        </div>
      </div>
      <div class="tab-1 d-flex flex-column align-items-center position-static">
        <div class="tab-1-child">
          <p>FANS ALSO LIKE</p>
        </div>
      </div>
      <div class="tab-2 d-flex flex-column align-items-center position-static">
        <div class="tab-2-child">
          <p>ABOUT</p>
        </div>
      </div>
      <div class="tab-3 d-flex flex-column align-items-center position-static">
        <div class="tab-3-child">
          <p>CONCERTS</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.tabs-menu {
  height: 42px;
  width: 1008px;
  border-radius: 0px;
  background: #0a0a0a;
  top: 224px;
  left: 164px;
  bottom: 502px;
  right: 194px;
}
.tabs {
  padding: 0px;
  width: 445px;
  height: 42px;
  left: 28px;
  top: 0px;
}
.tab-0 {
  padding: 12px 16px 0px;
  width: 107px;
  height: 42px;
  left: 0px;
  bottom: 0px;
  /* Inside auto layout */
  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 0px;
}
.tab-1 {
  padding: 12px 16px 0px;
  width: 146px;
  height: 42px;
  left: 107px;
  bottom: 0px;
  /* Inside auto layout */
  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 0px;
}
.tab-2 {
  padding: 12px 16px 0px;
  width: 81px;
  height: 42px;
  left: 253px;
  bottom: 0px;
  /* Inside auto layout */
  flex: none;
  order: 2;
  flex-grow: 0;
  margin: 0px 0px;
}
.tab-3 {
  padding: 12px 16px 0px;
  width: 111px;
  height: 42px;
  left: 334px;
  bottom: 0px;
  /* Inside auto layout */
  flex: none;
  order: 3;
  flex-grow: 0;
  margin: 0px 0px;
}
.tab-3-child {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0px;
  position: static;
  width: 79px;
  height: 20px;
  left: 16px;
  top: 12px;
  /* Inside auto layout */
  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 8px 0px;
}
.tab-3 .tab-3-child p {
  position: static;
  width: 79px;
  height: 20px;
  left: 0px;
  top: 0px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */
  text-align: center;
  letter-spacing: 0.25px;
  text-transform: uppercase;

  /* Black -> Grey/#CCCCCC - 100% */

  color: #cccccc;
  /* Inside auto layout */
  cursor: pointer;
  flex: none;
  order: 1;
  flex-grow: 0;
  margin: px 8px;
  cursor: pointer;
}
.tab-2-child {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0px;
  position: static;
  width: 49px;
  height: 20px;
  left: 16px;
  top: 12px;
  /* Inside auto layout */
  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 8px 0px;
}
.tab-2 .tab-2-child p {
  position: static;
  width: 49px;
  height: 20px;
  left: 0px;
  top: 0px;
  cursor: pointer;
  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 20px;
  text-align: center;
  letter-spacing: 0.25px;
  text-transform: uppercase;
  color: #cccccc;
  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: px 8px;
}
.tab-1-child {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0px;

  position: static;
  width: 114px;
  height: 20px;
  left: 16px;
  top: 12px;
  /* Inside auto layout */
  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 8px 0px;
}
.tab-1 .tab-1-child p {
  position: static;
  width: 114px;
  height: 20px;
  left: 0px;
  top: 0px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 20px;
  cursor: pointer;
  text-align: center;
  letter-spacing: 0.25px;
  text-transform: uppercase;

  color: #cccccc;
  flex: none;
  order: 1;
  flex-grow: 0;
  margin: px 8px;
}
.tab-0-child {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0px;

  position: static;
  width: 75px;
  height: 30px;
  left: 16px;
  top: 12px;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 8px 0px;
}
.tab-0 .tab-0-child p {
  position: absolute;
  width: 75px;
  height: 20px;
  margin-left: 0px;
  top: -5px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 20px;
  cursor: pointer;

  text-align: center;
  letter-spacing: 0.25px;
  text-transform: uppercase;

  color: #09d89d;
  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 17.2px 8px;
}
.indicator {
  position: static;
  width: 43px;
  height: 2px;
  left: 16px;
  bottom: 0px;

  /* Shade Green / #08C08C - 10% */

  background: #09d89d;

  /* Inside auto layout */

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 8px 0px;
}
</style>
