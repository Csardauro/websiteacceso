<script>
export default {
    name: 'Palabras'
}
</script>

<template>
<body>
    <div class="animated-text">
      <div class="line">Acceso inteligente</div>
      <div class="line">Seguridad inteligente</div>
      <div class="line">Negocio inteligente</div>
      <div class="line"></div>

    </div>
  </body>
</template>

<style>


.animated-text{
  color: #29AAE3;
  position: absolute;
  height: 40px;
  overflow: hidden;
  font-family: 'Open Sans', sans-serif;
}

.line{
  text-align: left;
  font-size: 22px;
  line-height: 60px;
}

.line:first-child{
  animation: anim 10s infinite ;
}

@keyframes anim {
  0%{
    margin-top: 0px;
  }
  16%{
    margin-top: -60px;
  }
  33%{
    margin-top: -120px;
  }
  50%{
    margin-top: -180px;
  }
  66%{
    margin-top: -120px;
  }
  82%{
    margin-top: -60px;
  }
  100%{
    margin-top: 0px;
  }
}

</style>