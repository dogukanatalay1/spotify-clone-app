<template>
  <div class="hero position-absolute">
    <img class="background-img" src="../assets/images/hero.png" alt="" />
    <div class="hero-nav">
      <img
        class="vector-horizental"
        src="../assets/images/Vector (Stroke) (2).png"
        alt=""
      />

      <img
        class="vector-horizental"
        src="../assets/images/Vector (Stroke) (1).png"
        alt=""
      />

      <input type="text" class="search-box" placeholder="Search" />

      <div
        class="artist-item d-flex flex-row align-items-center position-absolute"
      >
        <button @click="loginSpotify" class="sign-in">Sign With Spotify</button>

        <img src="../assets/images/artist.png" alt="" />
        <p class="artist-item-name">Ilham Anasruloh</p>
      </div>
    </div>

    <img src="../assets/images/vectordown.png" class="vector-down" alt="" />

    <div class="head-title d-flex flex-column position-absolute">
      <div class="nav-menu d-flex flex-row align-items-center position-static">
        <span class="span-artist"></span>
      </div>

      <p class="artist-name">Eunoia Monica</p>

      <!-- Hero buttons -->
      <div class="hero-buttons d-flex flex-row position-static">
        <button class="play-button d-flex flex-row">
          <span class="d-flex position-static mt-8 mb-8 mr-36"> PLAY </span>
        </button>
        <button class="follow-button d-flex flex-row ml-125 mt-12">
          <span> FOLLOW </span>
        </button>
        <button class="other-button d-flex flex-row ml-125 mt-12">
          <span> </span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import queryString from "query-string";

export default {
  data() {
    return {};
  },
  mounted() {
    // The code block that is going to be executed when the app or the component loaded
    const urlSearchParams = new URLSearchParams(window.location.search);
    const params = Object.fromEntries(urlSearchParams.entries());

    if (!params.code) {
      return;
    }
    axios
      .post(
        "https://accounts.spotify.com/api/token",
        queryString.stringify({
          code: params.code,
          redirect_uri: process.env.VUE_APP_REDIRECT_URI,
          grant_type: "authorization_code",
        }),
        {
          headers: {
            "Content-Type": "application/x-www-form-urlencoded",
            Authorization:
              "Basic " +
              new Buffer(
                process.env.VUE_APP_CLIENT_ID +
                  ":" +
                  process.env.VUE_APP_CLIENT_SECRET
              ).toString("base64"),
          },
        }
      )
      .then((res) => {
        localStorage.setItem('access_token', res.data.access_token);
        // later, we call access_token in Playlists.vue 
        console.log(res);
      });
  },
  methods: {
    loginSpotify() {
      const url = "https://accounts.spotify.com/authorize";
      let params = {
        response_type: "code",
        client_id: process.env.VUE_APP_CLIENT_ID,
        scope: "user-read-private user-read-email",
        redirect_uri: process.env.VUE_APP_REDIRECT_URI,
        show_dialog: true,
      };
      params = new URLSearchParams(params).toString();
      window.location.href = `${url}?${params}`;
    },
  },
};
</script>

<style scoped>
.hero {
  height: 224px;
  width: 1008px;
  left: 164px;
  top: 0px;
  border-radius: 0px;
  right: 194px;

  background: #ffffff;
}

