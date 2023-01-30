<template>
  <q-layout view="lHh Lpr lFf">
    <q-header glossy class="bg-red" elevated>
      <q-toolbar color="white">
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />
        <q-btn
          flat
          dense
          round
          icon="search"
          aria-label="Search"
          @click="toggleSearch"
        />

        <q-toolbar-title> Quasar App </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header>Быстрый доступ</q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
    <q-footer class="bg-red" elevated>
      <q-item></q-item>
    </q-footer>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";
import EssentialLink from "components/EssentialLink.vue";

const linksList = [
  {
    title: "Каталог",
    caption: "Продукция компании. Ассортимент и торговые марки",
    type: "section",
    icon: "list",
    link: "../catalog/",
  },
  {
    title: "О компании",
    caption: "Цели и задачи, история и планы на будущее",
    type: "section",
    icon: "badge",
    link: "../about/",
  },
  {
    title: "Контакты",
    caption: "Адреса и телефоны, группы в соцсетях",
    type: "section",
    icon: "chat",
    link: "../contacts/",
  },
];

export default defineComponent({
  name: "MainLayout",

  components: {
    EssentialLink,
  },

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
