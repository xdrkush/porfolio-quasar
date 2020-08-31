<template>
  <q-layout view="hHh Lpr lff" container style="height: 100vh" class="shadow-2 rounded-borders">
    <q-header elevated class="bg-black">
      <q-toolbar>
        <q-btn flat @click="drawer = !drawer" round dense icon="menu" />
        <q-toolbar-title>Hsuk Rd</q-toolbar-title>
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
          <q-item clickable v-ripple to="/">
            <q-item-section avatar>
              <q-icon name="inbox" />
            </q-item-section>

            <q-item-section>Acceuil</q-item-section>
          </q-item>
          <q-separator></q-separator>

          <q-item clickable v-ripple to="/about">
            <q-item-section avatar>
              <q-icon name="inbox" />
            </q-item-section>

            <q-item-section>Présentation</q-item-section>
          </q-item>
          <q-separator></q-separator>

          <q-item clickable v-ripple to="/contact">
            <q-item-section avatar>
              <q-icon name="star" />
            </q-item-section>

            <q-item-section>me contacter,</q-item-section>
          </q-item>

          <q-item clickable v-ripple to="/social">
            <q-item-section avatar>
              <q-icon name="send" />
            </q-item-section>

            <q-item-section>réseaux,</q-item-section>
          </q-item>

          <q-separator />

          <q-item clickable v-ripple to="/skill">
            <q-item-section avatar>
              <q-icon name="drafts" />
            </q-item-section>

            <q-item-section>Compétences,</q-item-section>
          </q-item>

          <q-separator />

          <q-item clickable v-ripple to="/project">
            <q-item-section avatar>
              <q-icon name="drafts" />
            </q-item-section>

            <q-item-section>Projets,</q-item-section>
          </q-item>
          <q-separator />

          <q-item clickable v-ripple to="/news">
            <q-item-section avatar>
              <q-icon name="drafts" />
            </q-item-section>

            <q-item-section>news.</q-item-section>
          </q-item>
          <q-separator />
        </q-list>
      </q-scroll-area>
    </q-drawer>

    <q-page-container>
      <q-page>
        <router-view/>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      miniState: true
    }
  }
}
</script>
