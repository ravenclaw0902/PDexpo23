<template>
  <div
    class="fullscreen bg-red text-white text-center q-pa-md flex flex-center"
  >
    <div>
      <div style="font-size: 25vh">404</div>

      <div class="text-h2" style="opacity: 0.6">
        Похоже, такой страницы не существует...
      </div>
      <div style="margin: 1rem auto auto">
        <q-btn
          class="glossy"
          rounded
          color="white"
          text-color="red"
          unelevated
          size="md"
          to="/"
          label="Вернуться в начало"
          no-caps
        />
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "ErrorNotFound",
});
</script>
