<template>
  <div class="aside-right position-absolute">
    <div class="activity-list d-flex flex-column position-absolute">
      <p class="activity-topic d-flex align-items-center position-static">
        Friend Activity
      </p>
      <div class="items d-flex flex-column position-static">
        <div class="friends-item">
          <img class="artist-photo" src="../assets/images/artist.png" alt="" />
          <div class="frame-1">
            <div class="friend-listened">
              <p>Friends Name</p>
            </div>
            <p class="played-song">Played Song Name</p>
            <p class="artist-name">Artist Name</p>
          </div>
        </div>
        <div class="friends-item">
          <img class="artist-photo" src="../assets/images/artist.png" alt="" />
          <div class="frame-1">
            <div class="friend-listened">
              <p>Friends Name</p>
            </div>
            <p class="played-song">Played Song Name</p>
            <p class="artist-name">Artist Name</p>
          </div>
        </div>
        <div class="friends-item">
          <img class="artist-photo" src="../assets/images/artist.png" alt="" />
          <div class="frame-1">
            <div class="friend-listened">
              <p>Friends Name</p>
            </div>
            <p class="played-song">Played Song Name</p>
            <p class="artist-name">Artist Name</p>
          </div>
        </div>
        <div class="friends-item">
          <img class="artist-photo" src="../assets/images/artist.png" alt="" />
          <div class="frame-1">
            <div class="friend-listened">
              <p>Friends Name</p>
            </div>
            <p class="played-song">Played Song Name</p>
            <p class="artist-name">Artist Name</p>
          </div>
        </div>
        <div class="friends-item">
          <img class="artist-photo" src="../assets/images/artist.png" alt="" />
          <div class="frame-1">
            <div class="friend-listened">
              <p>Friends Name</p>
            </div>
            <p class="played-song">Played Song Name</p>
            <p class="artist-name">Artist Name</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.aside-right {
  width: 194px;
  height: 700px;
  left: 1172px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  background: #070707;
}
.activity-list {
  align-items: flex-start;
  padding: 0px;
  width: 170px;
  height: 761px;
  left: 12px;
  top: 12px;
}
.activity-topic {
  height: 20px;
  left: 0px;
  right: 0px;
  top: 0px;

  font: Circular Std;
  font-style: normal;
  font-weight: 900;
  font-size: 14px;
  line-height: 20px;

  letter-spacing: 0.25px;

  color: #ffffff;

  flex: none;
  order: 0;
  align-self: stretch;
  flex-grow: 0;
  margin: 16px 0px;
}
.items {
  align-items: flex-start;
  padding: 0px;
  width: 170px;
  height: 708px;
  left: 0px;
  top: 53px;
  flex: none;
  order: 2;
  align-self: stretch;
  flex-grow: 0;
  margin: 16px 0px;
}
.friends-item {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0px;

  position: static;
  width: 170px;
  height: 84px;
  left: 0px;
  top: 520px;

  flex: none;
  flex-grow: 0;
  margin: 20px 0px;
  cursor: pointer;
}
.artist-photo {
  position: static;
  width: 36px;
  height: 36px;
  margin-left: 0px;
  top: 24px;
  flex: none;
  flex-grow: 0;
  margin: 0px 6px;
  border: 1px solid #fff;
  border-radius: 900px;
  margin-right: 0px;
}
.frame-1 {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 0px;

  position: static;
  width: 120px;
  height: 84px;
  left: 50px;
  top: 0px;

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 14px;
}
.friend-listened {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0px;

  position: static;
  width: 120px;
  height: 32px;
  left: 0px;
  top: 0px;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 0px;
}
.friend-listened p {
  position: static;
  width: 96px;
  height: 32px;
  left: 0px;
  top: 0px;

  font: Circular Std;
  font-style: normal;
  font-weight: bold;
  font-size: 12px;
  line-height: 16px;
  /* or 133% */
  display: flex;
  align-items: center;

  color: #ffffff;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 4px;
}
.played-song {
  position: static;
  width: 85px;
  height: 16px;
  left: 0px;
  top: 48px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 10px;
  line-height: 16px;
  /* identical to box height, or 160% */

  display: flex;
  align-items: center;

  color: #ababab;

  /* Inside auto layout */

  flex: none;
  order: 2;
  flex-grow: 0;
  margin: 0px 0px;
}
.artist-name {
  position: static;
  width: 55px;
  height: 16px;
  left: 0px;
  top: 32px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 10px;
  line-height: 16px;

  display: flex;
  align-items: center;

  color: #ababab;

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 0px;
}
</style>
