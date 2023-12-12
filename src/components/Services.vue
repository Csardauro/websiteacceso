<template>
    <Header />

    <div class="container">
        <div class="text-no-wrap text-h1 text-center font-weight-black up" style="text-align: center; color:#0d0d0e;">
            Esto es
            <div style="color: #29AAE3; margin-top: -60px;"> <br> Acceso Correcto </div>

        </div>

        <div class="text-h5 up" style="text-align: center;">
            Nuestro sistema de atención al cliente
            <br>permite que los proyectos se hagan de la mejor forma.

        </div>

        <div class="container">
            <img style="width: 7%; display: flex; margin: auto;" src="swipe_servicios.gif" alt="swipe">
        </div>

    </div>

    <div class="container-xxl">
        <img src="portada_servicios.gif" alt="Servicios Acceso Correcto">
    </div>

    <div class="container">
        <swiper :slidesPerView="3" :spaceBetween="30" :pagination="{ clickable: true }" :modules="modules" class="mySwiper"
            :autoplay="true">
            <swiper-slide>
                <div class="slide-content">
                    <img class="img-1" src="/Camaras.jpg" />
                    <h2>Cámaras de Seguridad</h2>
                    <p>Texto descriptivo 1</p>
                </div>
            </swiper-slide>
            <swiper-slide>
                <div class="slide-content">
                    <img class="img-1" src="/Casetas.jpg" />
                    <h2>Control de acceso</h2>
                    <p>Texto descriptivo 2</p>
                </div>
            </swiper-slide>
            <swiper-slide>
                <div class="slide-content">
                    <img class="img-1" src="/Porton.jpg" />
                    <h2>Vehícular</h2>
                    <p>Texto descriptivo 3</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>

    <div class="container-xxl up">
        <img src="cta_servicios.gif" alt="Servicios Acceso Correcto">
    </div>
    <div class="container up">
        <swiper :slidesPerView="3" :spaceBetween="30" :pagination="{ clickable: true }" :modules="modules" class="mySwiper"
            :autoplay="true">
            <swiper-slide>
                <div class="slide-content">
                    <img class="img-1" src="/Camaras.jpg" />
                    <h2>Interfon y Videoporteros</h2>
                    <p>Texto descriptivo 1</p>
                </div>
            </swiper-slide>
            <swiper-slide>
                <div class="slide-content">
                    <img class="img-1" src="/Casetas.jpg" />
                    <h2>Portones y puertas electrónicas</h2>
                    <p>Texto descriptivo 2</p>
                </div>
            </swiper-slide>
            <swiper-slide>
                <div class="slide-content">
                    <img class="img-1" src="/Porton.jpg" />
                    <h2>Cerca eléctrica</h2>
                    <p>Texto descriptivo 3</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>

    <div class="container-xxl up">
        <img src="cta_llamada.gif" alt="Llama a Acceso Correcto">
    </div>

    <div class="container-xxl up">
        <img src="calidad.png" alt="Llama a Acceso Correcto">
    </div>

   

    <piedepagina />
</template>

<script>
import Header from './Header.vue'
import piedepagina from './Footer.vue'
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';


// Import Swiper styles
import 'swiper/css';




export default {
    name: 'Services',
    components: {
        Header,
        piedepagina,
        Swiper,
        SwiperSlide,
    },

    setup() {
        const onSwiper = (swiper) => {
            console.log(swiper);
        };
        const onSlideChange = () => {
            console.log('slide change');
        };
        return {
            onSwiper,
            onSlideChange,
        };

    }
}
</script>

<style>
section {
    background-color: #f8f7f4;
}


.img-1 {
    border-radius: 20px;
    background: #000;
}

.up {
    margin-top: 5%;
    margin-bottom: 5%;
    align-content: center;
}
</style>