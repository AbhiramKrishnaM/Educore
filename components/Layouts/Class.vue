<template>
  <div class="wrapper d-flex justify-center align-center">
    <div class="circle-1 common"></div>
    <div class="circle-2 common"></div>
    <div class="circle-3 common"></div>

    <section
      class="white--text d-flex flex-column align-center justify-space-around text-center"
    >
      <div class="icon-wrapper d-flex align-center mb-4">
        <v-img
          aspect-ratio="1.6"
          contain
          :src="require('@/assets/images/classroom.png')"
        ></v-img>
      </div>
      <h1 class="mb-7">
        Create instant live <br />
        class now
      </h1>
      <v-btn
        depressed
        rounded
        class="shadow-default"
        v-text="'Create class'"
      ></v-btn>
    </section>
  </div>
</template>
<script>
export default {
  name: 'ClassComponent',
}
</script>

<style scoped>
h1 {
  font-size: 20px;
  font-weight: 300;
}

.wrapper {
  height: 250px;
  background: #4641e1;
  border-radius: 35px;
  position: relative;
  overflow: hidden;
}

.common {
  position: absolute;
  width: 300px;
  height: 300px;
  border-radius: 100%;
}

.circle-1 {
  bottom: 30%;
  right: 10%;
  background: #d9d9d90a;
}

.circle-2 {
  bottom: 30%;
  left: 10%;
  background: linear-gradient(307.38deg, #ffffff15 25.07%, #d9d9d900 61.39%);
}

.circle-3 {
  z-index: -1;
  bottom: 10%;
  left: 50%;
  transform: translate(-50%, 60%);
  background: #d9d9d910;
}

.icon-wrapper {
  width: 70px;
  height: 70px;
  border-radius: 100%;
  background-color: white;
}

.shadow-default {
  box-shadow: 5px 5px black;
}

.shadow-default:hover {
  box-shadow: none;
}
</style>
