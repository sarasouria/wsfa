<template>
    <div class="wrapper">
        <div class="prgrs">
            <div class="outer-circle">            
            </div>
            <div class="inner-circle">
                <img src="/assets/food-logo.png" alt="">
            </div>
        </div>
    </div>   
</template>

<style>
.wrapper{
    min-height: 100vh;
    width:100%;
    display: flex;
    justify-content: center;
    align-items: center;
}
.prgrs{
    width: 160px;
    height: 160px;
    position: relative;
}
.prgrs .outer-circle{
    width: 140px;
    height: 140px;
    border-radius: 50%;
    border: #FFD54F 1px solid;
    background-image: conic-gradient(#FFB300 0deg,#FFB300 45deg,#fff 45deg,#fff 180deg,#FFB300 180deg,#FFB300 225deg,#fff 225deg);
    position: absolute;
    top: 10px;
    left: 10px;
    animation: move 2s linear infinite;
}
.prgrs .inner-circle{
    width: 110px;
    height: 110px;
    border-radius: 50%;
    background-color: #fff;
    position: absolute;
    top: 25px;
    left: 25px;

}
.prgrs .inner-circle img{
    width: 110px;
    height: 110px;
    position: absolute;
}
@keyframes move {
    25%{
        transform: rotate(90deg);
    }
    50%{
        transform: rotate(180deg);
    }
    75%{
        transform: rotate(270deg);
    }
    100%{
        transform: rotate(360deg);
    }
}
</style>