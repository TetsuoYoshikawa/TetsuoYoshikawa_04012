<template>
  <div class="home">
    <input v-model="address" type="text"/>
    <button @click="getAddress">住所自動入力</button>
    <p>Address :{{showAddress}}</p>
  </div>
</template>

<script>
export default{
  data(){
    return{
      address:"",
      showAddress:""
    };
  },
  methods:{
    getAddress(){
      const item = await aixos.get('https://apis.postcode-is.com/api/v3/postcodes?postcode=${this.address} eAAy5AF3PpWl4patSnxhGQFOoJg7JBFPVFrJBes);
      const addressData = item.data;
      this.showAddress = allAddress;
  }
};
</script>
