<template>
  <v-app class="sms">
    <span class="bg"></span>
    <v-navigation-drawer 
      app 
      temporary 
      v-model="drawer"
      class="nav-color">
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="my-title">
            WHAT I CAN
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>
      <v-divider></v-divider>
      <v-list dense nav>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          class="color-picker"
        >
          <v-list-item-content :style="{color: item.color}">
            <v-list-item-title class="text-decoration-underline text-uppercase my-title">{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app src="@/assets/nav.jpg" dark>
      <v-app-bar-nav-icon @click="drawer =! drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="title-font">
        VM Core Production
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-title class="title-font" style="color: pink">
        Misha's birthday
      </v-toolbar-title>
    </v-app-bar>

    <v-main>
      <marquee bgcolor="red" class="marquee">Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача, Миша миша, ача ача,Миша миша, ача ача, Миша миша, ача ача, </marquee>
      <v-container fluid>
        <!-- Component start -->
        <app-content></app-content>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Content from '@/components/Content'

export default {
  name: 'App',
  components: {
    AppContent: Content,
  },
  data: () => ({
    drawer: false,
    items: [
      { title: 'Верстка', icon: '', color: 'red' },
      { title: 'photoshop скачать', icon: '', color: 'blue' },
      { title: 'draftsman of dicks', icon: '', color: 'yellow' },
      { title: 'the bestes SEO', icon: '', color: 'green' },
      { title: 'KIZARU TEAM', icon: '', color: 'black' },
      { title: 'Senior Seo Лысой горы', icon: '', color: 'white' },
    ]
  }),
};
</script>

<style scoped>
  .my-title {
    font-family: 'Pacifico', cursive;
  }

  .bg {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background: linear-gradient(180deg, #A4DF89 -2.53%, #3DD3DD 18.08%, #650F38 33.93%, #C1854E 49.79%, #920000 61.94%, #A6970F 73.04%, #243CBA 83.61%, #08155A 98.93%);
    transform: scale(1.1);
  }
  .nav-color {
    background: linear-gradient(180deg, #501BBF 0%, #77142C 25.52%, #5DC62C 50.52%, #B43FA8 70.83%, #159AAC 100%);
    border: 5px dashed #FFFFFF;
    box-sizing: border-box;
  }
  .color-picker:hover {
    background-color: rgba(36, 118, 201, 0.5);
    color: white;
    font-weight: 900;
    cursor:  url(./assets/cursor3.png), pointer;
  }
  .sms {
    cursor:  url(./assets/cursor3.png), pointer;
  }

  .marquee {
    color: white;
    font-weight: 900;
    letter-spacing: 2px;
  }

  .title-font {
    font-family: 'Ruge Boogie', cursive;
    font-size: 2.5rem;
    font-weight: 900;
    letter-spacing: 3px;
  }
</style>
