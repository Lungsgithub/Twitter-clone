<template>
  <q-layout view="lHr lpR fFf">

    <q-header bordered class="bg-white text-black">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />

        <q-toolbar-title class="text-weight-bold">
          <span class="gt-sm">{{ $route.name }}</span>

          <q-icon  class="q-pa-sm lt-md absolute-center" name="flutter_dash" color="primary"  size="48px" />

        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    
    <q-drawer :width="282" show-if-above v-model="leftDrawerOpen" side="left" bordered>
      <q-icon  class="q-pa-sm" name="flutter_dash" color="primary" size="64px" />

      <q-list>
      <q-item to="/" clickable v-ripple exact>

        <q-item-section avatar>

          <q-icon name="home" />
        </q-item-section>

        <q-item-section class = "text-h6 text-weight-bold">Home</q-item-section>
      </q-item>


      <q-item to="/about" clickable v-ripple exact>

      <q-item-section avatar>

      <q-icon  name="help" />

      </q-item-section>

<q-item-section class = "text-h6 text-weight-bold">About</q-item-section>
</q-item>

      
      </q-list>
    
    </q-drawer>

    <q-drawer show-if-above v-model="rightDrawerOpen" side="right" bordered>
      
       <q-input placeholder="Search Twitter" dense rounded outlined class="q-ma-md">
        <template>
          <q-icon name="search"/>
        </template>
       </q-input>



    <q-list separator padding>
      <q-item class="q-pa-md">
        <q-item-section>
          <q-item-label overline class="text-grey text-weight-bold">Education</q-item-label>
          <q-item-label>Great stuff</q-item-label>
          <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
        </q-item-section>

        <q-item-section side top>
          <q-item-label caption>5 min ago</q-item-label>
        </q-item-section>
      </q-item>

      <q-item class="q-pa-md">
        <q-item-section>
          <q-item-label overline class="text-grey text-weight-bold">Education</q-item-label>
          <q-item-label>Great stuff</q-item-label>
          <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
        </q-item-section>

        <q-item-section side top>
          <q-item-label caption>5 min ago</q-item-label>
        </q-item-section>
      </q-item>



      <q-item class="q-pa-md">
        <q-item-section>
          <q-item-label overline class="text-grey text-weight-bold">Education</q-item-label>
          <q-item-label>Great stuff</q-item-label>
          <q-item-label caption>Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
        </q-item-section>

        <q-item-section side top>
          <q-item-label caption>5 min ago</q-item-label>
        </q-item-section>
      </q-item>


      




    </q-list>

    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    const leftDrawerOpen = ref(false)
    const rightDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      },

      rightDrawerOpen,
      toggleRightDrawer () {
        rightDrawerOpen.value = !rightDrawerOpen.value
      }
    }
  }
}
</script>