<template>
  <q-item
    clickable
    tag="a"
    target="_self"
    :href="link"
    type="button"
    class="flex-center row brand-item"
  >
    <q-item-section>
      <q-img
        :name="title"
        src="/imgs/image-1x.png"
        srcset="/imgs/image-1x.png 400w,
        /imgs/image-2x.png 800w,
        /imgs/image-3x.png 1200w,
        /imgs/image-4x.png 1600w"
        sizes="(max-width:400px) 400w,
        (min-width: 400px) and (max-width: 800px) 800w,
        (min-width: 800px) and (max-width: 1200px) 1200w,
        (min-width: 1200px) 1600w"
        style="height: 280px; max-width: 300px"
      />
    </q-item-section>
    <q-item-section>
      <q-item-label>{{ title }}</q-item-label>
      <q-item-label caption>{{ caption }}</q-item-label>
    </q-item-section>
  </q-item>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "BrandItemList",
  props: {
    brand: {
      type: String,
      required: true,
    },

    item: {
      type: String,
      default: "",
    },

    title: {
      type: String,
      required: true,
    },

    caption: {
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
