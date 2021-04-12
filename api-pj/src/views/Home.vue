<template>
  <div class="home">
    <input v-model="address" type="text"/>
    <button @click="getAddress">住所自動入力</button>
    <p>Address :{{showAddress}}</p>
  </div>
</template>

<script>　
import axios from "axios";
export default{
  data(){
    return{
      address:"",
      showAddress:"",
      apikey:"eAAy5AF3PpWl4patSnxhGQFOoJg7JBFPVFrJBes",
    };
  },
  methods:{
    getAddress(){
      let url ="https://apis.postcode-jp.com/api/v3/postcodes/" +　this.address + "?apiKey=" + this.apikey;
      axios.get(url).then((ras) => {
         this.showAddress = ras.data.allAddress;
         });
　　　　}
    }
};
</script>

