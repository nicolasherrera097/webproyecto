<template>
  <v-container>
    <br><br><br>

    <v-layout wrap>
      <v-flex class="mt-5" xs12>
        <h1 style="color:#2c64ac">ALGUNOS DE NUESTROS PROYECTOS</h1>
        <hr class="black">
        <br>
      </v-flex>
    </v-layout>

    <v-row>
      <v-col
        v-for="n in 9"
        :key="n"
        class="d-flex child-flex"
        cols="4"
      >
        <v-img
          :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
          :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
          aspect-ratio="1"
          class="grey lighten-2"
        >
          <template v-slot:placeholder>
            <v-row
              class="fill-height ma-0"
              align="center"
              justify="center"
            >
              <v-progress-circular
                indeterminate
                color="grey lighten-5"
              ></v-progress-circular>
            </v-row>
          </template>
        </v-img>
      </v-col>
  </v-row>
  </v-container>
</template>
