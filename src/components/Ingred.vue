<template>
    <div class="ingred-wrapper">
        <prgrs v-if="loading" />
        <div class="ingred-title">
            Ingredients
        </div>
        <ul>
            <div v-for="(ingredient,index) in ingredients" :key="index">
                <li>
                    <strong>{{ingredient.name}}</strong>
                     {{ingredient.amount.metric.value}} 
                     {{ingredient.amount.metric.unit}}
                </li>    
            </div>
        </ul>
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
            ingredients:[],
            loading:false
        }        
    },
    created()
    {
        this.loading=true;       
        axios.get(`https://api.spoonacular.com/recipes/${this.$route.params.id}/ingredientWidget.json?apiKey=eb016ea8a1464ddd9e7f936d79762621`).then((response)=>{
                this.ingredients=response.data.ingredients;
            }).catch((error)=>{
               // alert(error)
            }).finally(()=>{
                this.loading=false;
            }); 
        
    }
}
</script>
<style>
.ingred-wrapper{
    width: 100%;
    height: fit-content;
    background: #fff;
    opacity: 0.8;
    padding: 12px;
    margin: 12px;
    border-radius: 5px;

}
.ingred-title{
    color: #757575;
    font-size: 36px;
    font-weight: bolder;
}
</style>