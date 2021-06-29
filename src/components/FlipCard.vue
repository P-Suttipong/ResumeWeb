<template>
  <div class="flip-box">
    <div class="flip-box-inner">
      <div class="flip-box-front">
        <img class="profile-img" src="../assets/profile.png" />
      </div>
      <div class="flip-box-back">
        <img class="profile-img" src="../assets/slogan.png" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.flip-box {
  background-color: transparent;
  width: 15vw;
  height: 15vw;
  border: 2px solid #fff;
  padding: 20px;
  border-radius: 15px;
  perspective: 1000px;
}

.flip-box:hover {
  animation: glowing 2s infinite;
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
.profile-img {
  width: 15vw;
}

@media only screen and (max-width: 800px) {
  .profile-img {
    width: 60vw;
  }
  .flip-box {
    width: 60vw;
    height: 60vw;
    background-color: transparent;
    border: 2px solid #fff;
    padding: 20px;
    border-radius: 15px;
    perspective: 1000px;
  }
  .flip-box:focus {
    animation: glowing 2s infinite;
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
