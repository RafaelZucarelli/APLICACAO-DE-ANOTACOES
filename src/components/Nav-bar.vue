<template>
  <v-app>
  
    <v-navigation-drawer app dark color="blue" v-model="drawer">
      <v-list>
        <v-list-item to="/HomePage" class="nav-link">Página Inicial</v-list-item>
        <v-list-item to="/Notes" class="nav-link">Anotações</v-list-item>
      
      </v-list>
    </v-navigation-drawer>
    
    <v-app-bar app dark color="blue">
      <v-btn icon @click="drawer = !drawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn>
      <v-toolbar-title class="logo">Bloco de Anotações</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <v-container>
        <router-view></router-view> 
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      drawer: false,
    };
  },
};
</script>

<style scoped>
.logo {
  color: white;
  font-size: 1.5em;
}
.nav-link {
  color: black; 
  text-decoration: none;
  padding: 8px 12px;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}
.nav-link:hover {
  background-color: #555;
  text-decoration: underline;
}
.nav-link.router-link-active {
  background-color: #555;
  font-weight: bold;
}
.v-main {
  padding-left: 300px; 
}
</style>
