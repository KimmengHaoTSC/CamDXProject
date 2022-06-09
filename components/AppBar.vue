<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      dark
      color="#16184E"
      fixed
      app
      temporary
    >
      <v-col cols="12" class="d-flex">
        <v-img
          :src="require('@/assets/CamDxLogo.png')"
          :contain="true"
          height="40"
        ></v-img>
      </v-col>
      <v-divider />
      <v-list>
        <v-list-item-group v-for="(item, i) in items" :key="i" color="primary">
          <v-list-item v-if="!item.submenu" :to="item.to">
            <!-- <v-list-item-action>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-action> -->
            <v-list-item-content>
              <v-list-item-title v-text="item.title" />
            </v-list-item-content>
          </v-list-item>
          <v-list-group v-else :prepend-icon="item.icon" no-action>
            <template #activator>
              <v-list-item-content>
                <v-list-item-title v-text="item.title"></v-list-item-title>
              </v-list-item-content>
            </template>
            <v-list-item
              v-for="(child, index) in item.submenu"
              :key="index"
              :to="child.to"
            >
              <v-list-item-content>
                <v-list-item-title v-text="child.title"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-group>
        </v-list-item-group>
        <v-list-item
          v-for="locale in availableLocales"
          :key="locale.code"
          @click="$i18n.setLocale(locale.code)"
        >
          <v-list-item-icon>
            <v-icon> mdi-web-box </v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ $t('language') }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      v-scroll="onScroll"
      fixed
      app
      height="64"
      elevate-on-scroll
      dark
      color="#16184E"
    >
      <!-- <v-container> -->
      <nuxt-link to="/" class="d-flex">
        <v-img
          :src="require('@/assets/CamDxLogo.png')"
          :contain="true"
          height="45"
        ></v-img>
      </nuxt-link>
      <v-spacer />

      <template v-for="(name, menuitem) in items.slice(0, 4)">
        <template v-if="name.submenu">
          <v-menu
            :key="menuitem"
            offset-y
            transition="slide-y-transition"
            bottom
          >
            <template #activator="{ on, attrs }">
              <v-btn
                plain
                class="py-5 submenubtn hidden-sm-and-down text-capitalize"
                :ripple="false"
                v-bind="attrs"
                style="height: auto"
                v-on="on"
              >
                {{ name.title }}
                <v-icon right small class="mx-0"> mdi-chevron-down </v-icon>
              </v-btn>
            </template>
            <v-list dense>
              <v-list-item
                v-for="item in name.submenu"
                :key="item.title"
                link
                :to="item.to"
              >
                <v-list-item-title class="text-capitalize">{{
                  item.title
                }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </template>
        <v-btn
          v-else
          :key="menuitem"
          depressed
          tile
          plain
          class="py-8 hidden-sm-and-down text-capitalize"
          :to="name.to"
          >{{ name.title }}<v-icon>{{ name.icon }}</v-icon>
        </v-btn>
      </template>
      <v-btn
        v-for="locale in availableLocales"
        :key="locale.code"
        depressed
        tile
        plain
        class="py-8 hidden-sm-and-down text-capitalize"
        @click="$i18n.setLocale(locale.code)"
      >
        <v-icon>mdi-web-box</v-icon>{{ $t('language') }}
      </v-btn>
      <v-app-bar-nav-icon class="hidden-md-and-up" @click="drawer = !drawer" />

      <template v-if="fabTab" #extension>
        <Tab
          v-show="fabTab"
          :tabbgcolor="'#16184E'"
          data-aos="zoom-in-up"
          data-aos-duration="500"
        ></Tab>
      </template>
    </v-app-bar>
  </div>
</template>

<script>
import Tab from './Home/Tab.vue'

export default {
  components: { Tab },
  data() {
    return {
      clipped: false,
      drawer: false,
      fabTab: false,
      items: [
        {
          icon: '',
          title: 'CamDigiKey',
          to: '/',
        },
        {
          icon: '',
          title: 'OBR',
          to: '/obr',
        },
        {
          icon: '',
          title: 'Resources',
          submenu: [
            {
              title: 'Event Calendar',
              to: '/inspire',
            },
            {
              title: 'Press Release',
              to: '/index1',
            },
            {
              title: 'Documents',
              to: '/#',
            },
          ],
        },
        {
          icon: 'mdi-open-in-new',
          title: 'Monitoring',
          to: '/monitor',
        },
      ],
      Tabitems: [
        {
          label: 'Overview',
          to: 'overview',
        },
        {
          label: 'Principles',
          to: 'principles',
        },
        {
          label: 'CamDigiKey',
          to: 'camdigikey',
        },
        {
          label: 'Service',
          to: 'service',
        },
        {
          label: 'F.A.Q',
          to: 'faq',
        },
        {
          label: 'Contact',
          to: 'contact',
        },
      ],
    }
  },
  computed: {
    availableLocales() {
      return this.$i18n.locales.filter((i) => i.code !== this.$i18n.locale)
    },
  },
  methods: {
    onScroll(e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset || e.target.scrollTop || 0
      this.fabTab = top > 1000 && this.$route.path === '/'
    },
  },
}
</script>