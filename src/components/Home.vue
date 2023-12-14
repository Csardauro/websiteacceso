<template>
   
        <Header />


        <div class="container-xxl">
    <div class="container-lg py-5">
        <swiper :slides-per-view="1" :space-between="30" :autoplay="{ delay: 10000, disableOnInteraction:false }" :pagination="{ clickable: true }" :modules="modules" class="mySwiper">
  <swiper-slide v-for="(slide, index) in slides" :key="index">
          <div class="container-fluid py-5">
            <div class="row">
              <div class="col-md-6">
                <div class="text-h2 font-weight-regular up text-left" :style="{ color: slide.titleColor }">
                  {{ slide.title }}
                </div>
                <div class="text-h6 up text-left">
                  {{ slide.description }}
                </div>
                <Palabras />
                <br>
                <br>
                <div class="d-flex justify-content-start">
                  <v-btn elevation="8" rounded="xl" size="large"
                    :class="[slide.buttonColor, 'text-white']">
                    {{ slide.buttonText }}
                  </v-btn>
                </div>
              </div>
              <div class="col-md-4">
                <img :src="slide.image" alt="Imagen" style="width: 90%; height: auto;">
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>

        <div class="container-xxl">
        <img src="../../public/portadaloop.gif" alt="Portada loop home">
    </div>
        <br>
        <div class="container">
            <div class="text-no-wrap text-h2 text-center font-weight-regular up" style="text-align: center; color:#033f58">
                La seguridad que tu empresa necesita</div>
            <div class="text-h6 up" style="text-align: center;">Creamos sistemas que te brindan seguridad de primer nivel en
                tu negocio,
                <br>logrando que evites delitos en tu zona de trabajo.
            </div>


        <div class="container-lg py-5">
            <swiper :slidesPerView="3" :spaceBetween="30" :pagination="{ clickable: true, }" :modules="modules"
                class="mySwiper" :autoplay="true">

                <swiper-slide><img class="img-1" src="/Camaras.jpg" /> </swiper-slide>
                <swiper-slide><img class="img-1" src="/Casetas.jpg" /></swiper-slide>
                <swiper-slide><img class="img-1" src="/Porton.jpg" /></swiper-slide>
            </swiper>
            <br>
        </div>
        </div>

        <div class="up">
            <v-parallax height="350" src="CTA_inicio.png">
                <div class="d-flex align-center text-white  fill-height container">
                    <div>
                        <div class="text-h3 font-weight-thin mb-4">
                            ¿Buscas prevenir <br>delitos en tu negocio?
                        </div>
                        <h4 class="text-body-1">
                            Dale clic al botón y cotiza hoy mismo
                        </h4>
                        <v-btn elevation="8" size="large" class="v-theme--light bg-light-blue-lighten-1 text-white">Llamar</v-btn>
                    </div>
                </div>

            </v-parallax>
        </div>


        <div class="container up">
            <v-container fluid>
                <v-row>
                    <v-col cols="12" md="6">
                        <v-img src="Trabajos_Carrusel.gif" alt="Descripción de la imagen" max-width="80%" contain></v-img>
                    </v-col>
                    <v-col cols="12" md="6">
                        <div>
                            <div class="text-h5 font-weight-bold up" style="color:#29AAE3">La mejor opción</div>
                            <div class="text-h6 up">Ten seguridad mental al saber que tu negocio se encuentra protegido
                                ante posibles delitos.
                            </div>
                        </div>
                        <div>
                            <div class="text-h5 font-weight-bold up" style="color:#29AAE3">Especializados en la seguridad
                            </div>
                            <div class="text-h6 up">Estamos capacitados para poder brindarte la mejor asistencia posible
                                en el momento indicado.
                            </div>
                            <div>
                                <div align-items="center">
                                    <v-row>
                                        <v-col cols="4">
                                            <v-img src="solucion.png" alt="Descripción de la imagen" max-width="40%"
                                                contain></v-img>
                                            <v-card-title style="color: #29AAE3">Soluciones</v-card-title>

                                        </v-col>
                                        <v-col cols="4">
                                            <v-img src="garantia.png" alt="Descripción de la imagen" max-width="40%"
                                                contain></v-img>
                                            <v-card-title style="color: #29AAE3">Garantías<br> reales</v-card-title>
                                        </v-col>

                                        <v-col cols="4">
                                            <v-img src="equipo.png" alt="Descripción de la imagen" max-width="40%"
                                                contain></v-img>
                                            <v-card-title style="color: #29AAE3">Equipo <br> calificado</v-card-title>
                                        </v-col>
                                    </v-row>
                                </div>
                            </div>
                        </div>
                    </v-col>
                </v-row>
            </v-container>
        </div>
        <br>

        <div class="container-sm">
            <v-container>

                <v-row>
                    <v-col cols="4">
                        <v-img class="img-1" src="interfon.jpg" aspect-ratio="1"></v-img>
                    </v-col>
                    <v-col cols="4">
                        <v-img class="img-1" src="conexiones.jpg" aspect-ratio="1"></v-img>
                    </v-col>
                    <v-col cols="4">
                        <v-img class="img-1" src="camaras_seguridad.jpg" aspect-ratio="1"></v-img>
                    </v-col>
                </v-row>

                <v-row>
                    <v-col cols="4">
                    <div class="text-h5 font-weight-bold" style="color:#29AAE3">
                        Interfón y videoporteros
                        
                    </div>
                    </v-col>
                    <v-col cols="4">
                        <div class="text-h5 font-weight-bold" style="color:#29AAE3">
                            Conexiones
                    </div>
                    </v-col>
                    <v-col cols="4">
                        <div class="text-h5 font-weight-bold" style="color:#29AAE3">
                        Cámaras de seguridad 
                    </div>
                    </v-col>
                </v-row>

                <v-row>
                    <v-col cols="4">
                        <div class="text-body-1"> Mayor seguridad y comodidad en la punta de tus dedos. 
                            Con Interfon y Videoporteros, controla quién entra a tu hogar o edificio. 
                            </div>
                    </v-col>
                    <v-col cols="4">
                        <p> la mejor defensa para tu seguridad. Registra entradas y salidas autorizadas, 
                            mejora la eficiencia y garantiza la protección de tu propiedad. </p>
                    </v-col>
                    <v-col cols="4">
                        <p>Previene delitos, disuade y supervisa con eficacia. 
                            Obtén evidencia, mejora procedimientos y ahorra costos de vigilancia.</p>
                    </v-col>
                </v-row>
            </v-container>
        </div>

        <div class="up">


  <v-parallax  src="Portada_trabajos.png">
    <div class="d-flex flex-column fill-height justify-center align-center text-white">
      <h1 class="text-h4 font-weight-thin mb-4">
        ¿Estás en busca de seguridad para tu negocio?
      </h1>
      <h2 class="subheading ">
          Podemos ayudarte
      </h2>
      <v-btn elevation="8" size="large" class="v-theme--light bg-light-blue-lighten-1 text-white">Llamar</v-btn>
    </div>
  </v-parallax>
        </div>
    

        <piedepagina />


