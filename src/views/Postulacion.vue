<template>
  <v-container>
    <br><br><br>

    <v-layout wrap>
      <v-flex class="mt-5" xs12>
        <h1 style="color:#2c64ac">POSTULACIÓN</h1>
        <hr class="black">
        <h2 class="ml-5 mr-5 mb-5 mt-5" align="justify">Para postular debe cumplir con ciertos requisitos, los cuales tendrá que
        detallar en el siguiente formulario.</h2>
      </v-flex>
    </v-layout>

    <v-row class="pa-15 justify-center">
      <v-card elevation="10" shaped class="blue--text" width="900">
        <v-card-title class="ml-8">Ingrese sus datos personales:</v-card-title>
        <v-row class="orange--text align-center flex-start">
          <v-col class="ml-12">
            <h4>Nombres:</h4>
          </v-col>
          <v-col class="mr-12">
            <v-text-field :rules="rules"></v-text-field>
          </v-col>
        </v-row>
        <v-row class="orange--text justify-content align-center">
          <v-col class="ml-12">
            <h4>Apellidos:</h4>
          </v-col>
          <v-col class="mr-12">
            <v-text-field :rules="rules"></v-text-field>
          </v-col>
        </v-row>
        <v-row class="orange--text justify-content align-center">
          <v-col class="ml-12">
            <h4>Edad:</h4>
          </v-col>
          <v-col>
            <v-select
              :items="numbers"
              menu-props="auto"
              hide-details
              label="Edad"
              single-line
            ></v-select>
          </v-col>
          <v-col >
            <h4>Telefono:</h4>
          </v-col>
          <v-col class="mr-12">
            <v-text-field :rules="telefono"></v-text-field>
          </v-col>
        </v-row>
        <v-row class="orange--text justify-content align-center">
          <v-col class="ml-12">
            <h4>E-Mail:</h4>
          </v-col>
          <v-col class="mr-12">
            <v-text-field :rules="rules"></v-text-field>
            <v-row>
              <h4 class="blue--text pa-2">
                Asegurate de tener acceso a este email.
              </h4>
            </v-row>
          </v-col>
        </v-row>
        <v-row class="orange--text justify-content align-center">
          <v-col class="ml-12">
            <h4>Rut:</h4>
          </v-col>
          <v-col class="mr-12">
            <v-text-field :rules="rules"></v-text-field>
          </v-col>
        </v-row>
        <v-row class="orange--text justify-content align-center">
          <v-col>
            <h4 class="ml-12">Direccion:</h4>
          </v-col>
          <v-col class="mr-12">
            <v-text-field :rules="rules"></v-text-field>
          </v-col>
        </v-row>
        <v-row class="ml-8 mr-8 pt-8">
          <v-divider class="ml-8 mr-8 pt-8" horizontal></v-divider>
        </v-row>

        <v-card-title class="ml-8">Ingrese datos de la vivienda:</v-card-title>
        <v-row class="ml-8 mr-8 pt-8">
          <v-divider class="ml-8 mr-8 pt-8" horizontal></v-divider>
        </v-row>
        <v-row class="black--text">
          <v-col class="ml-12">
            <h4>Superficie de la vivienda</h4>
          </v-col>
          <v-col class="mr-12">
            <v-slider
              v-model="value"
              :rules="metros"
              label="m2"
              step="1"
              thumb-label="always"
              ticks
              min="30"
              max="140"
            ></v-slider>
          </v-col>
        </v-row>
        <v-row class="black--text">
          <v-col class="ml-12">
            <h4>Año permiso edificación de la vivienda</h4>
          </v-col>
          <v-col class="mr-12">
            <v-slider
              v-model="value"
              :rules="edificacion"
              label="m2"
              step="1"
              thumb-label="always"
              ticks
              min="1900"
              max="2021"
            ></v-slider>
          </v-col>
        </v-row>
        <v-row class="ml-12">
          <v-checkbox
            v-model="ex4"
            label="¿Cuenta con la escritura de la vivienda?"
            color="primary"
            value="primary"
            hide-details
            class="black--text"
          ></v-checkbox>
        </v-row>
        <v-row class="ml-12">
          <v-checkbox
            v-model="ex4"
            label="¿Su carnet de identidad esta vigente?"
            color="primary"
            value="primary"
            hide-details
            class="black--text"
          ></v-checkbox>
        </v-row>
        <v-row class="ml-12">
          <v-checkbox
            v-model="ex4"
            label="¿posee cuenta de ahorro para la vivienda?"
            color="primary"
            value="primary"
            hide-details
            class="black--text"
          ></v-checkbox>
        </v-row>
        <v-row class="ml-12">
          <v-checkbox
            v-model="ex4"
            label="¿Fue beneficiario de algun subsidio de aislación?"
            color="primary"
            value="primary"
            hide-details
            class="black--text"
          ></v-checkbox>
        </v-row>
        <v-row class="ml-12">
          <v-checkbox
            v-model="ex4"
            label="¿Posee registro social de hogares?"
            color="primary"
            value="primary"
            hide-details
            class="black--text"
          ></v-checkbox>
        </v-row>
        <v-row class="ml-8 mr-8 pt-8">
          <v-divider class="mx-4" horizontal></v-divider>
        </v-row>
        <v-row class="ml-12">
          <v-checkbox
            v-model="ex4"
            label="¿Acepto los terminos y condiciones?"
            color="primary"
            value="primary"
            hide-details
            class="black--text"
          ></v-checkbox>
        </v-row>
        <v-row class="justify-center pt-8 pb-8">
          <v-card-actions>
            <v-btn color="blue" text @click="EnviarFormulario">
              Enviar Formulario
            </v-btn>
          </v-card-actions>
        </v-row>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    rules: [
      (value) => !!value || "Requerido.",
      (value) => (value || "").length <= 30 || "Max 30 caracteres",
    ],
    metros: [(v) => v <= 90 || "No debe superar los 90m2"],
    edificacion: [(v) => v <= 2007 || "No debe ser superior al 2007"],
    numbers: [
      "1",
      "2",
      "3",
      "4",
      "5",
      "6",
      "7",
      "8",
      "9",
      "10",
      "11",
      "12",
      "13",
      "14",
      "15",
      "16",
      "17",
      "18",
      "19",
      "20",
      "21",
      "22",
      "23",
      "24",
      "25",
      "26",
      "27",
      "28",
      "29",
      "30",
      "31",
      "32",
    ],
    telefono: [
      (value) => !!value || "Requerido",
      (value) => (value || "").length <= 9 || "Max 9 caracteres",
    ],
  }),
};
</script>