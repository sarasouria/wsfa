<template>
    <div class="nutrition-wrapper">
        <prgrs v-if="loading" />
        <div class="nutrition-title">
            Nutrition
        </div>       
        <ul>
            <li>
                <strong> Calories : </strong>
                {{nutrition.calories}}
            </li>
            <li>
                <strong>Carbs : </strong>   : 
                {{nutrition.carbs}}
            </li>
            <li>
                <strong>Fat : </strong>     
                {{nutrition.fat}}
            </li>
            <li>
                <strong>Protein : </strong>      
                {{nutrition.protein}}
            </li>
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
            nutrition:{},
            loading:false
        }
    },
    created()
    {
        this.loading=true;       
        axios.get(`https://api.spoonacular.com/recipes/${this.$route.params.id}/nutritionWidget.json?apiKey=eb016ea8a1464ddd9e7f936d79762621`).then((response)=>{
                this.nutrition=response.data;
            }).catch((error)=>{
               // alert(error)
            }).finally(()=>{
                this.loading=false;
            }); 
    }
}
</script>
<style>
.nutrition-wrapper{
    background-color: #fff;
    width: 100%;
    height: fit-content;
    opacity: 0.8;
    padding: 12px;
    margin: 12px;
    border-radius: 5px;
}
.nutrition-title{
    color: #757575;
    font-size: 36px;
    font-weight: bolder;
}
</style>