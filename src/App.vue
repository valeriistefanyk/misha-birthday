<template>
  <v-app class="sms">
    <span class="bg"></span>
    <v-navigation-drawer app temporary v-model="drawer" class="nav-color">
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="my-title">Що може Міша</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
      <v-divider></v-divider>
      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link class="color-picker">
          <v-list-item-content :style="{color: item.color}">
            <v-list-item-title
              class="text-decoration-underline text-uppercase my-title"
            >{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app src="@/assets/nav.jpg" dark>
      <v-app-bar-nav-icon @click="drawer =! drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="title-font hidden-sm-and-down">VM Core Production</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-title class="title-font" style="color: pink">Misha's birthday</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <marquee
        bgcolor="red"
        class="marquee"
      >Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача,Миша миша, ача ача, Миша миша, ача ача,
      Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача,Миша миша, ача ача, Миша миша, ача ача,
      Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача,Миша миша, ача ача, Миша миша, ача ача,
      Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача,Миша миша, ача ача, Миша миша, ача ача,
      Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача,Миша миша, ача ача, Миша миша, ача ача,
      Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача,Миша миша, ача ача, Миша миша, ача ача</marquee>
      <v-container fluid>
        <!-- Component start -->
        <app-content></app-content>
      </v-container>
    </v-main>

    <v-footer dark padless class="mt-10 font-italic">
      <v-card flat tile class="indigo lighten-1 white--text text-center">
        <v-card-text
          class="white--text"
        >Веб-сайт был создан в развлекательных целях, разработчиком креативной компании VM Core Production Валерием с целью поздравить коллегу, талантливого SEO-специалиста, копирайтера, логотипщика, дизайнера, Project-менеджера, программиста, PR-менеджера, верстальщика, участника группировки VM Core Production Band - Михаила. Все права защищены </v-card-text>
        <v-divider></v-divider>
        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} —
          <strong>VM CORE PRODUCTION</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
import Content from "@/components/Content";

export default {
  name: "App",
  components: {
    AppContent: Content,
  },
  data: () => ({
    drawer: false,
    items: [
      { title: "Верстать", icon: "", color: "red" },
      { title: "Качать photoshop", icon: "", color: "blue" },
      { title: "Рисовать в фигме", icon: "", color: "yellow" },
      { title: "the bestes SEO", icon: "", color: "green" },
      { title: "Играть в теннис", icon: "", color: "black" },
      { title: "ПРограммировать", icon: "", color: "#333" },
      { title: "Покер", icon: "", color: "rgb(52, 235, 55)" },
      { title: "Project manager", icon: "", color: "rgb(36, 31, 181)" },
      { title: "Играть в футбол", icon: "", color: "rgb(147, 30, 214)" },
      { title: "Ставки на спорт", icon: "", color: "rgb(194, 14, 167)" },
      { title: "Баскетбол", icon: "", color: "rgb(219, 200, 22)" },
      { title: "Senior Seo Лысой горы", icon: "", color: "rgb(230, 90, 34)" },
      { title: "Ломать заборы", icon: "", color: "rgb(196, 8, 64)" },
      { title: "Отлично водить", icon: "", color: "rgb(74, 133, 158)" },
      { title: "Лучшие логотипы", icon: "", color: "rgb(122, 168, 37)" },
      { title: "И многое другое...", icon: "", color: "white" },
    ],
  }),
};
</script>

<style scoped>
.my-title {
  font-family: "Pacifico", cursive;
}

.bg {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  background: linear-gradient(
    180deg,
    #a4df89 -2.53%,
    #3dd3dd 18.08%,
    #650f38 33.93%,
    #c1854e 49.79%,
    #920000 61.94%,
    #a6970f 73.04%,
    #243cba 83.61%,
    #08155a 98.93%
  );
}
.nav-color {
  background: linear-gradient(
    180deg,
    #501bbf 0%,
    #77142c 25.52%,
    #5dc62c 50.52%,
    #b43fa8 70.83%,
    #159aac 100%
  );
  border: 5px dashed #ffffff;
  box-sizing: border-box;
}
.color-picker:hover {
  background-color: rgba(36, 118, 201, 0.5);
  color: white;
  font-weight: 900;
  cursor: url(./assets/cursor3.png), pointer;
}
.sms {
  cursor: url(./assets/cursor3.png), pointer;
}

.marquee {
  color: white;
  font-weight: 900;
  letter-spacing: 2px;
}

.title-font {
  font-family: "Ruge Boogie", cursive;
  font-size: 2.5rem;
  font-weight: 900;
  letter-spacing: 3px;
}
</style>
