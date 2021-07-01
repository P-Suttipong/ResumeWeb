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
          SCROLL TO OPEN
        </p>
      </div>
    </div>
    <div
      :style="desc1"
      style="margin-top: 50vh"
      class="row justify-center profile-border"
    >
      <div class="glowing" :style="fadeInImg">
        <FlipCard></FlipCard>
      </div>
    </div>
    <div :style="desc1" style="margin-top: 10vh" class="column align-center">
      <div
        @mouseover="isOverBox1 = true"
        @mouseout="isOverBox1 = false"
        class="description-box"
      >
        <p>Hi, I'm Suttipong Pramuansin</p>
        <!-- <p class="sub-text-1">► IoT & Frontend Developer</p> -->
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
    <div :style="desc2" class="column align-center" style="margin-top: 20vh">
      <div class="description-box">
        <p>EDUCATION</p>
        <div>
          <p class="sub-text-1 title-bg">► Bachelor's Degree</p>
          <p class="sub-text-2">Prince of Songkla University Phuket Campus</p>
          <p class="sub-text-2">Kathu Phuket Thailand</p>
          <p class="sub-text-2">
            2016 - 2019, Bachelor of Computer Engineering
          </p>
        </div>
        <div style="margin-bottom: 30px">
          <p class="sub-text-1 title-bg">► High School</p>
          <p class="sub-text-2">
            The Demonstration School of Silpakorn University
          </p>
          <p class="sub-text-2">Nakhonpratom Thailand</p>
          <p class="sub-text-2">
            2014 - 2016, Sci & Math Program
          </p>
        </div>
      </div>
    </div>
    <div :style="desc3" class="column align-center" style="margin-top: 20vh">
      <div class="description-box">
        <p>WORK EXPERIENCE</p>
        <div>
          <p class="sub-text-1 title-bg">► Internship @WESERVE LIFESTYLE</p>
          <p class="sub-text-2">Phuket, Thailand</p>
          <p class="sub-text-2">
            May 2020 - July 2020
          </p>
        </div>
        <div>
          <p class="sub-text-1 title-bg">► IoT-Developer @WESERVE LIFESTYLE</p>
          <p class="sub-text-2">Phuket, Thailand</p>
          <p class="sub-text-2">
            July 2020 - Oct 2020
          </p>
        </div>
        <div style="margin-bottom: 30px">
          <p class="sub-text-1 title-bg">
            ► Full-Stack @Andaman Tracking Co., Ltd.
          </p>
          <p class="sub-text-2">Phuket, Thailand</p>
          <p class="sub-text-2">
            Nov 2020 ~
          </p>
        </div>
      </div>
    </div>
    <div :style="desc4" class="column align-center" style="margin-top: 20vh">
      <div class="description-box">
        <p>SKILLS</p>
        <div class="row justify-center">
          <img class="sc-icon" src="../assets/vue.png" />
          <img class="sc-icon" src="../assets/react.png" />
          <img class="sc-icon" src="../assets/sass.png" />
        </div>
        <div style="margin-top: 40px" class="row justify-center">
          <img class="sc-icon" src="../assets/nodejs.png" />
          <img class="sc-icon" src="../assets/nest.png" />
          <img class="sc-icon" src="../assets/python.png" />
        </div>
        <div style="margin-top: 40px" class="row justify-center">
          <img class="sc-icon" src="../assets/firebase.png" />
          <img class="sc-icon" src="../assets/mongo.png" />
          <img class="sc-icon" src="../assets/nodered.png" />
        </div>
        <div style="margin-top: 40px; margin-bottom: 40px" class="row justify-center">
          <img class="sc-icon" src="../assets/ps.png" />
          <img class="sc-icon" src="../assets/arduino.png" />
        </div>
      </div>
    </div>
    <div class="row justify-center">
      <img :style="rotation" class="nb-cover" src="../assets/nbcover.png" />
      <img class="nb-base" src="../assets/nb-base.png" />
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
import FlipCard from "../components/FlipCard.vue";
export default {
  components: { FlipCard },
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
      isShowChart: false,
      isGlow: false,
      date: new Date(),
      titleStyle: { opacity: 1 },
      desc1: { opacity: 0 },
      desc2: { opacity: 0 },
      desc3: { opacity: 0 },
      desc4: { opacity: 0 },
      rotation: {
        transform: `rotate(0deg)`,
        "transform-origin": "center left",
      },
      parallaxMouse: {
        "margin-left": "0px",
      },
      fadeInImg: "margin-top : 1000px",
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
      if (window.scrollY >= 400) {
        this.fadeInImg = "animation: slideUp 2s";
      } else {
        this.fadeInImg = "margin-top : 1000px";
      }
      if (window.scrollY >= 1000) {
        this.desc2 = { animation: "slideLeft 2s" };
      } else {
        this.desc2 = {
          "margin-left ": " 500px",
          opacity: "0",
        };
      }
      if (window.scrollY >= 1500) {
        this.desc3 = { animation: "slideRight 2s" };
      } else {
        this.desc3 = {
          "margin-right ": " 500px",
          opacity: "0",
        };
      }
      if (window.scrollY >= 2100) {
        this.desc4 = { animation: "slideLeft 2s" };
      } else {
        this.desc4 = {
          "margin-left ": " 500px",
          opacity: "0",
        };
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
.title-bg {
  background: #41238a;
  color: #47e98d;
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
.sub-text-2 {
  font-size: 1.3vw;
}
.nb-cover {
  margin-top: 5vh;
  width: 60vw;
  position: fixed;
  bottom: 6vh;
}
.nb-base {
  margin-top: 5vh;
  width: 60vw;
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
  width: 45vw;
}
.description-box:hover {
  animation: glowing 1s infinite;
}
.chart {
  position: relative;
  height: 30vw;
  width: 30vw;
}
@keyframes glowing {
  0% {
    box-shadow: 0px 0px 60px rgba($color: #41238a, $alpha: 0.8);
  }
  50% {
    box-shadow: 0px 0px 40px rgba($color: #4b1fbb, $alpha: 0.9);
  }
  100% {
    box-shadow: 0px 0px 60px rgba($color: #41238a, $alpha: 0.8);
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
@keyframes slideLeft {
  0% {
    margin-left: 500px;
    opacity: 0.1;
  }
  100% {
    margin-left: 0px;
    opacity: 1;
  }
}
@keyframes slideRight {
  0% {
    margin-right: 500px;
    opacity: 0.1;
  }
  100% {
    margin-right: 0px;
    opacity: 1;
  }
}
.h {
  margin-bottom: 50vh;
}

@media only screen and (max-width: 800px) {
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
  }
  .description-box:focus {
    animation: glowing 4s infinite;
  }
  .sub-text-1 {
    font-size: 3.5vw;
  }
  .sub-text-2 {
    font-size: 2.3vw;
  }
  .sc-icon {
    width: 10vw;
    margin: 0px 10px;
  }
  .chart {
    // position: relative;
    height: 70vw;
    width: 70vw;
  }
}
</style>
