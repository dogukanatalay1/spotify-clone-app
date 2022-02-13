<template>
  <div
    class="trackNav position-absolute"
    ref="trackNav"
    :class="containerClass"
  >
    <!-- Song info  -->
    <div
      class="
        song-info
        d-flex
        flex-row
        align-items-center
        position-absolute
        ml-16px
      "
    >
      <img
        src="../assets/images/Song Cover.png"
        class="track-song-cover"
        alt=""
      />

      <div class="track-song-info d-flex flex-column position-static">
        <div
          class="
            track-song-title
            d-flex
            flex-row
            align-items-center
            position-static
          "
        >
          <span
            class="track-song-name d-flex align-items-center text-align-center"
            >{playbackData.item.name }</span
          >
          <img
            src="../assets/images/heart.png"
            class="track-heart-icon"
            alt=""
          />
        </div>
        <p class="artist-name d-flex position-static align-items-center">
          Artist Name / Singer Collaboration
        </p>
      </div>
    </div>

    <!-- Track info -->
    <div
      class="
        track-middle
        d-flex
        flex-column
        justify-content-center
        align-items-center
        position-absolute
      "
    >
      <div class="track-buttons d-flex flex-row position-static">
        <div class="button-suffle">
          <div class="icon-suffle">Shuffle</div>
        </div>

        <div class="button-prev">
          <div class="prev-playlist-icon">
            <img
              src="../assets/images/Polygon 2.png"
              class="prev-button-icon"
              alt=""
            />
          </div>
        </div>

        <div class="button-play">
          <img src="../assets/images/Polygon 2.png" class="start-icon" alt="" />
        </div>

        <div class="button-next">
          <div class="next-playlist-icon">
            <img
              src="../assets/images/Polygon 2.png"
              class="next-button-icon"
              alt=""
            />
          </div>
        </div>

        <div class="button-repeat">Repeat</div>
      </div>

      <!--  -->

      <div
        class="
          track-duration
          d-flex
          flex-row
          justify-content-center
          align-items-center
          position-static
        "
      >
        <p class="played-time">5:16</p>
        <div class="track-song">
          <div class="track-played"></div>
        </div>
        <p class="total-time">5:41</p>
      </div>
    </div>

    <!-- Other menu nav -->
    <div
      class="
        other-menu
        d-flex
        flex-row
        justify-content-center
        align-items-center
        position-absolute
      "
    ></div>
  </div>
</template>

<script>
// trackNav / track-song / track-played
import SpotifyWebApi from "spotify-web-api-js";
const spotifyApi = new SpotifyWebApi();
//import ref from "vue";
//const containerClass = ref("");
// const trackNav = ref(null);
// const playbackData = ref();

export default {
  methods: {
    getMyCurrentPlayingTrack: function () {
      return spotifyApi.getMyCurrentPlayingTrack();
    },
  },
  mounted() {
   /* getMyCurrentPlayingTrack().then((res) => {
      playbackData.value = res;
    }); */
  },
};
</script>

