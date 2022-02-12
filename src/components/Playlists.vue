<template>
  <div class="popular-section d-flex flex-column p-0">
    <p class="section-title d-flex align-items-center position-static">
      Playlists
    </p>

    <div
      class="items d-flex flex-column position-static"
      v-for="(playlist, index) in playlists"
      :key="playlist.id"
    >
      <div class="song-item d-flex flex-row align-items-center position-static">
        <img
          :src="
            playlist.images.length > 0 ? playlist.images[0].url : unknownUrl
          "
          class="song-cover"
          alt=""
        />
        <p
          class="no position-static d-flex align-items-center text-align-center"
        >
          {{ index + 1 }}
        </p>
        <div class="icon">
          <img src="../assets/images/heart.png" class="heart-icon" alt="" />
        </div>

        <span class="song-title position-static d-flex align-items-center">
          {{ playlist.name }}
        </span>
        <span class="total-played position-static d-flex align-items-center">
          {{ playlist.owner.display_name }}
        </span>
      </div>

      <div class="divider">
        <img src="../assets/images/divider.png" class="divider-cross" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
import SpotifyWebApi from "spotify-web-api-js";

export default {
  data() {
    return {
      playlists: [],
      unknownUrl: require("../assets/images/Song Cover.png"),
    };
  },

  mounted() {
    const spotifyApi = new SpotifyWebApi();

    spotifyApi.setAccessToken(localStorage.getItem("access_token"));

    spotifyApi.getUserPlaylists().then((res) => {
      this.playlists = res.items;
      console.log(res);
    });
  },
};
</script>

<style scoped>
.popular-section {
  height: 227px;
  width: 630px;
  margin-left: 192px;
  margin-top: 428px;
  border-radius: 0px;
  align-items: flex-start;
  background: #0a0a0a;
  box-shadow: 0px 8px 88px 30px rgba(0, 0, 0, 0.3);
}
.section-title {
  width: 52px;
  height: 20px;
  left: 0px;
  top: 0px;

  font: Circular Std;
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 20px;

  letter-spacing: 0.25px;

  color: #ffffff;
  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 8px 0px;
}
.items {
  align-items: flex-start;
  padding: 0px;

  width: 630px;
  height: 199px;
  left: 0px;
  top: 28px;
  order: 1;
  flex-grow: 0;
  margin: 8px 0px;
}
.song-item {
  padding: 0px 12px 0px 0px;

  width: 630px;
  height: 32px;
  left: 0px;
  top: 1px;

  flex: none;
  order: 1;
  align-self: stretch;
  flex-grow: 0;
  margin: 0px 0px;
  cursor: pointer;
}
.song-cover {
  position: static;
  width: 32px;
  height: 32px;
  left: 0px;
  top: 0px;
  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 12px;
}
.no {
  width: 5px;
  height: 18px;
  left: 44px;
  top: 7px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 18px;
  letter-spacing: 0.4px;

  color: #ffffff;
  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 12px;
}
.icon {
  position: static;
  width: 32px;
  height: 32px;
  left: 61px;
  top: 0px;
  flex: none;
  order: 2;
  flex-grow: 0;
  margin: 0px 12px;
}
.heart-icon {
  position: static;
  width: 12px;
  height: 12px;
  margin-left: 8px;
  cursor: pointer;
}
.song-title {
  width: 360px;
  height: 18px;
  left: 105px;
  top: 7px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 18px;
  letter-spacing: 0.4px;
  color: #ffffff;
  flex: none;
  order: 3;
  flex-grow: 0;
  margin: 0px 12px;
}
.total-played {
  width: 61px;
  height: 18px;
  left: 540px;
  top: 7px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 18px;
  letter-spacing: 0.4px;
  color: #ffffff;

  flex: none;
  order: 4;
  flex-grow: 0;
  margin: 0px 12px;
  text-align: center;
}
.divider {
  position: static;
  width: 630px;
  height: 1px;
  left: 0px;
  top: 198px;
  flex: none;
  order: 12;
  align-self: stretch;
  flex-grow: 0;
  margin: 0px 0px;
}
.divider-cross {
  position: absolute;
  left: 0%;
  right: 0%;
  top: 0%;
  bottom: 0%;
  background: #1a1a1a;
  mix-blend-mode: normal;
}
</style>

