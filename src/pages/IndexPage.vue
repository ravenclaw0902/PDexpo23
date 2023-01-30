<template>
  <q-page class="flex flex-center">
    <q-btn
      align="around"
      class="glossy"
      rounded
      no-caps
      size="xl"
      color="red"
      to="/catalog"
      label="Каталог"
    />
    <q-btn
      align="around"
      class="glossy"
      rounded
      no-caps
      size="xl"
      color="red"
      to="/about"
      label="О компании"
    />
    <q-btn
      align="around"
      class="glossy"
      rounded
      no-caps
      size="xl"
      color="red"
      to="/contacts"
      label="Контакты"
    />
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
});
</script>
