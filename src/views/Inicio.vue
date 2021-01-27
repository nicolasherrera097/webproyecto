<template>
  <v-container>
    <br><br><br>
    <v-layout wrap>
      <v-flex class="mt-3" xs12>
        <div align="center">
          <v-img src="https://i.imgur.com/DLOYbuD.png"></v-img>
        </div>       
      </v-flex>

      <v-flex class="mt-5" xs12>
        <h1 style="color:#2c64ac" align="center">¿QUIÉNES SOMOS?</h1>
        <hr class="black ml-5 mr-5">
        <h2 class="ml-5 mr-5 mb-5 mt-5" align="justify">Somos una Empresa Constructora Familiar, que tenemos como objetivo mejorar las viviendas de todos nuestros usuarios; apostando no solo por beneficios a corto plazo, como es la calefacción de un hogar, sino también, hacer mejoras que vayan en pos de nuestro medio ambiente y nuestra salud física futura. Por lo cual, todas nuestras mejoras, están enfocadas en la postulación al Programa de Descontaminación Ambiental (PDA).</h2>
        <div align="center">
          <v-img src="https://i.imgur.com/U51aOSC.png" max-height="300" max-width="300"></v-img>
        </div>
      </v-flex>

      <v-flex class="mt-5 orange" xs6>
        <h1 style="color:#2c64ac" align="center">MISIÓN</h1>
        <hr class="black ml-5 mr-5">
        <h2 class="ml-5 mr-5 mb-5 mt-5" align="justify">Mejorar estructurales las viviendas de nuestros usuarios por medio de la termoaislación y la reducción de calefactores altamente contaminantes en  las localidades de Temuco, Labranza y Padre las Casas.</h2>
      </v-flex>
      <v-flex class="mt-5 indigo" xs6>
        <h1 style="color:#ec7c1c" align="center">VISIÓN</h1>
        <hr class="black ml-5 mr-5">
        <h2 class="ml-5 mr-5 mb-5 mt-5" align="justify">Mejorar la calidad de vida de nuestros usuarios, por medio de mejoras estructurales en su vivienda enfocadas en la termoaislación y reducción de la huella de carbono de las localidades de Temuco, Labranza y Padre las Casas.</h2>
      </v-flex>

      <v-flex class="mt-5" xs6>
        <v-img src="https://i.imgur.com/Q9hVN1A.png"></v-img>
      </v-flex>
      <v-flex class="mt-5" xs6>
        <h1 style="color:#2c64ac" align="center">¿CÓMO POSTULAR?</h1>
        <hr class="black ml-5 mr-5">
        <h2 class="ml-5 mr-5 mb-5 mt-5" align="justify" style="color:#2c64ac">Para postular debe cumplir los siguientes requisitos:</h2>
        <li class="ml-5 mr-5">Registro social de hogares menor al 70% (Excepto para los adultos mayores)</li>
        <li class="ml-5 mr-5">Contar con un permiso de edificación anterior al año 2007</li>
        <li class="ml-5 mr-5">La superficie de la vivienda debe ser menos a 90 mts2</li>
        <li class="ml-5 mr-5">Contar con la escritura de la vivienda</li>
        <li class="ml-5 mr-5">Contar con carnet vigente</li>
        <li class="ml-5 mr-5">Poseer una cuenta de ahorro para la vivienda del banco estado</li>
        <br>
        <div align="center">
          <v-btn rounded color="primary" dark href="http://localhost:8080/#/postulacion">Postulación</v-btn>
        </div>
      </v-flex>

      <v-flex class="mt-5" xs6>
        <h1 style="color:#2c64ac" align="center">¿CÓMO COTIZAR?</h1>
        <hr class="black ml-5 mr-5">
        <h2 class="ml-5 mr-5 mb-5 mt-5" align="justify">Nuestro sitio web cuenta con un simulador de cotización, en donde podrás calcular un presupuesto estimado de tus proyectos.</h2>
        <div align="center">
          <v-btn rounded color="primary" dark href="http://localhost:8080/#/cotizacion">Cotización</v-btn>
        </div>
      </v-flex>
      <v-flex class="mt-5" xs6>
        <v-img src="https://i.imgur.com/8TvQpV9.jpg"></v-img>
      </v-flex>

      <v-flex class="mt-5 " xs6>
        <h1 style="color:#ec7c1c" align="center">SOBRE NOSOTROS</h1>
        <hr class="black mr-5 ml-5">
        <h2 class="ml-5 mr-5 mb-5 mt-5" align="justify">En esta sección podrás visualizar antecedentes generales de nuestra empresa, además de nuestros principales servicios y proyectos.</h2>
        <div align="center">
          <v-btn rounded color="primary" dark href="http://localhost:8080/#/about">Sobre nosotros</v-btn>
        </div>
      </v-flex>
      <v-flex class="mt-5 " xs6>
        <h1 style="color:#2c64ac" align="center">CONTÁCTANOS</h1>
        <hr class="black ml-5 mr-5">
        <h2 class="ml-5 mr-5 mb-5 mt-5" align="justify">Utilice el siguiente formulario de contacto en caso de tener alguna pregunta o solicitud general sobre nuestros servicios. Haremos todo lo posible para responder en un plazo máximo de 24 horas.</h2>
        <div align="center">
          <v-btn rounded color="primary" dark href="http://localhost:8080/#/contacto">Contáctanos</v-btn>
        </div>
        
        
      </v-flex>

      <v-flex class="mt-5 orange" xs4>
        <h1 style="color:#2c64ac" align="center">SOBRE CONSTRUBAE</h1>
        <hr class="black ml-5 mr-5">
        <h2 class="ml-5 mr-5 mb-5 mt-5" align="justify">En esta página podrá encontrar toda la información necesaria para que pueda postular junto a nosotros al mejoramiento de tu vivienda con el Programa de Descontaminación Ambiental (PDA).</h2>
      </v-flex>
      <v-flex class="mt-5 orange" xs4>
        <h1 style="color:#2c64ac" align="center">ENCUÉNTRANOS</h1>
        <hr class="black ml-5 mr-5">
        <h4 class="ml-5 mr-5 mb-5 mt-5" align="center">José Reyes Morales #2090, Temuco</h4>
        <div align="center">
          <v-img src="https://i.imgur.com/WhYtRlH.png"></v-img>
          <br>
        </div>
      </v-flex>
      <v-flex class="mt-5 orange" xs4>
        <h1 style="color:#2c64ac" align="center">ENLACES DE INTERÉS</h1>
        <hr class="black ml-5 mr-5">
        <h2 class="ml-5 mr-5 mb-5 mt-5" align="justify"></h2>
        <div align="center">
          <v-btn rounded color="primary" dark href="http://localhost:8080/#/about">Sobre nosotros</v-btn>
          <br><br>
          <v-btn rounded color="primary" dark href="http://localhost:8080/#/postulacion">Postulación</v-btn>
          <br><br>
          <v-btn rounded color="primary" dark href="http://localhost:8080/#/cotizacion">Cotización</v-btn>
          <br><br>
          <v-btn rounded color="primary" dark href="http://localhost:8080/#/contacto">Contáctanos</v-btn>
        </div>
      </v-flex>


    </v-layout>
  </v-container>
</template>