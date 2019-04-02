<template>
<div>
  <v-toolbar dark color="primary" class="fix">
   <v-toolbar-side-icon
          
          dark
          @click.stop="drawer = !drawer"
        >
        </v-toolbar-side-icon>
  

    <v-toolbar-title class="white--text">Northside Youth Soccer League </v-toolbar-title>

    <v-spacer></v-spacer>

  </v-toolbar>
  <v-layout
    wrap
    style="height: 200px;"
  >
      

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list class="pa-1">
        <v-list-tile avatar>
          <v-list-tile-avatar>
            <img src="https://randomuser.me/api/portraits/men/85.jpg">
          </v-list-tile-avatar>

          <v-list-tile-content>
            <v-list-tile-title>John Leider</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>

      <v-list class="" dense>
        <v-divider></v-divider>

        <v-list-tile
          v-for="item in items"
          :key="item.title"
          @click="v-on"
        >
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>

          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
  </v-layout>
  </div>
</template>


<script>
export default {
    name:'hearder',
    data () {
      return {
        drawer: null,
        items: [
          { title: 'Home', icon: 'dashboard' },
          { title: 'About', icon: 'question_answer' }
        ]
      }
    }
  }
</script>
<style scoped>

.fix
{
    top: 0px;
    position:fixed;
}
</style>

