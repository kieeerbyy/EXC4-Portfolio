<template>
    <section class="team" id="team">
        <div class="team-box">
            <h2 class="heading">Team</h2>
            <div class="wrapper">
                <div class="team-item">
                    <img src="~/assets/anonymous.png/" alt="Descriptions">
                    <h2>Alyasa</h2>
                    <div class="rating">
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                    </div>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Saepe esse fugit modi similique, id aspernatur maxime dolorem enim suscipit impedit itaque ut quos qui, minus accusantium. Perferendis, aperiam. Molestias, mollitia!</p>
                </div>
                <div class="team-item">
                    <img src="~/assets/anonymous.png/" alt="Descriptions">
                    <h2>Anonymous</h2>
                    <div class="rating">
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                    </div>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Saepe esse fugit modi similique, id aspernatur maxime dolorem enim suscipit impedit itaque ut quos qui, minus accusantium. Perferendis, aperiam. Molestias, mollitia!</p>
                </div>

                <div class="team-item">
                    <img src="~/assets/anonymous.png/" alt="Descriptions">
                    <h2>Anonymous</h2>
                    <div class="rating">
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                        <i class='bx bxs-star' id="star"></i>
                    </div>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Saepe esse fugit modi similique, id aspernatur maxime dolorem enim suscipit impedit itaque ut quos qui, minus accusantium. Perferendis, aperiam. Molestias, mollitia!</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>

</script>

<style scoped>
.team{
    background: var(--bg-color);
}
.team-box{
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}
.team .heading{
    margin-bottom: 5rem;
}
.team-box img{
    width: 15rem;
    border-radius: 50%;
    border: 3px solid var(--main-color);
    box-shadow: 0 0 25px var(--main-color);
}
.wrapper{
    display: grid;
    grid-template-columns: repeat(3,1fr);
    gap: 3rem;
}
.team-item{
    min-height: 550px;
    max-width: 450px;
    background: rgba(0, 0, 0, 0.7);
    border: 3px solid rgba(238, 238, 238, 0.2);
    border-radius: 2rem;
    margin: 0 2rem;
    padding: 30px 60px;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1.5rem;
    color: white;
    transition: 0.4s ease-in-out;
}
.team-item:hover{
    border: 3px solid var(--main-color);
    transform: translateY(-10px)scale(1.03);
    box-shadow: 0 0 50px var(--main-color);
}
.team-item h2{
    font-size: 2.8rem;
}
.team p{
    font-size: 1.3rem;
    text-align: justify;
}
#star{
    color: gold;
    font-size: 2rem;
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