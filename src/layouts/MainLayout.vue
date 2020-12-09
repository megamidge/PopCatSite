<template>
  <q-layout view="hHh lpR fFf q-pa-none" style="min-height:100vh;max-height:100vh;">

    <q-page-container style="min-height:100vh;max-height:100vh;">
      <router-view />
    </q-page-container>

    <q-footer class="bg-white">
      <q-toolbar>
        <attributes/>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
import Attributes from 'src/components/Attributes.vue'
export default {
  components: { Attributes },
  data () {
    return {
    }
  }
}
</script>
