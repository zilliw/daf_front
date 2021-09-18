<template>
    <v-card flat>
      <v-navigation-drawer
        permanent
        color="#fafbfc"
      >


          <v-list>
              <v-list-group
                v-for="menu in menus"
                :key="menu.title"
                v-model="menu.active"
                :prepend-icon="menu.action"
                no-action
              >
                  <template v-slot:activator>
                    <v-list-item-content>
                      <v-list-item-title v-text="menu.title" class="menu"></v-list-item-title>
                    </v-list-item-content>
                  </template>
                  <v-list-item
                    v-for="child in menu.items"
                    :key="child.title"
                            >
                    <v-list-item-content>
                      <v-list-item-title v-text="child.title" class="menu"></v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
              </v-list-group>
          </v-list>
      </v-navigation-drawer>
    </v-card>
</template>

<script>
export default {
  data: () => ({
    menus: [
      {
        action: 'mdi-cash-multiple',
        title: 'Affaires',
        items: [
          { title: 'Affaires' },
          { title: 'Suivi des temps' },
        ]
      },
    ]
  })
}
</script>

<style scoped>
    .menu {
      font-size: 12px;
      border: #1E75BA;
    }
    .logo {
      padding-left: 10px;
      padding-right: 10px;
    }
</style>