.hero-nav {
  position: absolute;
  height: 39px;
  left: 0px;
  right: 0px;
  top: 0px;
  width: 1008px;
  height: 39px;
}
.head-title {
  align-items: flex-start;
  padding: 0px;
  width: 484px;
  height: 159px;
  left: 28px;
  top: 39px;
}
.hero-buttons {
  align-items: center;
  padding: 0px 0px 0px;
  width: 286px;
  height: 48px;
  left: 0px;
  top: 111px;

  flex: none;
  order: 2;
  flex-grow: 0;
  margin: 0px 0px;
}
.play-button {
  justify-content: center;
  align-items: center;
  padding: 8px;

  position: static;
  width: 111px;
  height: 36px;
  left: 0px;
  top: 12px;

  background: #0db145;
  border-radius: 1000px;

  border: none;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 0px;
}
.play-button span {
  font: Circular Std;
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 20px;

  align-items: center;
  text-align: center;
  letter-spacing: 1.25px;
  text-transform: capitalize;

  color: #ffffff;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 4px;
}
.follow-button {
  justify-content: center;
  align-items: center;
  padding: 8px;

  position: static;
  width: 111px;
  height: 36px;

  border: 1px solid #fcfcfc;
  box-sizing: border-box;
  border-radius: 1000px;

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 6px;

  background-color: Transparent;
  background-repeat: no-repeat;
  cursor: pointer;
  overflow: hidden;
}
.follow-button span {
  font: Circular Std;
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 20px;

  align-items: center;
  text-align: center;
  letter-spacing: 1.25px;
  text-transform: capitalize;

  color: #ffffff;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 4px;
}
.other-button {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 8px;

  position: static;
  width: 37px;
  height: 36px;
  left: 230px;
  top: 12px;

  border: 1px solid #fcfcfc;
  box-sizing: border-box;
  border-radius: 1000px;

  flex: none;
  order: 2;
  flex-grow: 0;
  margin: -5px 10px;
  background-color: Transparent;
  background-repeat: no-repeat;
  cursor: pointer;
  overflow: hidden;
}
.nav-menu {
  padding: 0px;
  width: 85px;
  height: 20px;
  left: 0px;
  top: 0px;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 0px;
}
.artist-name {
  position: relative;
  width: 484px;
  height: 91px;
  left: 0px;
  top: 60px;
  font: Circular Std;
  font-style: normal;
  font-weight: 900;
  font-size: 68px;

  letter-spacing: -1.5px;

  color: #ffffff;

  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 8px 0px;
}
.span-artist {
  position: static;
  width: 51px;
  height: 18px;
  left: 34px;
  top: 1px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 18px;

  letter-spacing: 0.4px;

  color: #ffffff;

  flex: none;
  order: 1;
  flex-grow: 1;
  margin: 0px 14px;
}
.search-box {
  height: 20px;
  width: 142px;
  left: 68px;
  top: 9px;
  border-radius: 1000px;
  padding: 1px, 4px, 1px, 4px;
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 1px 4px;

  position: absolute;
  width: 142px;
  height: 20px;
  left: 68px;
  top: calc(50% - 20px / 2 - 0.5px);

  background: #ffffff;
  border-radius: 1000px;
  border: none;
}
.vector-horizental {
  height: 14px;
  width: 8px;
  margin-left: 13px;
  margin-top: 5px;
  cursor: pointer;
  border-radius: 0px;
}
.artist-item {
  padding: 0px;
  width: 121px;
  height: 24px;
  right: 185px;
  top: calc(50% - 24px / 2 - 0.5px);
  cursor: pointer;
}
.artist-item-name {
  position: static;
  width: 93px;
  height: 18px;
  left: 28px;
  top: 3px;

  font: Circular Std;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 18px;

  display: flex;
  align-items: center;
  letter-spacing: 0.4px;

  color: #ffffff;

  text-shadow: 0.5px 0.8px 0.4px #000000;
  flex: none;
  order: 1;
  flex-grow: 0;
  margin: 0px 4px;
}
.vector-down {
  height: 8px;
  width: 14px;
  left: 980px;
  top: 14px;
  border-radius: 0px;
  position: absolute;
  cursor: pointer;
}
.sign-in {
  justify-content: center;
  align-items: center;
  padding: 8px;

  position: static;
  width: 150px;
  height: 36px;
  left: 0px;
  top: 12px;
  margin-right: 30px;
  background: #0db145;
  border-radius: 1000px;
  color: #ffffff;
  border: none;

  flex: none;
  order: 0;
  flex-grow: 0;
  margin: 0px 0px;
}
</style>
