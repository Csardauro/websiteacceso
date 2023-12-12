<template>
  <section class="section_contact">
  <Header_contact />
  
      
   

    <v-container fluid>
    <v-row>
      <v-col cols="12" sm="6">
        <div class="text-left mb-4 container-xl" style="padding-left: 15%;">
          <h2 class="text-h3 font-weight-bold mb-0" style="color: #f8f8f8;">Contáctanos</h2>
          <h2 class="text-h3 font-weight-bold mt-0" style="color: #29AAE3;">y cuentanos tu idea</h2>
          <p class="text-h6" style="color: #f8f8f8;">
          Gracias por estar interesado(a) en nuestros servicios, llena el formulario para saber más sobre tu proyectos
          y en brevedad un especialista se pondrá en contacto contigo.
          </p>
          
          <h2 class="text-h5 font-weight-bold mb-0" style="color: #29AAE3;">(999) 222 5447 </h2>
        </div>

        
        
      </v-col>

      <v-col cols="12" sm="6">
        <v-card class="mx-auto" max-width="420">
          <v-card-text class="text-left">
            <v-form>
              <label>Nombre</label>
              <v-text-field type="name" v-model="name" required></v-text-field>
              <label>Correo electrónico</label>
              <v-text-field type="email" v-model="email" required></v-text-field>
              <label>Número</label>
              <v-text-field type="number" v-model="number" required></v-text-field>
              <label>¿En qué estás pensando?</label>
              <v-select
                v-model="interestedIn"
                :items="interestOptions"
                required
              ></v-select>
              <v-btn color="primary" type="submit">Enviar</v-btn>
            </v-form>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>

<piedepagina />
</section>
</template>

<style>
:root {
  --background-image: url('/fondo_contacto.gif');
}

.section_contact {
  background-image: var(--background-image);
  background-size: contain;
  background-repeat: no-repeat;
  background-color: white;
}


.up {
    margin-top: 5%;
    margin-bottom: 5%;
    align-content: center;
}

form {
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;

  
}
label {
    color: #181818;
    display: inline-block;
    margin: 25px 0  15px;
    font-size: 0.6rem;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
}

input {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-color: #29AAE3;
    border-bottom: 1px solid #ddd;
    color: #29AAE3;
}

</style>


<script>
import piedepagina from './Footer.vue'
import Header_contact from './Header_contact.vue'

export default {
    name: 'Contact',
    components:{
        Header_contact,
        piedepagina,
    },

    data() {
    return {
      name: '',
      email: '',
      number: '',
      interestedIn: null,
      interestOptions: [
        'Seguridad electrónica',
        'Comunicación, Voz y Datos',
        'Controles de Acceso',
        'Automatización'
      ]
    };
  },

  methods: {
    submitForm() {
      console.log('Formulario enviado');
      console.log('Nombre:', this.name);
      console.log('Correo:', this.email);
      console.log('Número celular:', this.number);
      console.log('Interesado(a) en:', this.interestedIn);
    }
  }

}
</script>