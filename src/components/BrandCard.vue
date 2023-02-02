<template>
  <q-card :to="link">
    <q-item class="flex flex-center brand-img">
      <q-img>{{ logo }}</q-img>
      <q-btn :href="link" target="_blank" label="Сайт бренда" />
    </q-item>
    <q-item class="flex flex-center brand-text">
      <h2 class="brand-title">{{ title }}</h2>
      <span class="brand-subtitle">{{ subtitle }}</span>
      <div class="brand-descr">{{ descr }}</div>
    </q-item>
  </q-card>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "BrandCard",
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      default: "",
    },
    descr: {
      type: String,
      default: "",
    },
    logo: {
      type: String,
      default: "",
    },
    link: {
      type: String,
      default: "",
    },
  },
});
</script>
