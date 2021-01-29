<template>
   <nav>
       <v-app-bar  color="white" dark app class="line" >
           <v-toolbar-title class="text-uppercase red--text" >
               <span class="font-weight-light">Cloud </span>
               <span>Inventory</span>
           </v-toolbar-title>
            <template>
              <v-btn
                color="red"
                dark
                small
                absolute
                bottom
                right
                fab
              >
                <v-icon>mdi-plus</v-icon>
              </v-btn>
            </template>
       </v-app-bar>
      <v-navigation-drawer  v-model="drawer" dark app mini-variant class="red">

          <v-list flat>
               <v-list-item class="mb-12">
                  <v-list-item-action>
                     <v-icon >fas fa-cloud-download-alt</v-icon>
                  </v-list-item-action>
              </v-list-item>
              <v-list-item  router to="/">
                  <v-list-item-action>
                     <v-icon >fas fa-desktop</v-icon>
                  </v-list-item-action>
              </v-list-item>
              <v-list-item  router to="/">
                  <v-list-item-action>
                      <v-badge color="yellow" >
                        <template v-slot:badge>1</template>
                        <v-icon >fas fa-shopping-cart</v-icon>
                    </v-badge>
                    
                  </v-list-item-action>
              </v-list-item>
              <v-list-item  router to="/">
                  <v-list-item-action>
                     <v-icon >fas fa-city</v-icon>
                  </v-list-item-action>
              </v-list-item>
              <v-list-item  router to="/">
                  <v-list-item-action>
                     <v-icon >fas fa-cog</v-icon>
                  </v-list-item-action>
              </v-list-item>
          </v-list>
          <v-list  style="position: absolute; bottom:0" class="ml-3" flat>
            <v-list-item  router to="/">
                  <v-list-item-action>
                     <v-icon >fas fa-sign-out-alt</v-icon>
                  </v-list-item-action>
              </v-list-item>
          </v-list>
      </v-navigation-drawer>
   </nav>
</template>
<script>
export default {
   data: () => ({
      drawer: true,
      links :[
          {icon: 'fas fa-desktop', route: '/'},
          {icon: 'fas fa-shopping-cart',  route: '/shopping'},
          {icon: 'fas fa-city',  route: '/city'},
          {icon: 'fas fa-cog',  route: '/cog'}
      ]
     
    }),
    components: {

  },

   
}
</script>
<style scoped>
.border {
  border-left: 4px solid #0ba518;
}
</style>
