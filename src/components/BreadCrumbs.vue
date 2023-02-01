<template>
  <q-breadcrumbs-el :label="label" :to="link" />
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "BreadCrumbs",
  props: {
    title: {
      type: String,
      required: true,
    },

    label: {
      type: String,
      default: "",
    },

    link: {
      type: String,
      default: "#",
    },
  },
});
</script>
