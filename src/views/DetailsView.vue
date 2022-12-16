<template>
    <div class="main-box">  
        <div class="col1">
            <receipe />
            <ingredients  />
            <nutrition />
        </div>
        <div class="col2">
            <instructions />
        </div>                                
    </div>
</template>
<script>
import ingredients from '../components/Ingred.vue';
import nutrition from '../components/Nutrition.vue';
import instructions from '../components/Instructions.vue';
import receipe from '../components/Receip.vue';
export default{
    components:{
        ingredients,
        nutrition,
        instructions,
        receipe
    }
}

</script>
<style>
.main-box{
    min-height: 100%;
    width:100%;
    display: flex;
    background-image: url('https://images.pexels.com/photos/349610/pexels-photo-349610.jpeg');
    background-size: cover;
    justify-content:center;
    flex-wrap: wrap;
}


.main-box .col1{
    height: inherit;
    width:50%;
    display: flex;
    flex-direction: column;
    padding: 12px;
    flex-wrap: wrap;

}
.main-box .col2{
    height: inherit;
    width:50%;
    display: flex;
    flex-direction: column;
    padding: 12px;
    flex-wrap: wrap;

}

@media screen and (max-width: 600px) {
    .main-box{
        flex-direction: column;
    }
    .main-box .col1{
        width:100%;
        align-content: center;       
    }
    .main-box .col2{
        width: 100%;
        align-content: center;       
    }
}

</style>