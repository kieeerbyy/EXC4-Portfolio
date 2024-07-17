<template>
    <section class="home" id="home">
      <div class="home-content">
        <h1>Hi, It's <span>Alyasa</span></h1>
        <h3 class="text-animation">I'm a <span></span></h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum dolorem accusamus dolores, aspernatur optio sequi quo exercitationem commodi tenetur mollitia quisquam voluptas veniam consectetur earum! Voluptas explicabo possimus assumenda cupiditate.</p>
  
        <div class="social-icons">
          <a href="#"><i class='bx bxl-linkedin'></i></a>
          <a href="#"><i class='bx bxl-github'></i></a>
          <a href="#"><i class='bx bxl-instagram-alt'></i></a>
          <a href="#"><i class='bx bxl-twitter'></i></a>
        </div>
  
        <div class="btn-group">
          <a href="#" class="btn">Hire</a>
          <a href="#contact" class="btn">Contact</a>
        </div>
      </div>
      <div class="home-img">
        <img src="~/assets/image.jpeg/" alt="Descriptions">
      </div>
    </section>
  </template>
  
  <script setup>


  </script>
  
  <style scoped>
.home {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 15rem;
}
.home-content{
    display: flex;
    flex-direction: column;
    align-items: baseline;
    text-align: left;
    justify-content: center;
    margin-top: 3rem;
}
span{
    color: var(--main-color);
}
.logo span{
    color: var(--main-color);
}
.home-content h3{
    margin-bottom: 2rem;
    margin-top: 1rem;
    font-size: 3.5rem;
}
.home-content h1{
    font-size: 7rem;
    font-weight: 700;
    margin-top: 1.5rem;
    line-height: 1;
}
.home-img{
    border-radius: 50%;
}
.home-img img{
    position: relative;
    top: 3rem;
    width: 32vw;
    border-radius: 50%;
    box-shadow: 0 0 25px var(--main-color);
    cursor: pointer;
    transition: 0.4s ease-in-out;
}
.home-img img:hover{
    box-shadow: 0 0 25px var(--main-color),
                0 0 50px var(--main-color),
                0 0 100px var(--main-color);
}
.home-content p {
    font-size: 1.5rem;
    font-weight: 500;
    line-height: 1.8;
    max-width: 1000px;
}
.social-icons a{
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 4.5rem;
    height: 4.5rem;
    background: transparent;
    border: 2px solid var(--main-color);
    font-size: 2.5rem;
    border-radius: 50%;
    color: var(--main-color);
    margin: 3rem 1.5rem 3rem 0;
    transition: 0.3s ease-in-out;
}
.social-icons a:hover{
    color: var(--text-color);
    transform: scale(1.3)translateY(-5px);
    box-shadow: 0 0 25px var(--main-color);
    background-color: var(--main-color);
}
.btn{
    display: inline-block;
    padding: 1rem 2.8rem;
    background: var(--main-color);
    box-shadow: 0 0 25px var(--main-color);
    border-radius: 4rem;
    font-size: 1.6rem;
    color: black;
    border: 2px solid transparent;
    letter-spacing: 0.1rem;
    font-weight: 600;
    transition: 0.3s ease-in-out;
    cursor: pointer;
}
.btn:hover{
    transform: scale(1.05);
    box-shadow: 0 0 50px var(--main-color);
}
.btn-group{
    display: flex;
    align-items: center;
    gap: 1.5rem;
}
.btn-group a:nth-of-type(2){
    background-color: black;
    color: var(--main-color);
    border: 2px solid var(--main-color);
    box-shadow: 0 0 25px transparent;
}
.btn-group a:nth-of-type(2):hover{
    box-shadow: 0 0 25px var(--main-color);
    background-color: var(--main-color);
    color: black;
}
.text-animation{
    font-size: 34px;
    font-weight: 600;
    min-width: 280px;
}
.text-animation span{
    position: relative;
}
.text-animation span::before{
    content: "Web Developer";
    color: var(--main-color);
    animation: words 20s infinite;
}
.text-animation span::after{
    content: "";
    background-color: var(--bg-color);
    position: absolute;
    width: calc(100% + 8px);
    height: 100%;
    border-left: 3px solid var(--bg-color);
    right: -8px;
    animation: cursor 0.6s infinite, typing 20s steps(14) infinite;
}

@keyframes cursor{
    to{
        border-left: 2px solid var(--main-color);
    }
}
@keyframes words{
    0%,
    20%{
        content: "Frontend Designer";
    }
    21%,
    40%{
        content: "Web Designer";
    }
    41%,
    60%{
        content: "UI / UX Designer";
    }
    61%,
    80%{
        content: "Web Developer";
    }
    81%,
    100%{
        content: "Software Engineer";
    }
}
@keyframes typing{
    10%,
    15%,
    30%,
    35%,
    50%,
    55%,
    70%,
    75%,
    90%,
    95%{
        width: 0;
    }
    5%,
    20%,
    25%,
    40%,
    45%,
    60%,
    65%,
    80%,
    85%{
        width: calc(100% + 8px);
    }
}
.heading{
    font-size: 8rem;
    text-align: center;
    margin: 5rem 0;
}
@media(max-width:1285px){
    html{
        font-size: 55%;
    }
    .services-container{
        padding-bottom: 7rem;
        grid-template-columns: repeat(2,1fr);
        margin: 0 5rem;
    }
}
@media(max-width:991px){
    header{
        padding: 2rem 3%;
    }
    section{
        padding: 10rem 3% 2rem;
    }
    .timeline-items::before{
        left: 7px;
    }
    .timeline-item:nth-child(odd){
        padding-right: 0;
        text-align: left;
    }
    .timeline-item:nth-child(odd), .timeline-item:nth-child(even){
        padding-left: 37px;
    }
    .timeline-dot{
        left: 0;
    }
    .services{
        padding-bottom: 7rem;
    }
    .team .wrapper{
        grid-template-columns: repeat(1,1fr);
    }
    .contact form{
        flex-direction: column;
    }
    .footer{
        padding: 2rem 3%;
    }
}

@media(max-width:895px){
    #menu-icon{
        display: block;
        z-index: 999;
        cursor: pointer;
    }
    #menu-icon i.active:before{
        content: "\f00d";
    }
    .navbar{
        position: fixed;
        height: 100vh;
        top: 0;
        left: -100%;
        width: 100%;
        padding-top: 80px;
        background: rgb(0, 0, 0);
        backdrop-filter: blur(200px);
        transition: all 0.3s ease;
    }
    .navbar.active{
        left: 0;
    }
    .navbar a{
        display: block;
        color: #fff;
        font-size: 18px;
        font-weight: 500;
        margin-left: 25px;
        transition: color 0.3s ease;
        align-items: center;
    }
    .home{
        flex-direction: column-reverse;
        margin: 5rem 4rem;
    }
    .home-content h3{
        font-size: 2.6rem;
    }
    .home-content h1{
        font-size: 8rem;
        margin-top: 3rem;
    }
    .home-content p{
        max-width: 600px;
        margin: 0 auto;
    }
    .home-img img{
        width: 56vw;
    }
    .services h2{
        margin-bottom: 3rem;
    }
    .services-container{
        grid-template-columns: repeat(1,1fr);
    }
}
  </style>
  