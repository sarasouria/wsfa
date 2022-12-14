<template>
<div class="meal">
    <img :src="meal.image" :alt="meal.title">
    <div class="meal-name">
        {{meal.title}}
    </div>
</div>

</template>
<script>

export default ({
    props:{
        meal:{
            title:String,
            image:String,
            id:Number
        }
    }
})
</script>
<style>
.meal{
    width: calc(100% - 50px);
    height: fit-content;
    background-color: #FFB300;
    color: #fff;
    display: flex;
    align-items: center;
    margin: 24px;
    border-radius: 5px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    transform: translateX(50px);
    transition: all 2s ease linear;
}
.meal:hover{
    cursor: pointer;
    background-color: #EF6C00;
}
.meal img{

    width: 100px;
    height: 100px;
    border-radius: 50%;
    border: #fff 2px solid;
    margin-left: -50px;
}
.meal .meal-name{
    padding: 12px;
}
</style>