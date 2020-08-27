<template>
  <v-container grid-list-lg>
      <v-layout row wrap>
          <v-flex xs12 sm6 md8>
    <v-carousel cycle height="400" hide-delimiter-background show-arrows-on-hover>
      <v-carousel-item v-for="(slide, i) in slides" :key="i" :src="require('../assets/' + img[i])">
        <v-sheet height="100%" color="rgba(100, 100, 100, 0.1)">
          <v-row class="fill-height" align="center" justify="center">
            <div class="display-1">{{ slide }}</div>
          </v-row>
          
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
          </v-flex>


          <v-flex xs12 sm6 md4>
        
      <v-hover v-slot:default="{ hover }">
        <v-card
          :elevation="hover ? 12 : 2"
          class="mx-auto"
          width="400px"
        >
          <v-img 
          :src="hover ? require('@/assets/misha2.jpg') : require('@/assets/misha1.jpg')" width="400px" height="400px" aspect-ratio="1.7"></v-img>
        </v-card>
      </v-hover>
          </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
    export default {
        data() {
            return {
                colors: [
          'indigo',
          'warning',
          'pink darken-2',
          'red lighten-1',
          'deep-purple accent-4',
        ],
        slides: [
          'Миша отдыхает',
          'Миша пьет пывце',
          'Миша сдал ЗНО',
          'Миша с Олегом',
          'Миша спит в бане'
        ],
        img: [
          '1.jpg',
          '2.jpg',
          '4.jpg',
          '3.jpg',
          '5.jpg',
        ],
        }
    }}
</script>
