<template>
    <footer class="footer">
        <div class="social">
            <a href="#"><i class='bx bxl-linkedin'></i></a>
                <a href="#"><i class='bx bxl-github' ></i></a>
                <a href="#"><i class='bx bxl-instagram-alt' ></i></a>
                <a href="#"><i class='bx bxl-twitter'></i></a>
        </div>

        <ul class="list">
            <li><a href="#home">FAQ</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#education">About Me</a></li>
            <li><a href="#contact">Contact</a></li>
            <li><a href="#team">Team</a></li>
        </ul>
        <p class="copyright">
            © Alyasa Sumo | All Rights Reserved 2024
        </p>
    </footer>
</template>

<script setup>

</script>

<style scoped>
.footer{
    position: relative;
    bottom: 0;
    width: 100%;
    padding: 40px 0;
    background-color: var(--bg-color);
}
.footer .social{
    text-align: center;
    padding-bottom: 25px;
    color: var(--main-color);
}
.footer .social a{
    font-size: 25px;
    color: var(--main-color);
    border: 2px solid var(--main-color);
    width: 42px;
    height: 42px;
    line-height: 42px;
    display: inline-block;
    text-align: center;
    border-radius: 50%;
    margin: 0 10px;
    transition: 0.3s ease-in-out;
}
.footer .social a:hover{
    transform: scale(1.2)translateY(-10px);
    background-color: var(--main-color);
    color: black;
    box-shadow: 0 0 25px var(--main-color);
}
.footer ul{
    margin-top: 0;
    padding: 0;
    font-size: 18px;
    line-height: 1.6;
    margin-bottom: 0;
    text-align: center;
}
.footer ul li a{
    color: white;
    border-bottom: 3px solid transparent;
    transition: 0.3s ease-in-out;
}
.footer ul li a:hover{
    border-bottom: 3px solid var(--main-color);
}
.footer ul li{
    display: inline-block;
    padding: 0 15px;
}
.footer .copyright{
    margin-top: 50px;
    text-align: center;
    font-size: 16px;
    color: white;
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