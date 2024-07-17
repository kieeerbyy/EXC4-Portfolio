<template>
    <section class="services" id="services">
        <h2 class="heading">Services</h2>

        <div class="services-container">
            <div class="service-box">
                <div class="service-info">
                    <h4>UI Design</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Et reprehenderit facilis labore doloremque nam dolore ratione cumque delectus voluptatibus quod? Numquam at totam recusandae eum veniam quasi a amet iure.</p>
                </div>
            </div>

            <div class="service-box">
                <div class="service-info">
                    <h4>Frontend Development</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Et reprehenderit facilis labore doloremque nam dolore ratione cumque delectus voluptatibus quod? Numquam at totam recusandae eum veniam quasi a amet iure.</p>
                </div>
            </div>

            <div class="service-box">
                <div class="service-info">
                    <h4>Backend Development</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Et reprehenderit facilis labore doloremque nam dolore ratione cumque delectus voluptatibus quod? Numquam at totam recusandae eum veniam quasi a amet iure.</p>
                </div>
            </div>

            <div class="service-box">
                <div class="service-info">
                    <h4>Software Engineer</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Et reprehenderit facilis labore doloremque nam dolore ratione cumque delectus voluptatibus quod? Numquam at totam recusandae eum veniam quasi a amet iure.</p>
                </div>
            </div>

        </div>
    </section>
</template>

<script setup>

</script>

<style scoped>
.services{
    background: var(--bg-color);
    color: black;
}
.services h2{
    margin-bottom: 5rem;
    color: white;
}
.services-container{
    display: grid;
    grid-template-columns: repeat(2,1fr);
    align-items: center;
    gap: 2.5rem;
}
.service-box{
    background-color: var(--main-color);
    height: 300px;
    border-radius: 3rem;
    border: 5px solid transparent;
    cursor: pointer;
    transition: 0.4s ease-in-out;
}
.service-box:hover{
    background: white;
    color: black;
    border: 5px solid var(--main-color);
    transform: scale(1.03);
}
.service-box .service-info{
    display: flex;
    flex-direction: column;
    text-align: left;
    max-height: 200px;
    justify-content: left;
    align-items: baseline;
    padding: 5rem 5rem;
}
.service-info h4{
    font-size: 3rem;
    font-weight: 800;
    line-height: 2;
}
.service-info p{
    font-size: 1.6rem;
    font-weight: 600;
    max-height: 100px;
    line-height: 1.7;
    margin: auto;
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