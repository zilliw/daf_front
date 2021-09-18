<template class="container">
    <v-layout>
                <TheMenu>
                </TheMenu>
        <v-col>
            <v-row>
                <TheHeader>
                </TheHeader>
            </v-row>
            <v-row class="item">
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

<style >
.container {
        display: flex;
        max-width: 100%;
        max-height: 100%;
}
.item {
        display: flex;
        height: 100%;
        }
</style>