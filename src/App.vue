<template>
  <div id="app">
    <MenuBar />
    <sectionHome />
    <quienesSomos />
    <queHacemos />
    <sectionPlanes />
    <nuestrosClientes />
    <sectionContacto />
    <FooterDown />
    <FloatButtons />
  </div>
</template>

<script>
import MenuBar from "./components/MenuBar.vue";
import sectionHome from "./components/sectionHome.vue";
import sectionContacto from "./components/sectionContacto.vue";
import quienesSomos from "./components/quienesSomos.vue";
import sectionPlanes from "./components/sectionPlanes.vue";
import queHacemos from "./components/queHacemos.vue";
import FooterDown from "./components/FooterDown.vue";
import FloatButtons from "./components/FloatButtons.vue";

export default {
  name: "App",

  components: {
    MenuBar,
    sectionHome,
    sectionContacto,
    quienesSomos,
    sectionPlanes,
    FooterDown,
    queHacemos,
    FloatButtons
  }
};
</script>
<style lang="scss">
@import "_basic.scss";
@include newFont("Poppins", "Poppins-Regular.ttf");
@include newFont("PoppinsB", "Poppins-SemiBold.ttf");
@include newFont("RobotoB", "RobotoCondensed-Bold.ttf");
@include newFont("Roboto", "RobotoCondensed-Regular.ttf");
* {
  padding: 0;
  margin: 0;
}
#app {
  overflow: hidden;
  min-width: 280px;
}
p {
  text-align: justify;
  font-family: Poppins;
  font-size: 17px;
  max-width: 1280px;
}
body {
  background: #ecf0f1;
  overflow-x: hidden;
  min-width: 280px;
}
*::selection {
  background: #3d64ad;
  color: white;
}
section {
  font-family: Roboto;
  width: 100%;
  background-color: #ecf0f1;
  margin-top: 50px;
  min-width: 280px;
}
h1 {
  width: 100%;
  height: 30px;
  padding: 15px 5px;
  text-align: center;
  font-size: 35px;
  @include phones() {
    font-size: 30px;
  }
}
</style>
