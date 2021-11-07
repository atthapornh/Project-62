<template>
  <div>
    <b-container class="bv-example-row">
    <b-row class="text-left">
         <b-col></b-col>

         <b-col cols="10" class="bg1">
    <h1>รายระเอียดร้าน</h1>
  <!--   <p><button v-on:click="logout">Logout</button></p> -->
   <br><br><img src="@/assets/tum1.jpg"><br><br>

    
    </b-col>
      <b-col> </b-col>
     </b-row>
</b-container>
  </div>
</template>
<script>

import RoomService from "@/services/RoomsService";
export default {
  data() {
    return {
      rooms: [],
    };
  },
  async created() {
    this.rooms = (await RoomService.index()).data;
  }
};
</script>
<style scoped>
</style>