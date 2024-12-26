<script setup lang="ts">
  const { MainButton, useWebAppPopup, useWebApp } = await import('vue-tg')
  
  const { showAlert } = useWebAppPopup()

  const { initDataUnsafe } = useWebApp()
</script>

<template>
    <section>
        <h1>Hello Telegram Mini App Game Creator</h1>

        <h2> Ваше имя это {{initDataUnsafe.user?.username}} </h2>

        <MainButton text="Вот она я" color="rgba(0, 191,111,1)" @click="() => showAlert('А вот и сообщение')" />
    </section>
</template>

<style scoped>


</style>