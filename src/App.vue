<template>
  <!-- <div class="q-pa-md"> -->
    <q-layout view="hHh Lpr lff" container style="height: 100vh" class="shadow-2">
      <q-header elevated class="bg-black">
        <q-toolbar>
          <q-btn flat @click="drawer = !drawer" round dense icon="fa fa-bars" />
          <q-toolbar-title>Header</q-toolbar-title>
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
          <p v-for="n in 15" :key="n">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
          </p>
        </q-page>
      </q-page-container>
    </q-layout>
  <!-- </div> -->
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'LayoutDefault',

  components: {
    // HelloWorld
  },

  data () {
    return {
      leftDrawerOpen: false,
      drawer: false,
      miniState: true
    }
  }
}
</script>

<style>
</style>
