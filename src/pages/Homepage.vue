<template>
  <div class="h">
    <div class="column align-center">
      <div
        :style="parallaxMouse"
        style="margin-top: 15vh"
        class="column align-center"
      >
        <p :style="titleStyle" class="title">PLEASE</p>
        <p :style="titleStyle" class="sub-title">
          SCROLL DOWN
        </p>
      </div>
    </div>
    <div :style="desc1" style="margin-top: 50vh" class="column align-center">
      <div
        @mouseover="isOverBox1 = true"
        @mouseout="isOverBox1 = false"
        class="description-box"
      >
        <p>Hi, I'm Suttipong Pramuansin.</p>
        <p class="sub-text-1">► IoT & Frontend Developer</p>
        <p class="sub-text-1">► s.pramuansin@gmail.com</p>
        <p class="sub-text-1">► +66 94 591 9532</p>

        <div
          v-if="!isOverBox1"
          style="margin-top: 5vh"
          class="row justify-center"
        >
          <a
            href="https://www.facebook.com/77ayfishermanfriend/"
            target="_blank"
            ><img class="sc-icon" src="../assets/fb.png"
          /></a>
          <a
            href="https://www.instagram.com/77ayfishermanfriend/"
            target="_blank"
            ><img class="sc-icon" src="../assets/ig.png"
          /></a>
          <a href="https://github.com/P-Suttipong" target="_blank"
            ><img class="sc-icon" src="../assets/gh.png"
          /></a>
        </div>
        <div v-else style="margin-top: 5vh" class="row justify-center">
          <a
            href="https://www.facebook.com/77ayfishermanfriend/"
            target="_blank"
            ><img class="sc-icon" src="../assets/fbcolor.png"
          /></a>
          <a
            href="https://www.instagram.com/77ayfishermanfriend/"
            target="_blank"
            ><img class="sc-icon" src="../assets/igcolor.png"
          /></a>
          <a href="https://github.com/P-Suttipong" target="_blank"
            ><img class="sc-icon" src="../assets/ghcolor.png"
          /></a>
        </div>
      </div>
    </div>
    <div
      :style="desc1"
      style="margin-top: 10vh"
      class="row justify-center profile-border"
    >
      <div :style="fadeInImg" class="flip-box">
        <div class="flip-box-inner">
          <div class="flip-box-front">
            <img class="profile-img" src="../assets/profile.png" />
          </div>
          <div class="flip-box-back">
            <img class="profile-img" src="../assets/slogan.png" />
          </div>
        </div>
      </div>
      <!-- <img :style="fadeInImg" class="profile-img" src="../assets/profile.png" /> -->
    </div>
    <div class="row justify-center">
      <img :style="rotation" class="nb-cover" src="../assets/nbcover.png" />
      <img class="nb-base" src="../assets/nb-base.png" />
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  created() {
    window.addEventListener("scroll", this.handleScroll);
    window.addEventListener("mousemove", this.handleMouse);
  },
  unmounted() {
    window.removeEventListener("scroll", this.handleScroll);
    window.removeEventListener("mousemove", this.handleMouse);
  },
  setup() {
    const showP = ref(false);
    return { showP };
  },
  data() {
    return {
      isOverBox1: false,
      isGlow: false,
      date: new Date(),
      titleStyle: { opacity: 1 },
      desc1: { opacity: 0 },
      rotation: {
        transform: `rotate(0deg)`,
        "transform-origin": "center left",
      },
      parallaxMouse: {
        "margin-left": "0px",
      },
      fadeInImg: "",
    };
  },
  methods: {
    handleScroll() {
      // console.log("X: " + window.scrollX + " " + "Y: " + window.scrollY);
      this.titleStyle.opacity = 1 - window.scrollY / 350;
      if (window.scrollY <= 300) {
        this.rotation.transform = `rotate(0deg)`;
        this.desc1.opacity = 0;
      } else if (window.scrollY > 300 && window.scrollY < 391) {
        this.rotation.transform = `rotate(${300 - window.scrollY}deg)`;
        this.desc1.opacity = window.scrollY / 350 - 1;
      } else if (window.scrollY >= 391) {
        this.rotation = {
          "transform-origin": "center left",
          transform: `rotate(270deg)`,
        };
        this.isGlow = true;
        this.desc1.opacity = 1;
      }
      if (window.scrollY >= 650) {
        this.fadeInImg = "animation: slideUp 2s";
      } else {
        this.fadeInImg = "";
      }
    },
    handleMouse(e) {
      if (window.innerWidth > 600) {
        this.parallaxMouse = {
          "margin-left": `${200 - e.screenX / 10}px`,
        };
      }
    },
  },
  mounted() {
    this.showP = true;
  },
  components: {},
};
</script>

