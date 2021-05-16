<template>
 <div class="dashboard">
   <h1 class="subheading grey--text">Dashboard</h1>
   <v-container  class="my-5">
     <v-card class="pa-6" v-for="project in projects" :key="project.title">
       <v-layout row :class="`pa-3  project ${project.status}`">

         <v-flex xs12 md6>
           <div class="caption grey--text">Project Title</div>
           <div>{{project.title}}</div>
         </v-flex>

         <v-flex xs6 sm4 md2>
            <div class="caption grey--text">Person</div>
            <div>{{project.person}}</div>
         </v-flex>

          <v-flex xs6 sm4 md2>
            <div class="caption grey--text">Due by</div>
            <div>{{project.due}}</div>
         </v-flex>

          <v-flex xs2 sm4 md2>
           <div>
             <v-chip small :class="` done ${project.status} white--text caption my-2`">{{project.status}}</v-chip>
           </div>
         </v-flex>
       </v-layout>
     
     </v-card>
   </v-container>
    
 </div>
</template>

<script>
 

  export default {
    data() {
      return {
        projects:[
          {title:'Risk Management System', person:'Samwel Mchomvu',due:'30th May 2021',status:'Ongoing',contenet:'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s'},
          {title:'AI for Maternal & Child Health', person:'Samwel Mchomvu',due:'25th Fed 2021',status:'Completed',contenet:'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s'},
          {title:'WakaPay', person:'Sajad',due:'30th March 2021',status:'Completed',contenet:'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s'},
          {title:'E-Service', person:'Stephan',due:'30th May 2021',status:'Ongoing',contenet:'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s'},
          {title:'DSSA', person:'Adam',due:'30th May 2021',status:'Ongoing',contenet:'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s'},
        ]
      }
    },
  }
  
</script>

<style >
.project.Completed{
  border-left: 0.25rem solid #3cd1c2;
}
.project.Ongoing{
  border-left: 0.25rem solid orange;
}
.project.Overdue{
  border-left: 0.25rem solid tomato;
}
.v-chip.Completed{
    background:  #3cd1c2;
}
.v-chip.Ongoing{
    background:  orange;
}
.v-chip.Overdue{
    background:  tomato;
}

</style>