<style>
.trackNav {
  width: 1366px;
  height: 68px;
  top: 700px;

  height: 68px;
  left: -11px;
  right: 11px;
  bottom: 0px;
  background: #181818;
}
.song-info {
  padding: 0px;
  width: 215px;
  height: 46px;
  left: 16px;
  top: calc(50% - 46px / 2);
}
.track-song-cover {
  position: static;
  width: 46px;
  height: 46px;
  left: 0px;
  top: 0px;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 12px;
}
.track-song-info {
  align-items: flex-start;
  padding: 0px;
  width: 157px;
  height: 34px;
  left: 58px;
  top: 6px;
}
.artist-name {
  width: 157px;
  height: 16px;
  left: 0px;
  top: 18px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 10px;
  line-height: 16px;
  text-align: center;
  color: #ababab;
  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 0px;
  cursor: pointer;
}
.track-song-title {
  padding: 0px;

  width: 142px;
  height: 18px;
  left: 0px;
  top: 0px;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 0px;
  cursor: pointer;
}
.track-song-name {
  position: static;
  width: 118px;
  height: 18px;
  left: 0px;
  top: 0px;
  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 18px;
  letter-spacing: 0.4px;

  color: #ffffff;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 12px;
  cursor: pointer;
}
.track-heart-icon {
  position: static;
  left: 4.17%;
  right: 0.4%;
  top: 8.33%;
  bottom: 7.37%;

  background: #181818;
  cursor: pointer;
}
.track-middle {
  padding: 0px;
  width: 649px;
  height: 49px;
  left: calc(50% - 649px / 2 + 0.5px);
  top: calc(50% - 49px / 2 - 0.5px);
}
.other-menu {
  padding: 0px;
  width: 177px;
  height: 20px;
  right: 150px;
  top: calc(50% - 20px / 2);
  border: 1px dashed red;
}
.track-duration {
  padding: 0px;
  width: 649px;
  height: 13px;
  left: calc(50% - 649px / 2);
  top: calc(50% - 13px / 2 + 18px);

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 8px 0px;
}
.played-time {
  position: static;
  width: 18px;
  height: 13px;
  left: 0px;
  top: 0px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 10px;
  line-height: 13px;
  display: flex;
  align-items: center;
  text-align: right;

  color: #ababab;
  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 9px;
}
.total-time {
  position: static;
  width: 18px;
  height: 13px;
  left: 631px;
  top: 0px;

  font-family: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 10px;
  line-height: 13px;

  display: flex;
  align-items: center;

  color: #ababab;

  flex: none;
  order: 2;
  flex-grow: 0;
  margin: 0px 9px;
}
.track-song {
  position: static;
  width: 595px;
  height: 3px;
  left: 27px;
  top: 5px;

  background: #303030;
  border-radius: 100px;

  flex: none;
  order: 1;
  flex-grow: 1;
  margin: 0px 9px;
  cursor: pointer;
}
.track-played {
  position: relative;
  width: 50%;
  left: 0px;
  top: 0px;
  bottom: 0px;

  background: #ababab;
  border-radius: inherit;
  height: inherit;
}
.track-buttons {
  align-items: flex-start;
  padding: 0px;

  width: 188px;
  height: 28px;
  left: calc(50% - 188px / 2);
  top: calc(50% - 28px / 2 - 10.5px);
  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 6px 0px;
}
.button-suffle {
  position: static;
  width: 28px;
  height: 28px;
  left: 0px;
  top: 0px;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 12px;
}
.button-prev {
  position: static;
  width: 28px;
  height: 28px;
  left: 40px;
  top: 0px;

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 12px;
}
.button-play {
  position: static;
  width: 28px;
  height: 28px;
  left: 80px;
  top: 0px;

  border: 1px solid #a9a9a9;
  box-sizing: border-box;
  border-radius: 1000px;
  cursor: pointer;
  flex: none;
  order: 2;
  flex-grow: 0;
  margin: 0px 12px;
}
.button-next {
  position: static;
  width: 28px;
  height: 28px;
  left: 120px;
  top: 0px;
  flex: none;
  order: 3;
  flex-grow: 0;
  margin: 0px 12px;
}
.button-repeat {
  position: static;
  width: 28px;
  height: 28px;
  left: 160px;
  top: 0px;

  flex: none;
  order: 4;
  flex-grow: 0;
  margin: 0px 12px;
}
.start-icon {
  position: static;
  margin-left: 9px;
  cursor: pointer;
}
.prev-playlist-icon {
  position: absolute;
  width: 20px;
  height: 20px;
  left: calc(50% - 20px / 2);
  top: calc(50% - 20px / 2);
  cursor: pointer;
}

.prev-button-icon {
  position: absolute;
  bottom: 17px;
  right: 22px;
  transform: matrix(-1, 0, 0, 1, 0, 0);
}
.next-playlist-icon {
  position: absolute;
  width: 20px;
  height: 20px;
  cursor: pointer;
}
.next-button-icon {
  position: absolute;
  right: 2px;
  top: 8.5px;
}
.icon-suffle {
  font-size: 10px;
  margin-top: 6px;
  color: #ffffff;
  font: Circular Std;
  cursor: pointer;
}
.button-repeat {
  font-size: 10px;
  margin-top: 6px;
  color: #ffffff;
  font: Circular Std;
  cursor: pointer;
}
</style>