<style lang="scss">
@import "../assets/_global.scss";
.title {
  font-size: 10vw;
  // margin-bottom: -5vh;
  font-weight: bold;
  color: white;
}
.sub-title {
  font-size: 4.7vw;
  margin-bottom: -5vh;
  font-weight: bold;
  color: white;
}
.sub-text-1 {
  font-size: 2vw;
}
.nb-cover {
  margin-top: 5vh;
  width: 80vw;
  position: fixed;
  bottom: 70px;
}
.nb-base {
  margin-top: 5vh;
  width: 80vw;
  position: fixed;
  bottom: 0;
}
.sc-icon {
  width: 5vw;
  margin: 0px 20px;
}
.description-box {
  color: white;
  font-size: 3vw;
  border: 2px solid white;
  padding: 10px 30px;
  border-radius: 15px;
}
.description-box:hover {
  // box-shadow: 0px 0px 30px rgba($color: #da00bd, $alpha: 0.6);
  animation: glowing 2s infinite;
}
.profile-img {
  width: 15vw;
}
@keyframes glowing {
  0% {
    box-shadow: 0px 0px 90px rgba($color: #da00bd, $alpha: 0.4);
  }
  50% {
    box-shadow: 0px 0px 90px rgba($color: #4605f8, $alpha: 0.4);
  }
  100% {
    box-shadow: 0px 0px 90px rgba($color: #da00bd, $alpha: 0.4);
  }
}
@keyframes slideUp {
  0% {
    margin-top: 200px;
    opacity: 0.1;
  }
  100% {
    margin-top: 0px;
    opacity: 1;
  }
}
.h {
  height: 300vh;
}
.flip-box {
  background-color: transparent;
  width: 15vw;
  height: 15vw;
  border: 2px solid #f1f1f1;
  padding: 20px;
  border-radius: 15px;
  perspective: 1000px;
}

.flip-box-inner {
  position: relative;
  width: 15vw;
  height: 15vw;
  text-align: center;
  transition: transform 1s;
  transform-style: preserve-3d;
}

.flip-box:hover .flip-box-inner {
  transform: rotateY(180deg);
}

.flip-box-front,
.flip-box-back {
  position: absolute;
  width: 15vw;
  height: 15vw;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
}

.flip-box-front {
  background-color: #bbb;
}

.flip-box-back {
  transform: rotateY(180deg);
}

@media only screen and (max-width: 600px) {
  .title {
    margin-top: 20vh;
    margin-bottom: 0px;
    font-size: 18vw;
    font-weight: bold;
    color: white;
  }
  .sub-title {
    font-size: 8vw;
    margin-bottom: -5vh;
    font-weight: bold;
    color: white;
  }
  .nb-cover {
    width: 90vw;
    position: fixed;
    bottom: 20px;
  }
  .nb-base {
    width: 90vw;
    position: fixed;
    bottom: 0;
  }
  .description-box {
    width: 60vw;
    color: white;
    font-size: 8vw;
    border: 2px solid white;
    padding: 20px 20px;
    border-radius: 15px;
    animation: glowing 4s infinite;
  }
  .sub-text-1 {
    font-size: 3.5vw;
  }
  .sc-icon {
    width: 10vw;
    margin: 0px 10px;
  }
  .profile-img {
    width: 60vw;
  }
  .flip-box {
    width: 60vw;
    height: 60vw;
    background-color: transparent;
    border: 2px solid #f1f1f1;
    padding: 20px;
    border-radius: 15px;
    perspective: 1000px;
  }

  .flip-box-inner {
    background-color: transparent;
    position: absolute;
    transition: transform 1s;
    transform-style: preserve-3d;
  }

  .flip-box:focus .flip-box-inner {
    transform: rotateY(180deg);
  }

  .flip-box-front,
  .flip-box-back {
    position: absolute;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
  }

  .flip-box-back {
    z-index: 50;
    transform: rotateY(180deg);
  }
}
</style>
