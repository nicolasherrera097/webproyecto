<template>
  <v-container>
    <br><br><br>
    
    <v-layout wrap>
      <v-flex class="mt-5" xs12>
        <h1 style="color:#2c64ac">COTIZACIÓN</h1>
        <hr class="black">
        <h2 class="ml-5 mr-5 mb-5 mt-5" align="justify">¡Calcula el presupuesto de tus proyectos con nuestro simulador!</h2>
      </v-flex>

      <v-flex class="mt-5" xs6>
        <h2 style="color:#2c64ac">Trabajos seleccionados</h2>
        <hr class="black mr-6"><br>

        <v-data-table
          :headers="headers"
          :items="trabajos"
          :items-per-page="5"
          class="elevation-1 ml-6 mr-6"
        ></v-data-table><br><br>
        

        <v-row class="black--text">
          <v-col class="ml-12">
            <h4>Total</h4>
          </v-col>
          <v-col class="mr-12">
            <v-text-field
            label="$1.300.000"
            placeholder="Placeholder"
            solo
          ></v-text-field>           
          </v-col>
        </v-row>
        <v-row class="black--text">
          <v-col class="ml-12">
            <h4>Días aproximados de trabajo</h4>
          </v-col>
          <v-col class="mr-12">
            <v-text-field
            label="5"
            placeholder="Placeholder"
            solo
          ></v-text-field>           
          </v-col>
        </v-row>

      </v-flex>
      <v-flex class="mt-5" xs6>
        <h2 style="color:#2c64ac">Seleccione trabajo</h2>
        <hr class="black">
        <v-checkbox
            v-model="ex4"
            label="Pintura"
            color="primary"
            value="primary"
            hide-details
            class="black--text"
        ></v-checkbox>
        <v-checkbox
            v-model="ex4"
            label="Radier"
            color="primary"
            value="primary"
            hide-details
            class="black--text"
        ></v-checkbox>
        <v-checkbox
            v-model="ex4"
            label="Cerámica"
            color="primary"
            value="primary"
            hide-details
            class="black--text"
        ></v-checkbox>
        <v-checkbox
            v-model="ex4"
            label="Piso Flotante"
            color="primary"
            value="primary"
            hide-details
            class="black--text"
        ></v-checkbox>
        <v-checkbox
            v-model="ex4"
            label="Paneles térmicos"
            color="primary"
            value="primary"
            hide-details
            class="black--text"
        ></v-checkbox>
        <br>
        <hr class="black"><br>

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
            <h4>Subtotal</h4>
          </v-col>
          <v-col class="mr-12">
            <v-text-field
            label="$250.000"
            placeholder="Placeholder"
            solo
          ></v-text-field>           
          </v-col>
        </v-row>

        <div align="center">
          <v-btn rounded color="primary" dark>Agregar a cotización</v-btn>
        </div><br>

        <div align="center">
          <v-img src="https://i.imgur.com/U51aOSC.png" max-height="200" max-width="200"></v-img>
        </div><br>
      </v-flex>

      <v-flex class="mt-5" xs12>
        <hr class="black">
        <v-row class="orange--text justify-content align-center">
          <v-col class="ml-12">
            <h4>E-Mail:</h4>
          </v-col>
          <v-col class="mr-12">
            <v-text-field :rules="rules" placeholder="n.herrera04@ufromail.cl"></v-text-field>
            <v-row>
              <h4 class="blue--text pa-2">
                Asegurate de tener acceso a este email.
              </h4>
            </v-row>
          </v-col>
        </v-row>
        
      </v-flex>
    </v-layout>
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
    headers: [
          {
            text: 'N°',
            align: 'start',
            sortable: false,
            value: 'name',
          },
          { text: 'Trabajo', value: 'trabajo' },
          { text: 'M2', value: 'm2' }
    ],
    trabajos: [
      {
        name: '1',
        trabajo: 'Pintura',
        m2: 70,
      },
      {
        name: '2',
        trabajo: 'Cerámica',
        m2: 100
      }
    ]
  }),
};
</script>