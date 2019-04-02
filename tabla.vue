
<template>
  <v-card class="trasparencias"> 
    <v-card-title>
      
      <v-spacer></v-spacer>
      <v-text-field
        v-model="search"
        append-icon="search"
        label="Search"
        single-line
        hide-details
      ></v-text-field>
    </v-card-title>
    <v-data-table
      :headers="headers"
      :items="juegos"
      :search="search"
    >
      <template v-slot:items="props">
        <td>{{ props.item.month }}</td>
        <td class="text-xs-right">{{ props.item.day }}</td>
        <td class="text-xs-right">{{ props.item.Teams}}</td>
        <td class="text-xs-right">{{ props.item.location }}</td>
        <td class="text-xs-right">{{ props.item.Times }}</td>
      </template>
      <v-alert v-slot:no-results :value="true" color="error" icon="warning">
        Your search for "{{ search }}" found no results.
      </v-alert>
    </v-data-table>
  </v-card>
</template>



<script>
  export default {
      name:'tabla',
    data () {
      return {
        search: '',
        headers: [
          {
            text: 'Months',
            align: 'left',
            sortable: false,
            value: 'month'
          },
          { text: 'day', value:'day' },
          { text: 'Teams', value: 'Teams' },
          { text: ' Locations', value: 'location' },
          { text: 'Times', value: 'Times' }
        ],
        juegos: [
           { 
    month: 'September',
   day: "9/1",
   Teams:'U1 and U4',
   location:'AJ Katzenmaier',
   Times:'9:30 a.m.' 
  },
  { 
    month: 'September',
    day: "9/1",
   Teams:'U3 and U2',
   location:'Greenbay',
   Times:'1:00 a.m.' 
  },
  {
    month: 'September',
    day: "9/8",
    Teams:'U5 and U6',
    location:'Howard A Yeager',
    Times:'9:30 a.m.'
   },
  { 
    month: 'September',
    day: "9/8",
    Teams:'U6 and U1',
    location:'Marjorie P Hart',
    Times:'1:30 a.m.'
   },
  { 
    month: 'September',
    day: "9/15",
    Teams:'U2 and U4',
    location:'North',
    Times:'9:30 a.m.' 
  },
  { 
    month: 'September',
    day: "9/15",
    Teams:'U3 and U5',
    location:'AJ Katzenmaier',
    Times:'1:00 a.m.'
   },
  {
    month: 'September',
    day: "9/22",
    Teams:'U1 and U3',
    location:'South',
    Times:'9:30 a.m.'
   },
  { 
    month: 'September', 
    day: '9/22',
    Teams:'U2 and U6',
    location:'Howard A Yeager',
    Times:'1:00 a.m.' 
},
  { month: 'September', 
  day: "9/29",
  Teams:'U4 and U5'
  ,location:'Greenbay',
  Times:'9:30 a.m.'
 },
  { 
    month: 'October', 
    day: "10/6",
    Teams:'U2 and U5',
    location:'Howard A Marjorie P Hart',
    Times:'9:30 a.m.'
 },
  { 
    month: 'October', 
    day: "10/6",
    Teams:'U1 and U6',
    location:'South',
    Times:'1:00 a.m.'
 },
  { 
    
    month: 'October',
    day: "10/8",
    Teams:'U3 and U4',
    location:'Howard A Yeager',
    Times:'9:30 a.m.'
   },
  { 
    month: 'October',
    day: "10/8",
    Teams:'U5 and U1',
    location:'Greenbay',
    Times:'1:00 a.m.' 
  },
  {
    month: 'October', 
    day: "10/20",
    Teams:'U6 and U3',
    location:'North',
    Times:'9:30 a.m.'
 },
  { month: 'October',
   day: "10/20",
   Teams:'U2 and U4',
   location:'Marjorie P Hart',
   Times:'1:00 a.m.' 
  },
  { month: 'October',
   day: "10/27",
   Teams:'U3 and U1',
   location:'AJ Katzenmaier P Hart',
   Times:'9:30 a.m.' 
  },
  { 
    month: 'October', 
    day: "10/27",
    Teams:'U5 and U6',
    location:'Howard A Yeager',
    Times:'1:00 a.m.' 
  }
]
        
      }
    }
  }
</script>

<style scoped>
.trasparencias
{

  opacity: 0.7;
  top:50px ;
}
</style>
