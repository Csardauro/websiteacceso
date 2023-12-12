<script>
export default {
    name: 'Privacy',
}
</script>

<template>
    <v-alert
      type="mdiLockOutline"
      title="Aviso de privacidad"
      text="Utilizamos cookies y tecnologías similares para personalizar el contenido, adaptar los anuncios y medir su eficacia, así como para ofrecer una mejor experiencia. Al hacer clic en Vale o activar una opción en las Preferencias de cookies, aceptas lo establecido en nuestra Política de Cookies. Para cambiar tus preferencias o retirar tu consentimiento, actualiza tus Preferencias de cookies."
      variant="tonal"
> 

<template v-slot:actions>
      <v-btn height="48">
        No Thanks
      </v-btn>

      <v-btn
        :loading="loading"
        class="flex-grow-1"
        height="48"
        variant="tonal"
        @click="load"
      >
        Take Checkup
      </v-btn>
    </template>


    ></v-alert>
  </template>

<style>
</style>