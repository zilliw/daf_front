<template>
<v-container class="flex-container">
  <v-simple-table
  :headers="headers"
  >
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">
            Code
          </th>
          <th class="text-left">
            Code enfant
          </th>
          <th class="text-left">
            Client
          </th>
         <th class="text-left">
            Nom
          </th>
         <th class="text-left">
            Département
          </th>
         <th class="text-left">
            Utilisateur
          </th>
         <th class="text-left">
            Prestation
          </th>
         <th class="text-left">
            Statut
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in desserts"
          :key="item.code"
        >
          <td>{{ item.code }}</td>
          <td>{{ item.childcode }}</td>
          <td>{{ item.client }}</td>
          <td>{{ item.name }}</td>
          <td>{{ item.department }}</td>
          <td>{{ item.user }}</td>
          <td>{{ item.delivery }}</td>
          <td>{{ item.status }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
</v-container>
</template>


<script>
  export default {
    data () {
      return {
        desserts: [
          {
            code: '1',
            childcode: "1.1",
            client: "Allianz",
            name: "Allianz - Maintenance 2021",
            department: "Observatoire",
            user: "William A",
            delivery: "XX",
            status: "En cours"
},
          {
            code: '2',
            childcode: "2",
            client: "BPCE",
            name: "BPCE - Maintenance 2021",
            department: "Gestion Patrimoine",
            user: "Saliou S",
            delivery: "XX",
            status: "En cours"
},
        ],
        headers:[
          {
            sortable:false,
          }
        ]

      }
    },
  }
</script>

<style scoped>

.flex-container {
  padding: 10px;
  margin: 0;
  display: flex;
  flex-direction: column;
}

</style>