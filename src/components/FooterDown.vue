<template>
  <footer>
    <div>
      © 2021 SOMATTEC
      <div id="my-profile" style="position:absolute;visibility:hidden;">
        <h3>
          Desarrollador
        </h3>

        <ul alt="desarrollador de la pagina">
          <li>
            <a href="https://wa.me/51970155664" target="_black">
              <v-icon v-text="whatsapp" size="20px" color="#000000"> </v-icon>
              Whatsapp</a
            >
          </li>

          <li>
            <a href="mailto:alejandrorgp18@gmail.com"
              ><v-icon v-text="email" size="20px" color="#000000"> </v-icon>
              Enviar email</a
            >
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
//import photo from "@/assets/photo.jpg";
export default {
  name: "FooterDown",
  data() {
    return {
      info: "fab fa-dev",
      whatsapp: "fab fa-whatsapp",
      email: "fa fa-envelope",
      portafolios: "fas fa-briefcase",
      toggle_info: false
      //photo: "background-image: url(" + photo + ");"
    };
  },
  methods: {
    showHidden(ver) {
      let info = document.getElementById("my-profile");
      let about = document.querySelector(".about");
      console.log(about);
      this.toggle_info = !this.toggle_info;
      let res = this.toggle_info == false ? "hidden" : "visible";
      let line = this.toggle_info == false ? "none" : "underline";
      if (ver == true) {
        this.toggle_info = "visible";
      }
      about.style.textDecoration = line;
      info.style.visibility = res;
    }
  }
};
</script>

<style lang="scss">
@import "_basic.scss";

footer {
  margin-top: 40px;
  padding: 2%;
  background: rgb(226, 226, 226);
  color: gray;
  font-family: Roboto;
  text-align: center;
  > div {
    position: relative;
  }
  #my-profile {
    @include flex(space-around, wrap, center);
    box-shadow: 3px 3px 30px -16px rgba(0, 0, 0, 0.75);
    padding: 35px 3px 25px 3px;
    background: rgb(226, 226, 226);
    color: black;
    top: -110px;
    left: 100px;
    position: relative;
    padding: 10px;
    padding-top: 30px;
    height: 90px;
    width: 150px;

    .iconos {
      padding: 10px 5px 5px 5px;
      width: 100%;
      display: inline-flex;
      justify-content: space-around;
    }
    .profile-container {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      strong {
        margin-top: 10px;
        width: 100%;
        font-size: 12px;
      }
    }
    h3 {
      width: 100%;
      background: #d8d8d8;
      @include flex(center);
      position: absolute;
      top: 0;
      padding: 5px;
      font-size: 11px;
      font-family: Poppins;
      color: rgb(37, 37, 37);
    }
    .photo {
      margin-top: 10px;
      height: 45px;
      width: 45px;
      border-radius: 50%;
      background-size: contain;
      box-shadow: 3px 3px 90px -16px rgba(0, 0, 0, 0.75);
    }
    ul {
      strong {
        width: 100%;
      }
      li {
        font-size: 12px;
        padding-top: 3px;
        text-align: left;
      }
      a:hover {
        color: #3184d3;
      }
      list-style: none;
    }
  }
  @include flex(center);
  a {
    text-decoration: none;
    color: black;
  }
}
</style>
