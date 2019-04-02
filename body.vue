<template>
  <div class="body">
    
    <body-table>
    </body-table>
    
  </div>

</template>


<script>
import tabla from '../components/tabla.vue'

export default {
    name:'body',
    components:{
      'body-table': tabla
    },
    data(){
        return
        //
    }
}
</script>


<style scoped>
.body
{
  background-image: url("http://avante.biz/wp-content/uploads/Football-Soccer-Wallpapers/Football-Soccer-Wallpapers-010.jpg");
  background-size: 100%;
}
</style>
