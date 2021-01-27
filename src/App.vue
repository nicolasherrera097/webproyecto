<template>
  <v-app>
    <v-app-bar app color="light-blue accent-2" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://i.imgur.com/U51aOSC.png"
          transition="scale-transition"
          width="60"
        />
      </div>

      <v-spacer/>

      <v-btn to="/inicio" text>Inicio</v-btn>
      <v-btn to="/about" text>Sobre nosotros</v-btn>
      <v-btn to="/postulacion" text>Postulación</v-btn>
      <v-btn to="/cotizacion" text>Cotización</v-btn>
      <v-btn to="/contacto" text>Contacto</v-btn>
    </v-app-bar>
      
    <router-view/>

    <v-footer color="indigo" padless>
      <v-row justify="center" no-gutters>
        <v-btn
          v-for="link in links"
          :key="link"
          color="white"
          text
          rounded
          class="my-2"
        >
          {{ link }}
        </v-btn>
        <v-col
          class="indigo py-4 text-center white--text"
          cols="12"
        >
          {{ new Date().getFullYear() }} — <strong>ConstruBae. Todos los derechos reservados. Política de privacidad – Términos y condiciones</strong>
        </v-col>
      </v-row>
    </v-footer>
    
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      icons: [
        'mdi-home',
        'mdi-email',
        'mdi-calendar',
        'mdi-delete',
      ],
      items: [
        'default',
        'absolute',
        'fixed',
      ],
      padless: false,
      variant: 'default',
    }),
    computed: {
      localAttrs () {
        const attrs = {}
        if (this.variant === 'default') {
          attrs.absolute = false
          attrs.fixed = false
        } else {
          attrs[this.variant] = true
        }
        return attrs
      },
    },
  }
</script>
