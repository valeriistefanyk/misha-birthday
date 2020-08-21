<template>
  <v-container grid-list-lg>
    <v-layout row wrap>
      <v-flex xs12 sm6 md4>
        <v-img src="@/assets/withbd.gif"></v-img>
      </v-flex>
      <v-flex xs12 sm6 md4>
        <v-card class="mx-auto" max-width="400" color="rgb(219, 151, 13)" dark>
          <v-img class="pt-4" src="@/assets/hlaponinstar.jpg" height="100%"></v-img>
          <v-card-title>Поздравление от Хлаckstar Games</v-card-title>
          <v-card-subtitle>Ну привет Миша. Я тут подсяду? Спасибо. Зачетку принес? Хочу написать мои пожелания на твой день рождения. Не принес??? Отчислен.</v-card-subtitle>
        </v-card>
      </v-flex>
      <v-flex xs12 sm6 md4>
        <div>
          <v-img src="@/assets/putin.jpg"></v-img>
          <v-card-actions class="mt-4">
            <v-spacer></v-spacer>
            <v-btn color="accent-4" large @click="dialog=true">DON'T CLICK</v-btn>
          </v-card-actions>
        </div>
      </v-flex>
    </v-layout>

    <v-row justify="center">
      <v-dialog v-model="dialog" max-width="800">
        <v-card>
          <v-img src="@/assets/mishaonthebed.jpg"></v-img>
        </v-card>
      </v-dialog>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
    };
  },
};
</script>

<style lang="scss" scoped>
</style>