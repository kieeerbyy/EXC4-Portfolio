<template>
    <section class="education" id="education">
      <h2 class="heading">Education</h2>
  
      <div class="timeline-items">
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2021</div>
          <div class="timeline-content">
            <h3>High School</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima delectus numquam, quos maxime itaque accusamus possimus provident recusandae nulla eveniet!</p>
          </div>
        </div>
  
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2022</div>
          <div class="timeline-content">
            <h3>University</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima delectus numquam, quos maxime itaque accusamus possimus provident recusandae nulla eveniet!</p>
          </div>
        </div>
  
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2023</div>
          <div class="timeline-content">
            <h3>Internship</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima delectus numquam, quos maxime itaque accusamus possimus provident recusandae nulla eveniet!</p>
          </div>
        </div>
  
        <div class="timeline-item">
          <div class="timeline-dot"></div>
          <div class="timeline-date">2024</div>
          <div class="timeline-content">
            <h3>Job 1</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima delectus numquam, quos maxime itaque accusamus possimus provident recusandae nulla eveniet!</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>

  </script>
  
  <style scoped>
.heading{
    font-size: 8rem;
    text-align: center;
    margin: 5rem 0;
}
.education{
    padding: 100px 15px;
    background: var(--second-bg-color);
}
.education h2{
    margin-bottom: 5rem;
}
.timeline-items{
    max-width: 1200px;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    position: relative;
}
.timeline-items::before{
    content: "";
    position: absolute;
    width: 5px;
    height: 100%;
    background-color: var(--main-color);
    left: calc(50% - 1px);
}
.timeline-item{
    margin-bottom: 40px;
    width: 100%;
    position: relative;
}
.timeline-item:last-child{
    margin-bottom: 0;
}
.timeline-item:nth-child(odd){
    padding-right: calc(50% + 30px);
    text-align: right;
}
.timeline-item:nth-child(even){
    padding-left: calc(50% + 30px);
}
.timeline-dot{
    height: 21px;
    width: 21px;
    background-color: var(--main-color);
    box-shadow: 0 0 25px var(--main-color),
                0 0 50px var(--main-color);
    position: absolute;
    left: calc(50% - 8px);
    border-radius: 50%;
    top: 10px;
}
.timeline-date{
    font-size: 20px;
    font-weight: 800;
    color: white;
    margin: 6px 0 15px;
}
.timeline-content{
    background-color: var(--bg-color);
    border: 3px solid var(--main-color);
    padding: 30px 50px;
    border-radius: 4rem;
    box-shadow: 0 0 10px var(--main-color);
    cursor: pointer;
    transition: 0.3s ease-in-out;
}
.timeline-content:hover{
    transform: scale(1.05);
    box-shadow: 0 0 25px var(--main-color);
}
.timeline-content h3{
    font-size: 20px;
    color: white;
    margin: 0 0 10px;
    font-weight: 500;
}
.timeline-content p{
    color: white;
    font-size: 16px;
    font-weight: 300;
    line-height: 22px;
}

::-webkit-scrollbar{
    width: 15px;
}
::-webkit-scrollbar-thumb{
    background-color: var(--main-color);
}
::-webkit-scrollbar-track{
    background-color: var(--bg-color);
    width: 50px;
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
  