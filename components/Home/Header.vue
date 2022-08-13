<template>
  <div class="wrapper pa-8 rounded-xl d-flex align-center white--text">
    <h1>
      Your students are doing great <span>60%</span> students has<br />
      completed the test.
    </h1>

    <div class="background-polygon"></div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader',
}
</script>
<style scoped>
.wrapper {
  z-index: 10;
  width: 100%;
  height: 20vh;
  overflow: hidden;
  background-color: #4540e1;
  position: relative;
}

h1 {
  z-index: 12;
  font-weight: 300;
  font-size: 30px;
  line-height: 1.4em;
}

span {
  font-weight: bold;
  font-size: 40px;
}

.background-polygon {
  z-index: 11;
  height: 400px;
  width: 200px;
  position: absolute;
  left: 3%;
  background: linear-gradient(117.45deg, #ffffff36 5.89%, #fff0 75.99%);
  clip-path: polygon(0 0, 52% 0, 100% 100%, 75% 100%);
  transform: rotate(-40deg);
}
</style>
