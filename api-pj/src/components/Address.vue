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
      const item = await aixos.get('https://apis.post code-is.com/api/v3/post codes?postcode=${this.address});
      const addressData = item.data;
      this.showAddress = allAddress;
  }
};
</script>
