<template>
    <div class="receipe-wrapper">
        <prgrs v-if="loading" />
        <img :src="receipe.url" alt="">
    </div>
</template>
<script>
import prgrs from './Prgrs.vue';
import axios from 'axios';
export default{
    components:{
        prgrs
    },
    props:{
        id:0
    },
    data()
    {
        return{
            loading:false,
            receipe:{}
        }
    },
    created()
    {
        this.loading=true;       
        axios.get(`https://api.spoonacular.com/recipes/${this.$route.params.id}/card?apiKey=eb016ea8a1464ddd9e7f936d79762621`).then((response)=>{
                this.receipe=response.data;
            }).catch((error)=>{
                //alert(error)
            }).finally(()=>{
                this.loading=false;
            }); 
    }
}
</script>
<style>
.receipe-wrapper{
    background-color: #fff;
    width: 100%;
    height: fit-content;
    margin: 12px;
    border-radius: 5px;
}
.receipe-wrapper img{
    width:inherit;
   
    object-fit: contain;
}
</style>