<template>
  <q-page class="flex flex-center">
    <q-card
      class="custom-tabsname cursor-pointer bg-white relative-position row flex-center"
    >
      <q-tabs align="left">
        <q-route-tab to="../catalog/" label="Каталог" />
        <q-route-tab to="../about/" label="О компании" />
        <q-route-tab to="../contacts/" label="Контакты" />
      </q-tabs>
    </q-card>
    <q-card
      v-touch-swipe.mouse.up.left.down.right="handleSwipe"
      class="custom-area cursor-pointer bg-white relative-position row flex-center"
    >
      <q-btn
        class="glossy custom-button"
        rounded
        push
        no-caps
        size="xl"
        color="red"
        to="../catalog/"
        label="Каталог"
      />
      <q-btn
        class="glossy custom-button"
        rounded
        push
        no-caps
        size="xl"
        color="red"
        to="../about/"
        label="О компании"
      />
      <q-btn
        class="glossy custom-button"
        rounded
        push
        no-caps
        size="xl"
        color="red"
        to="../contacts/"
        label="Контакты"
      />
    </q-card>
  </q-page>
</template>

<style lang="sass" scoped>
.custom-tabsname
  width: 95vw
  height: 5vh
  border-radius: 0
  padding: .1%
  box-shadow: none
.custom-area
  width: 95vw
  height: 80vh
  border-radius: 0
  padding: .1%
  box-shadow: none
.custom-button
  margin: .15rem .5rem
</style>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "CatalogPage",
});
</script>
