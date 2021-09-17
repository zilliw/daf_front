<template>
    <v-layout>
        <TheMenu>
        </TheMenu>
        <v-col>
          <v-row>
        <TheHeader>
        </TheHeader>
          </v-row>

        </v-col>
  </v-layout>
</template>

<script>
import TheHeader from './TheHeader'
import TheMenu from './TheMenu'

export default {
  components: {
    TheHeader,
    TheMenu,
  }
}
</script>
