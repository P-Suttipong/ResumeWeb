<template>
  <div class="h">
    <div class="column align-center">
      <div style="margin-top: 20vh" class="column align-center">
        <p :style="titleStyle" class="title">PLEASE</p>
        <p :style="titleStyle" style="font-size: 4.6vw" class="title">
          SCROLL DOWN
        </p>
      </div>
    </div>
    <div :style="desc1" style="margin-top: 50vh" class="column align-center">
      <p class="description-text">Hi, I'm Suttipong Pramuansin.</p>
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
  },
  unmounted() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  setup() {
    const showP = ref(false);
    return { showP };
  },
  data() {
    return {
      isGlow: false,
      titleStyle: { opacity: 1 },
      desc1: { opacity: 0 },
      rotation: {
        transform: `rotate(0deg)`,
        "transform-origin": "center left",
      },
    };
  },
  methods: {
    handleScroll() {
    //   console.log(window.scrollY);
      this.titleStyle.opacity = 1 - window.scrollY / 350;
      if (window.scrollY <= 300) {
        this.rotation.transform = `rotate(0deg)`;
        this.desc1.opacity = 0;
      } else if (window.scrollY > 300 && window.scrollY < 391) {
        this.rotation.transform = `rotate(${300 - window.scrollY}deg)`;
        this.desc1.opacity = 0;
      } else if (window.scrollY >= 391) {
        this.rotation = {
          "transform-origin": "center left",
          transform: `rotate(270deg)`,
        };
        this.isGlow = true;
        this.desc1.opacity = 1;
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
  //   margin-top: 5vh;
  margin-bottom: -5vh;
  font-size: 10vw;
  font-weight: bold;
  color: white;
}
.suttipong {
  margin-top: 100px;
  margin-bottom: 0px;
  font-size: 16vw;
  font-weight: bold;
  color: white;
}
.pramuansin {
  font-size: 14vw;
  font-weight: bold;
  color: white;
}
.continue-btn {
  z-index: 10;
  position: relative;
  bottom: 100px;
  color: #fff;
}
.nb-cover {
  margin-top: 5vh;
  //   width: 90vw;
  position: fixed;
  bottom: 70px;
}
.nb-base {
  margin-top: 5vh;
  //   width: 90vw;
  position: fixed;
  bottom: 0;
}
.description-text {
  color: white;
  font-size: 3vw;
}
.h {
  height: 300vh;
}

@media only screen and (max-width: 600px) {
  .title {
    margin-top: 20vh;
    margin-bottom: 0px;
    font-size: 50vw;
    font-weight: bold;
    color: white;
  }
}
</style>
