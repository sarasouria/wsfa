<template>  
<div class="result-wrapper">
    <prgrs class="col-12" v-if="loading"  />
    <div class="container">       
        <div class="row justify-content-center p-3">           
            <div class="col-xl-4 col-md-6 col-sm-12" v-for="(result,index) in results" :key="index">
                 <meal :meal="result" @click="getInfo(result.id)"/>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import axios from 'axios';
import prgrs from '../components/Prgrs.vue';
import meal from '../components/Meal.vue';
export default ({
    
    components:{
        prgrs,
        meal
    },
    data(){
        return{
            results:[],
            loading:false
        }
    },    
    created()
    {
        this.loading=true;       
        axios.get(`https://api.spoonacular.com/recipes/complexSearch?query=${this.$route.params.query}&apiKey=eb016ea8a1464ddd9e7f936d79762621`).then((response)=>{
                this.results=response.data.results;
            }).catch((error)=>{
               // alert(error)
            }).finally(()=>{
                this.loading=false;
            });            
    },
    methods:{
        getInfo(meal_id)
        {
            this.$router.push({name:"details",params:{id:meal_id}});
        }
    }
})
</script>
<style>
.result-wrapper{
    
    background-image: url('https://images.pexels.com/photos/349610/pexels-photo-349610.jpeg');
    background-size: cover;
    min-height: 100vh;
    width: 100%;
}
</style>