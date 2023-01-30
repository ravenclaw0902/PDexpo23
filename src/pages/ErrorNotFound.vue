<template>
  <div
    class="fullscreen bg-red text-white text-center q-pa-md flex flex-center"
  >
    <div>
      <div style="font-size: 30vh">404</div>

      <div class="text-h2" style="opacity: 0.6">
        Похоже, такой страницы не существует...
      </div>

      <q-btn
        align="around"
        class="q-mt-xl glossy"
        rounded
        color="white"
        text-color="red"
        unelevated
        to="/"
        label="Вернуться в начало"
        no-caps
      />
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "ErrorNotFound",
});
</script>
