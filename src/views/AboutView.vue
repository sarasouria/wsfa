<template>
  <div class="about">       
      <div class="about-box">
        <div class="image-box">
          <img src="/assets/chef.png" alt="">
        </div>
        <div class="text-box">
          <h1>Wasfa website</h1>
          <p>This website contains receipes from all over the world , insert dish's name in the search box above and get detailed information about the meal such as how to cook , ingredients and nutritions .</p>
        </div>        
      </div>          
  </div>
</template>

<style>
  .about {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    background-image: url('https://images.pexels.com/photos/349610/pexels-photo-349610.jpeg');
    background-size: cover;
  }
  .about-box{
    background-color: #fff;
    width: 600px;
    height: fit-content;
    border-radius: 8px;
    margin: 12px;
    display: flex;
  }
  .about-box p{
    font-size: 18px;
  }
  .about-box h1{
    font-size: 36px;
  }
.about .image-box img{
  width: 300px;
  height: fit-content;
  margin-left: -30px;
  object-fit: contain;
}
.about-box .text-box{
  padding: 24px;
  width: 70%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

@media screen and (max-width: 600px){
  .about-box{
    flex-direction: column;
  }
  .about-box .text-box{
    width:100%;
  }
  .about-box .image-box{
    display: flex;
    justify-content: center;
  }
  .about-box .image-box img{
    margin-left: 0;
  }

}

</style>
