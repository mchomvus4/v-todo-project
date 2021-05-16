<template>
  <nav>
   <v-main >
   <v-toolbar>
    <v-app-bar-nav-icon class="indigo--text" @click.stop="drawer = !drawer"></v-app-bar-nav-icon> 
    <v-toolbar-title class="text-uppercase blue--text">
     <span class="font-weight-light"></span> &nbsp;
     <span>NOTTECH Lab</span>
    </v-toolbar-title>
    <v-spacer></v-spacer>
     <v-btn text>
      <v-icon>mdi-logout</v-icon>
      <span>logout</span>
     </v-btn>
   </v-toolbar>
   <v-navigation-drawer app v-model="drawer" class="primary">
    <v-list>
     <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
      <v-list-item-action>
       <v-icon class="white--text">{{link.icon}}</v-icon>
      </v-list-item-action>
      <v-list-item-content>
       <v-list-item-title class="white--text">{{link.text}}</v-list-item-title>
      </v-list-item-content>
     </v-list-item>
    </v-list>
   </v-navigation-drawer>
   </v-main>
  </nav>
  
</template>

<script>
export default {
data() {
 return {
  drawer: false,
  links:[
   {icon: 'mdi-view-dashboard', text:'Dashboard', route:'/'},
   {icon: 'mdi-folder', text:'My Project', route:'/projects'},
   {icon: 'mdi-account-group', text:'Team', route:'/team'},
  ]
 }
},
}
</script>



