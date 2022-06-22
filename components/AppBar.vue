<template>
  <div>
    <v-navigation-drawer v-model="drawer" class="backgroundTheme" dark fixed app temporary>
      <v-col align-self="start">
        <v-img :src="require('@/assets/CamDxLogo.png')" :contain="true" height="40"></v-img>
      </v-col>
      <v-divider />
      <v-list>
        <v-list-item-group v-for="(item, i) in items" :key="i">
          <v-list-item v-if="!item.submenu" :to="item.to">
            <v-list-item-content>
              <v-list-item-title class="textSize" v-text='$t(item.title)' />
            </v-list-item-content>
          </v-list-item>
          <v-list-group v-else :prepend-icon="item.icon" no-action>
            <template #activator>
              <v-list-item-content>
                <v-list-item-title class="textSize" v-text='$t(item.title)'></v-list-item-title>
              </v-list-item-content>
            </template>
            <v-list-item v-for="(child, index) in item.submenu" :key="index" :to="child.to">
              <v-list-item-content>
                <v-list-item-title v-text='$t(child.title)'></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-group>
        </v-list-item-group>
        <v-list-item href="https://monitoring.camdx.gov.kh" target="_blank">
          <v-list-item-content>
            <v-list-item-title class="textSize" >{{ $t('appbar.monitoring') }}</v-list-item-title>
          </v-list-item-content>
          <v-list-item-icon>
            <v-icon> mdi-open-in-new </v-icon>
          </v-list-item-icon>

        </v-list-item>
        <v-list-item v-for="locale in availableLocales" :key="locale.code" @click="$i18n.setLocale(locale.code)">
          <v-list-item-icon>
            <v-icon> mdi-web-box </v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title class="textSize" >{{ $t('language') }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar v-scroll="onScroll" fixed app height="64" elevate-on-scroll dark class="backgroundTheme">
      <!-- <v-container> -->
      <v-app-bar-nav-icon class="hidden-md-and-up" @click="drawer = !drawer" />
      <nuxt-link to="/" class="d-flex">
        <v-img :src="require('@/assets/CamDxLogo.png')" :contain="true" height="45"></v-img>
      </nuxt-link>

      <v-spacer />

      <template v-for="(item, index) in items.slice(0, 4)">
        <template v-if="item.submenu">
          <v-menu :key="index" offset-y transition="slide-y-transition" open-on-hover :close-on-content-click="false">
            <template #activator="{ on, attrs }">
              <v-btn 
                plain class="py-5 submenubtn hidden-sm-and-down text-capitalize" :ripple="false" v-bind="attrs"
                style="height: auto" v-on="on">
                {{ $t(item.title) }}
                <v-icon right small class="mx-0"> mdi-chevron-down </v-icon>
              </v-btn>
            </template>
            <v-list dense class="listItem">
              <v-list-item v-for="(subitem, subindex) in item.submenu" :key="subindex" link :to="subitem.to">
                <v-list-item-title class="text-capitalize">
                  {{ $t(subitem.title) }}
                </v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </template>
        <v-btn v-else :key="index" depressed tile plain class="py-8 hidden-sm-and-down text-capitalize" :to="item.to">{{
            $t(item.title)
        }}<v-icon>{{ item.icon }}</v-icon>
        </v-btn>
      </template>
      <v-btn depressed tile plain class="py-8 hidden-sm-and-down text-capitalize" href="https://monitoring.camdx.gov.kh/" target="_blank">
        {{ $t('appbar.monitoring') }}
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
      <v-btn 
        v-for="locale in availableLocales" :key="locale.code" depressed tile plain
        class="py-8 hidden-sm-and-down text-capitalize" @click="$i18n.setLocale(locale.code)">
        <v-icon>mdi-web-box</v-icon>{{ $t('language') }}
      </v-btn>
      <!-- <v-app-bar-nav-icon class="hidden-md-and-up" @click="drawer = !drawer" /> -->
      <v-icon v-if="$route.path === '/' || $route.path == '/kh'" v-click-outside="onClickOutside" @click="fabTab = !fabTab">mdi-dots-vertical
      </v-icon>

      <!-- <v-icon class="hidden-md-and-up">mdi-dots-vertical</v-icon> -->
      <template v-if="fabTab" #extension>
        <ListTab></ListTab>
      </template>
    </v-app-bar>
  </div>

</template>

<script>
import ListTab from './Home/ListTab.vue'

export default {
  name: 'AppBarPage',
  components: { ListTab },
  data() {
    return {
      clipped: false,
      drawer: false,
      fabTab: false,
      items: [
        {
          icon: "",
          title: "appbar.camdigikey",
          to: "/",
        },
        {
          icon: "",
          title: "appbar.obr",
          to: "/obr",
        },
        {
          icon: "",
          title: "appbar.resources",
          submenu: [
            {
              title: "appbar.subresources.sub1",
              to: "/#",
            },
            {
              title: "appbar.subresources.sub2",
              to: "/#",
            },
            {
              title: "appbar.subresources.sub3",
              to: "/#",
            },
          ],
        },
      ],
      Tabitems: [
        {
          label: "homePage.tab.overview",
          to: "overview",
        },
        {
          label: "homePage.tab.principles",
          to: "principles",
        },
        {
          label: "homePage.tab.camDigiKey",
          to: "camdigikey",
        },
        {
          label: "homePage.tab.service",
          to: "service",
        },
        {
          label: "homePage.tab.faq",
          to: "faq",
        },
        {
          label: "homePage.tab.contact",
          to: "contact",
        },
      ],
    };
  },
  computed: {
    availableLocales() {
      return this.$i18n.locales.filter((i) => i.code !== this.$i18n.locale);
    },
  },
  methods: {
    onScroll(e) {
      // if (typeof window === 'undefined') return
      // const top = window.pageYOffset || e.target.scrollTop || 0
      // this.fabTab = top > 1000 && this.$route.path === '/'
    },
    onClickOutside() {
      this.fabTab = false
    },
  },
}
</script>
