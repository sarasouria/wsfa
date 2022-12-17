<template>
  <div class="about">       
      <div class="about-box">
        <div class="image-box">
          <img src="/assets/chef.png" alt="">
        </div>
        <div class="text-box">
          <h1>Wasfa website</h1>
          <p>This website contains recipes from all over the world , insert dish's name in the search box above and get detailed information about the meal such as how to cook , ingredients and nutritions .</p>
        </div>        
      </div>          
  </div>
</template>

<style>
.about{
  min-height: 100vh;
  width:100%;
  display: flex;
  justify-content: center;

  background-image: url('https://images.pexels.com/photos/349610/pexels-photo-349610.jpeg');
  background-size: cover;

  padding: 12px;

}
.about-box{
  display: flex;
  width: 50%;
  height:fit-content;
  background: #fff;
  border-radius: 8px;
  margin-top: 12px;

}
.about-box .image-box{
  width: 40%;
  height: fit-content;
  margin-left: -30px;
}
.about-box .image-box img{
  width:100%;
 
}
.about-box .text-box{
  display: flex;
  flex-direction: column;
  width:60%;
  height:100%;
  padding: 16px;
  align-self: center;
}
@media screen and (max-width: 600px){
  .about-box{
    width:100%;
    flex-direction: column;
  }
  .about-box .image-box{
    width:100%;
    margin-left: 0;

  }
  .about-box .image-box img{
    object-fit: contain;   
  }
  .about-box .text-box{
    width:100%;
  }
}
</style>