</template>

<style>


.up {
    margin-top: 5%;
    margin-bottom: 5%;
    align-content: center;
}





.img-1 {
    border-radius: 20px;
}

.img-2 {
    width: 650px;
    height: 400px;
    padding: 15%;
    border-radius: 80px;

}

.img-3 {
    width: 60%;
}

.section-images .hero-images-container {
    max-width: 346px;
}

.section-images .hero-images-container-1 {
    max-width: 390px;
    position: absolute;
    right: 68%;
    top: 160%;
    padding: 20px;
}



.swiper {
    width: 100%;
    height: 100%;
}

.swiper-slide {
    text-align: center;
    font-size: 18px;
    background: #fff;

    /* Center slide text vertically */
    display: flex;
    justify-content: center;
    align-items: center;
}

.swiper-slide img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>

<script>

import Privacy from './Alet_privacy.vue'
import Header from './Header.vue'
import Palabras from './Swiper-home.vue'
import piedepagina from './Footer.vue'



import { Swiper, SwiperSlide } from 'swiper/vue';

import 'swiper/swiper-bundle.css';



import 'swiper/css';
import { FreeMode, Pagination, Navigation, Autoplay } from 'swiper/modules';


export default {
    name: 'Home',
    components: {
        Header,
        Palabras,
        Swiper,
        SwiperSlide,
        Privacy,
        piedepagina,

    },

    setup() {
        const onSwiper = (swiper) => {
            console.log(swiper);
        };
        const onSlideChange = () => {
            console.log('slide change');
        };
        return {
            modules: [FreeMode, Pagination, Autoplay, Navigation],
            onSwiper,
            onSlideChange,
        };
        

    },
    data() {
        return {
      slides: [
        { 
          title: 'Asegura tu negocio con Acceso Correcto',
          description: 'Sistemas de seguridad, Comunicación, Voz y Datos, Controles de Acceso y Automatización',
          buttonText: 'Conocer trabajo',
          buttonColor: 'bg-light-blue-lighten-1',
          titleColor: '#033f58',
          image: '/phoneloop.gif',
        },
        { 
          title: 'Portería inteligente',
          description: 'Simplifica y digitaliza los accesos a tu negocio, ingresando de manera segura y atendiendo a tus visitantes.',
          buttonText: 'Comprar',
          buttonColor: 'bg-light-blue-lighten-1',
          titleColor: '#033f58',
          image: '/vdc.png',
        },
      ],
    };
  },
 

}


</script>

