<template>
  <v-layout>
    <v-flex xs12 sm6 offset-sm3>
      <v-card>
        <v-container grid-list-sm fluid>
          <v-layout row wrap>
            <v-flex v-for="n in 9" :key="n" xs4 d-flex>
              <v-card flat tile class="d-flex">
                <v-img :src="randomPicture(500,300)"
                  aspect-ratio="1"
                  class="grey lighten-2">
                  <v-layout
                    slot="placeholder"
                    fill-height
                    align-center
                    justify-center
                    ma-0>
                    <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                  </v-layout>
                </v-img>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  name: 'ImageCollage',
  methods: {
    randomPicture (x = 100, y = 100) {
      return `https://placeimg.com/${x}/${y}/any?t=${(Date.now())}&r=${Math.floor(Math.random() * Math.floor(100000000))}`
    }
  }
}
</script>

<style scoped>

</style>
