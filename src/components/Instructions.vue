<template>
    <div class="instructions-wrapper">
        <prgrs v-if="loading" />
        <div class="instructions-title">
            Instructions
        </div>       
            <div v-for="(instruction,index) in instructions" :key="index">                
                <div class="instruction-name">
                    <h3>{{instruction.name}}</h3>
                </div>                              
                <ul v-for="(step,index) in instruction.steps" :key="index">                   
                    <li>
                        <h6>Step {{step.number}}</h6>
                        <p>{{step.step}}</p>
                    </li>
                </ul>                
            </div>        
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
            instructions:[]
        }
    },
    created()
    {
        this.loading=true;       
        axios.get(`https://api.spoonacular.com/recipes/${this.$route.params.id}/analyzedInstructions?apiKey=eb016ea8a1464ddd9e7f936d79762621`).then((response)=>{
                this.instructions=response.data;
            }).catch((error)=>{
                //alert(error)
            }).finally(()=>{
                this.loading=false;
            }); 
    }
}
</script>
<style>
.instructions-wrapper{
    background-color: #fff;
    width: 100%;
    height: fit-content;
    opacity: 0.8;
    padding: 12px;
    margin: 12px;
    border-radius: 5px;
}
.instructions-title{
    color: #757575;
    font-size: 36px;
    font-weight: bolder;
}
.instruction-name{
    padding: 12px;
    font-size: 24px;
    font-weight: bold;
}
</style>