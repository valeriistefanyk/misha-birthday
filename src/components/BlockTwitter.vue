<template>
  <v-container grid-list-lg>
    <v-alert
      color="indigo"
      dark
      class="text-center"
    >
      Некоторые знакомые из Твиттера и Ютуба (премиум) попросили передать поздравления
    </v-alert>
    <v-layout row wrap>
      <v-flex xs12 sm6 md4 v-for="(person) in people_set1" :key="person.name">
        <v-card
          class="mx-auto"
          elevation="12"
          max-width="500"
          :color="person.color"
          dark
          :style="{background: person.style}"
        >
          <v-card-title>
            <v-icon large left>mdi-twitter</v-icon>
            <span class="title font-weight-light">Twitter</span>
          </v-card-title>
          <v-card-text class="headline font-weight-bold">{{ person.text }}</v-card-text>

          <v-card-actions>
            <v-list-item class="grow">
              <v-list-item-avatar color="grey darken-3">
                <v-img
                  class="elevation-6"
                  :eager="true"
                  :src="require('../assets/' + person.picture)"
                  alt="fdsf"
                ></v-img>
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>{{ person.name }}</v-list-item-title>
              </v-list-item-content>
                <v-icon class="mr-1">mdi-heart</v-icon>
                <span class="subheading mr-2">{{ person.likes }}</span>
            </v-list-item>
          </v-card-actions>
        </v-card>
      </v-flex>

      <v-flex xs12 sm12 md8>
      <v-card color="rgba(40, 40, 40, 0.6)" elevation="12" dark
    max-width="1000"
    class="mx-auto"
  >
    <v-list-item>
      <v-list-item-content>
        <v-list-item-subtitle>Реклама</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
    <v-img
      src="@/assets/malva.jpg"
      height="194"
    ></v-img>
    <v-card-text class="text-subtitle-1 font-weight-bold">
      Садиба "Мальва" відчиняє свої двері для постояльців! До Ваших послуг комфортабельні дво-, три- та чотиримісні номери. Знаходимось за крок від твого спуску.
    </v-card-text>
    <v-card-actions>      
      <v-spacer></v-spacer>
      <v-btn
        text
        color="accent-4"
        @click="dialog=true"
      >
        Дізнатись більше
      </v-btn>
    </v-card-actions>
  </v-card>
  </v-flex>

  <v-flex xs12 sm6 md4 v-for="(person) in people_set2" :key="person.name">
        <v-card
          class="mx-auto"
          elevation="12"
          max-width="500"
          :color="person.color"
          dark
          :style="{background: person.style}"
        >
          <v-card-title>
            <v-icon large left>mdi-twitter</v-icon>
            <span class="title font-weight-light">Twitter</span>
          </v-card-title>
          <v-card-text class="headline font-weight-bold">{{ person.text }}</v-card-text>

          <v-card-actions>
            <v-list-item class="grow">
              <v-list-item-avatar color="grey darken-3">
                <v-img
                  class="elevation-6"
                  :eager="true"
                  :src="require('../assets/' + person.picture)"
                  alt="fdsf"
                ></v-img>
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>{{ person.name }}</v-list-item-title>
              </v-list-item-content>
                <v-icon class="mr-1">mdi-heart</v-icon>
                <span class="subheading mr-2">{{ person.likes }}</span>
            </v-list-item>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>

    <v-row justify="center">
    <v-dialog v-model="dialog" persistent max-width="290">
      <v-card>
        <v-card-title class="my-title text-uppercase font-weight-bold">Сначала лого сделай, Миша</v-card-title>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="green darken-1" text @click="dialog = false">Я понял, хорошо</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>

  </v-container>
</template>

<script>
export default {
  name: "BlockTwitter",
  data() {
    return {
      dialog: false,
      people_set1: [
        {
          name: "Jordan",
          likes: 185,
          color: "rgba(245, 66, 182, 0.8)",
          text:
            "Мало кто знает, но свое лого я срисовал с тебя. С ДР и успехов в логотипах!",
          picture: "jordan.jpg",
        },
        {
          name: "Musk",
          likes: 1488,
          color: "rgba(38, 197, 218, 0.8)",
          text:
            "Misha, I wish you to become the top 1 in your favorite industry. From time to time drink cognac and enjoy life",
          picture: "elonmusk.jpg",
        },
        {
          name: "Ma Lun",
          likes: "5:3",
          color: "rgba(10, 84, 196, 0.8)",
          text: "學會玩",
          picture: "malun.jpg",
        },
        {
          name: "Кучанський",
          likes: "0101",
          color: "rgba(245, 224, 66, 0.6)",
          text:
            "0110110101101001011100110110100001100001011011000110111101101000",
          picture: "kuchanskiy.jpg",
        },
        {
          name: "Вишняков",
          likes: "не понел",
          color: "rgba(90, 90, 90, 0.8)",
          text:
            "ЭЭ э м эмм ээ ну это ээ э с днем эээ рождения эмм прокси сервер эээ",
          picture: "vishnya.jpg",
        },
        
        
        {
          name: "Царук",
          likes: "7",
          color: "rgba(10, 84, 196, 0.8)",
          text: "Слыш Назаренко, раз у хлопца день рождения, поставь ему 5. Я же не лох какой-то",
          picture: "tsaruk.jpg",
        },
        {
          name: "Шумахер",
          likes: "350km/h",
          color: "rgba(38, 197, 218, 0.8)",
          text: "До некоторого момента я всегда считал себя чемпионом. Но увидев твой болид и мастерство вождения, откровенно скажу - ты прирожденный гонщик",
          picture: "schumacher.jpg",
        },
      ],
      people_set2: [
        {
          name: "Даша",
          likes: "",
          color: "rgba(186, 6, 6, 0.7)",
          text: 'Дааа Миша, как же я одгого раза классно с тобой во Львов съездила, ах как вспомню',
          picture: "dasha.jpg",
        },
        {
          name: "Дымхаузен",
          likes: "10",
          color: "rgba(17, 184, 53, 0.7)",
          text: 'С ДР гламурный мазаф*ака😈 И добро пожаловать в наше царство - баронов Дымхаузенов 🤴🏼🙈 Покурил Milano и жизнь стала ярче 🤙🏼😎👱🏻‍♀️',
          picture: "hookahking.jpg",
        },
        {
          name: "Терентьев",
          likes: 0,
          color: "#2611AA",
          text: "Сам пи**рас(((",
          picture: "terentos.jpg",
          style:
            "linear-gradient(0deg, rgba(243,251,36,1) 0%, rgba(49,171,91,1) 17%, rgba(175,18,186,1) 36%, rgba(181,88,48,1) 55%, rgba(195,23,50,1) 76%, rgba(58,56,222,1) 100%)",
        },
      ]
    };
  },
};
</script>

<style scoped>
  .my-title {
    font-family: 'Pacifico', cursive;
  }
</style>