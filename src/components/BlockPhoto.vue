<template>
  <v-container grid-list-lg>
      <v-layout row wrap>
          <v-flex xs12 sm6 md8>
    <v-carousel cycle height="400" hide-delimiter-background show-arrows-on-hover>
      <v-carousel-item v-for="(slide, i) in slides" :key="i">
        <v-sheet :color="colors[i]" height="100%">
          <v-row class="fill-height" align="center" justify="center">
            <div class="display-3">{{ slide }} Slide</div>
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
          'First',
          'Second',
          'Third',
          'Fourth',
          'Fift'
        ]
        }
    }}
</script>
