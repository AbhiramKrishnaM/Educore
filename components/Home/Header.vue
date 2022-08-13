<template>
  <div
    class="wrapper pa-8 rounded-xl d-flex justify-space-between align-center white--text"
  >
    <div class="background-polygon"></div>

    <h1>
      Your students are doing great <span>60%</span> students has<br />
      completed the test.
    </h1>
    <div class="illustration-wrapper mr-6">
      <div class="halo first"></div>
      <div class="halo second"></div>
      <div class="halo third"></div>

      <v-img
        height="100%"
        width="100%"
        :src="require('@/assets/images/Kid.svg')"
        alt="Kid learning "
        class="image"
      ></v-img>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader',
}
</script>
<style scoped>
.wrapper {
  width: 100%;
  height: 20vh;
  background-color: #4540e1;
  position: relative;
}

h1 {
  font-weight: 300;
  font-size: 27px;
  line-height: 1.4em;
}

span {
  font-weight: bold;
  font-size: 40px;
}

.background-polygon {
  height: 400px;
  width: 200px;
  position: absolute;
  left: 3%;
  background: linear-gradient(117.45deg, #ffffff36 5.89%, #fff0 75.99%);
  clip-path: polygon(0 0, 52% 0, 100% 100%, 75% 100%);
  transform: rotate(-40deg);
}

.illustration-wrapper {
  position: relative;
  height: 210px;
  width: 210px;
}

.image {
  position: absolute;
  bottom: 10%;
}

.halo {
  position: absolute;
  border-radius: 100%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.first {
  width: 230px;
  height: 230px;
  background: linear-gradient(180deg, #ffffff3d 0%, #fff0 100%);
}

.second {
  width: 200px;
  height: 200px;
  background: linear-gradient(180deg, #ffffff1a 0%, #fff0 100%);
}

.third {
  width: 170px;
  height: 170px;
  background: linear-gradient(180deg, #ffffff1f 46.95%, #fff0 100%);
}
</style>
