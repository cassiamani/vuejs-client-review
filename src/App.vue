<template>
    <q-layout view="hHh Lpr lff" container style="height: 100vh" class="shadow-2">
      <q-header elevated class="bg-white text-grey-8">
        <q-toolbar>
          <q-btn flat @click="drawer = !drawer" round dense icon="fa fa-bars" />
          <q-toolbar-title>Client review</q-toolbar-title>
        </q-toolbar>
      </q-header>

      <q-drawer
        v-model="drawer"
        show-if-above

        :mini="miniState"
        @mouseover="miniState = false"
        @mouseout="miniState = true"

        :width="200"
        :breakpoint="500"
        bordered
        content-class="bg-grey-3"
      >
        <q-scroll-area class="fit">
          <q-list padding>
            <q-item clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="fa fa-user" />
              </q-item-section>

              <q-item-section>
                Client
              </q-item-section>
            </q-item>
          </q-list>
        </q-scroll-area>
      </q-drawer>

      <q-page-container>
        <q-page padding>

          <router-view  />

        </q-page>
      </q-page-container>
    </q-layout>
</template>

<script>

export default {
  name: 'LayoutDefault',

  components: {
  },

  data () {
    return {
      drawer: false,
      miniState: true
    }
  }
}
</script>

<style>
</style>
