<script>
    export default{
    data()
    {
        return{
            searchForm:{
                query:''
            }
        }
    },
    methods:{
        search()
        {
            this.$router.push({ name: 'result', params: { query: this.searchForm.query } });            
        }
    }
    }
    
</script>

<template>
    <section class="header">       
        <div class="welcome-msg">
            <img src="/assets/smoke.png" alt="" class="smoke">
            <img src="/assets/smoke.png" alt="" class="smoke2">
            <h1>Wasfa</h1>
            <p>This website contains recipes from all over the world , insert dish's name in the search box below and get detailed information about the meal such as how to cook , ingredients and nutritions .</p>                            
            
            <form v-on:submit.prevent="search">
              <input type="text" id="search-input" placeholder="Type meal name ..." v-model="searchForm.query">
              <input type="submit" value="Search" id="search-btn">
            </form>
        </div>
        
    </section>
    <section class="about-us">
        <div class="who-we-are">
            <h1>About us</h1>
            <p>This website contains receipes from all over the world , insert dish's name in the serch box above and get detailed information about the meal such as how to cook , ingredients and nutritions .</p>
        </div>
        <div class="picture">
            <img src="/assets/cooker.png" alt="">
        </div>
    </section>
    <footer>
        <div class="links">
            <a href="/#">
                <svg xmlns="http://www.w3.org/2000/svg" width="64" height="64" fill="#fff" class="bi bi-facebook" viewBox="0 0 16 16">
                    <path d="M16 8.049c0-4.446-3.582-8.05-8-8.05C3.58 0-.002 3.603-.002 8.05c0 4.017 2.926 7.347 6.75 7.951v-5.625h-2.03V8.05H6.75V6.275c0-2.017 1.195-3.131 3.022-3.131.876 0 1.791.157 1.791.157v1.98h-1.009c-.993 0-1.303.621-1.303 1.258v1.51h2.218l-.354 2.326H9.25V16c3.824-.604 6.75-3.934 6.75-7.951z"/>
                </svg></a>
            <a href="/#">
                <svg xmlns="http://www.w3.org/2000/svg" width="64" height="64" fill="#fff" class="bi bi-instagram" viewBox="0 0 16 16">
                    <path d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.917 3.917 0 0 0-1.417.923A3.927 3.927 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.916 3.916 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.926 3.926 0 0 0-.923-1.417A3.911 3.911 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0h.003zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599.28.28.453.546.598.92.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.47 2.47 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.478 2.478 0 0 1-.92-.598 2.48 2.48 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233 0-2.136.008-2.388.046-3.231.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92.28-.28.546-.453.92-.598.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045v.002zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92zm-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217zm0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334z"/>
                  </svg>
            </a>
            <a href="/#">
                <svg xmlns="http://www.w3.org/2000/svg" width="64" height="64" fill="#fff" class="bi bi-whatsapp" viewBox="0 0 16 16">
                    <path d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"/>
                  </svg>
            </a>
        </div>
        <div class="rights">
            Developed by Eng. Zein Khalil .
        </div>
    </footer>

</template>
<style scoped>
.header{
    min-height: 100vh;
    display: flex;
    background-image: url("https://images.pexels.com/photos/887827/pexels-photo-887827.jpeg?auto=compress&cs=tinysrgb");
    background-size: cover;   
    position: relative;
}
.header .welcome-msg{
    width: 600px;
    height:fit-content;
    color: #fff;
    padding: 48px;  
    background-color: #FF5722;  
    margin-top: 10vh;
    margin-left: 5vw;    
    border-bottom-right-radius: 48px;
    opacity: 0.9;
    border-bottom-left-radius: 48px;

}
form{
  display: flex;
}
.header .welcome-msg input{
    font-size: 18px;
    padding: 8px;
    border-width: 1px;
    border-color: #fff;
    border-style: solid;
}
#search-input{   
    border-radius: 5px 0 0 5px;
}
#search-btn{
    background-color:#FF3D00 ;    
    color: #fff;    
    border-radius: 0 5px 5px 0;
    cursor: pointer;
}
.header .welcome-msg h1{
    font-size: 102px;   
}
.header .welcome-msg .smoke,.smoke2{
    width: 300px;
    height: 200px;
    margin:0 0 0 5vw;
    position: absolute;

    top: -30px;
    left: 0;

    animation: smoke 2s linear infinite;
}
.smoke2{
    animation: smoke 2s linear infinite;
    animation-delay: 1s;
}
.about-us{
    background-color: cornflowerblue;
}
.header .welcome-msg p{
    margin-bottom: 2rem;
}
#search-btn:hover{
    background-color:#FF8A65 ;
}
@keyframes smoke {
    0%{
        filter: blur(0);
        opacity: 0;
        transform: translateY(-10px);
    }
    25%{
        filter: blur(3px);
        opacity: 0.5;
        transform: translateY(-20px);
    }
    50%{
        filter: blur(5px);
        opacity: 1;
        transform: translateY(-30px);
    }
    75%{
        filter: blur(3px);
        opacity: 0.5;
        transform: translateY(-40px);
    }
    100%{
        filter: blur(0);
        opacity: 0;
        transform: translateY(-50px);
    }
}
.about-us{
    display: flex;
    height: 100vh;
}
.about-us .who-we-are{
    width: 50%;
    height: inherit;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    color: #fff;
    font-size: 18px;
    padding: 48px;
}
.about-us .who-we-are p{
    padding: 24px;
}
.about-us .picture{
    width: 50%;
    height: inherit;
    animation: appereance 2s linear;
    transition: all 1s ease;
}
.about-us .picture img{
    width: 100%;
    height: 100%;
}
footer{
    display: flex;
    flex-direction: column;
    height: 30vh;

}
footer .links{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20vw;
    height: 20vh;
    width: 100%;
    background-color: #424242;
}
footer .rights{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 10vh;
    width: 100%;
    background-color: #212121;
    color: #fff;
}
@keyframes appereance {
    25%{
        transform: translateX(75px);
    }
    50%{
        transform: translateX(50px);
    }
    75%{
        transform: translateX(25px);
    }
    100%{
        transform: translateX(0);
    }
}
@media screen and (max-width: 600px){
    .header{
        display:flex;
        justify-content: center;        
        padding: 5vw;
    }
    .header .welcome-msg{       
        display:flex;
        flex-direction: column;
        flex-wrap: wrap;
        padding:5vw;
        justify-content: center;
        text-align: center;
        margin:0;

    }
    .about-us{
        flex-direction: column;
        flex-wrap: wrap;
        height: fit-content;
        padding: 5vw;
    }
    .about-us .who-we-are{
        width: 100%;
    }
    .about-us .picture{
        width: 100%;
    }

}

</style>
