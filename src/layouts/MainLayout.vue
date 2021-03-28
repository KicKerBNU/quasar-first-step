<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
          v-if="!mobile"
        />

        <q-toolbar-title>
          Everton Buzzi
        </q-toolbar-title>

        <div v-if="!mobile">
          Welcome to my personal web site
        </div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label header class="text-grey-8">
          Essential Links
        </q-item-label>
        <EssentialComponents
          v-for="router in essentialRouts"
          :key="router.title"
          v-bind="router"
        />
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
  </q-layout>
</template>

<script>
import { Platform } from "quasar";
import EssentialComponents from "components/EssentialComponents.vue";
import EssentialLink from "components/EssentialLink.vue";

const linksData = [
  {
    title: "Twitter",
    caption: "@EvertonBuzzi",
    icon:
      "img:https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/twitter.png?alt=media",
    link: "https://twitter.com/evertonbuzzi"
  },
  {
    title: "GitHub",
    caption: "@KicKerBNU",
    icon:
      "img:https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/github.png?alt=media",
    link: "https://github.com/KicKerBNU"
  },
  {
    title: "Linkedin",
    caption: "@EvertonBuzzi",
    icon:
      "img:https://firebasestorage.googleapis.com/v0/b/fin-backend.appspot.com/o/linkedin.png?alt=media",
    link: "https://br.linkedin.com/in/evertonbuzzi"
  }
];
const routsData = [
  {
    title: "Home",
    caption: "",
    icon: "home",
    link: "",
    routs: "/"
  },
  {
    title: "Curriculum",
    caption: "",
    icon: "school",
    link: "",
    routs: "curriculum"
  },
  {
    title: "Stack",
    caption: "",
    icon: "code",
    routs: "stack"
  },
  {
    title: "About Me",
    caption: "",
    icon: "chat",
    routs: "aboutMe"
  },
  {
    title: "Find Me",
    caption: "",
    icon: "record_voice_over",
    routs: "findMe"
  }
];

export default {
  name: "MainLayout",
  components: { EssentialLink, EssentialComponents },
  data() {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData,
      essentialRouts: routsData,
      mobile: false
    };
  },
  mounted() {
    this.mobile = !Platform.is.desktop;
  }
};
</script>
