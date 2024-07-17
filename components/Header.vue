<template>
    <header class="header">
      <a href="#home" class="logo">Alyasa <span>Sumo</span></a>
      <i class='bx bx-menu' id="menu-icon" @click="toggleMenu"></i>
      <nav class="navbar" :class="{ 'is-open': isMenuOpen }">
        <a href="#home" class="active">Home</a>
        <a href="#education">Education</a>
        <a href="#services">Services</a>
        <a href="#team">Team</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>
  </template>
  
  <script setup>
import { onMounted } from 'vue'

onMounted(() => {
  const menuIcon = document.querySelector('#menu-icon')
  const navbar = document.querySelector('.navbar')
  const sections = document.querySelectorAll('section')
  const navLinks = document.querySelectorAll('header nav a')

  window.onscroll = () => {
    sections.forEach(sec => {
      const top = window.scrollY
      const offset = sec.offsetTop - 150
      const height = sec.offsetHeight
      const id = sec.getAttribute('id')

      if (top >= offset && top < offset + height) {
        navLinks.forEach(link => {
          link.classList.remove('active')
          document.querySelector(`header nav a[href*=${id}]`).classList.add('active')
        })
      }
    })
  }

  menuIcon.onclick = () => {
    menuIcon.classList.toggle('bx-x')
    navbar.classList.toggle('active')
  }
})
</script>
  
  <style scoped>
  .header{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 4rem 12% 4rem;
    background: rgba(0, 0, 0, 0.3);
    backdrop-filter: blur(10px);
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 5;
}
.logo {
    font-size: 3rem;
    color: var(--text-color);
    font-weight: 800;
    cursor: pointer;
    transition: 0.3s ease;
}
.logo:hover{
    transform: scale(1.1);
}
.logo span{
    text-shadow: 0 0 25px var(--main-color);
    color: var(--main-color);
}
.navbar a{
    font-size: 1.8rem;
    color: var(--text-color);
    margin-left: 4rem;
    font-weight: 500;
    transition: 0.3s ease;
    border-bottom: 3px solid transparent;
}
.navbar a:hover,
.navbar a.active{
    color: var(--main-color);
    border-bottom: 3px solid var(--main-color);
}
#menu-icon{
    font-size: 3.6rem;
    color: var(--main-color);
    display: none;
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
  