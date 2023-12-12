<template>
    <div class="video-container" @click="toggleVideo">
      <div class="poster" v-show="!videoPlaying"></div>
      <div class="play-button" v-show="!videoPlaying"></div>
      <video
        ref="video"
        class="video"
        preload="none"
        poster="portada_video.jpg"
        @ended="resetVideo"
        controls
        controlsList="nodownload"
        disablePictureInPicture
      >
        <source :src="videoSrc" type="video/mp4">
        Tu navegador no admite la reproducción de videos.
      </video>
    </div>
  </template>
  
  
  
  
  <script>
  export default {
    data() {
      return {
        videoPlaying: false,
        videoSrc: "video_prueba.mp4", // Ruta de tu video
      };
    },
    methods: {
      toggleVideo() {
        const video = this.$refs.video;
        if (this.videoPlaying) {
          video.pause();
          this.videoPlaying = false;
        } else {
          video.play();
          this.videoPlaying = true;
        }
      },
      resetVideo() {
        this.videoPlaying = false;
        this.$refs.video.load(); // Vuelve a cargar el video
      },
    },
  };
  </script>
  
  

  
  
  <style scoped>
/* Estilos para el contenedor del video */
.video-container {
  position: relative;
  width: 640px;
  height: 352px;
  margin: 0 auto;
  cursor: pointer;
}

.poster {
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  /* Añadir estilos de imagen de portada */
  background-image: url('Portada_video.jpg');
  background-size: cover;
}

/* Estilos para el botón de reproducción */
.play-button {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 60px;
  height: 60px;
  background-color: rgba(0, 0, 0, 0.5);
  border-radius: 50%;
  cursor: pointer;
}

/* Estilos para el icono de reproducción */
.play-button::after {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-40%, -50%);
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 12px 0 12px 18px;
  border-color: transparent transparent transparent #fff;
}

/* Estilos para la capa de reproducción */
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  cursor: pointer;
}

/* Estilos para el video */
.video {
  position: relative;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: none;
}

/* Estilos para los controles de video */
.video::-webkit-media-controls-panel {
  display: flex !important;
  justify-content: space-between !important;
  align-items: center !important;
  width: 100% !important;
  height: 100% !important;
  background: rgba(0, 0, 0, 0.6) !important;
  backdrop-filter: blur(3px) !important;
  color: white !important;
  font-size: 14px !important;
  border: none !important;
}

.video::-webkit-media-controls-play-button {
  color: #fff !important;
  font-size: 24px !important;
}
</style>
