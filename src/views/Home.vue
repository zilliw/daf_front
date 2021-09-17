<template>
    <v-layout>
        <TheMenu>
        </TheMenu>
        <v-col>
          <v-row>
        <TheHeader>
        </TheHeader>
          </v-row>
          <v-row>
<OpportunityTable>
</OpportunityTable>
            </v-row>
        </v-col>
  </v-layout>
</template>

<script>
import TheHeader from './TheHeader'
import TheMenu from './TheMenu'
import OpportunityTable from './OpportunityTable'

export default {
  components: {
    TheHeader,
    TheMenu,
    OpportunityTable
  }
}
</script>
