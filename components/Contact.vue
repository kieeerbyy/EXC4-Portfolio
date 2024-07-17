<template>
    <section class="contact" id="contact">
        <h2 class="heading">Contact<span> Me </span></h2>

        <form action="">
            <div class="input-group">
                <div class="input-box">
                    <input type="text" placeholder="Full Name">
                    <input type="email" placeholder="Email">
                </div>
                <div class="input-box">
                    <input type="number" placeholder="Phone Number">
                    <input type="text" placeholder="Subject">
                </div>
            </div>

            <div class="input-group-2">
                <textarea name="" id="" cols="30" rows="10" placeholder="Your Message"></textarea>
                <input type="submit" value="Send Message" class="btn">
            </div>
        </form>
    </section>
</template>

<script setup>

</script>

<style scoped>
.contact{
    background-color: var(--second-bg-color);
}
.contact h2{
    margin-bottom: 3rem;
}
.contact form{
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 3rem;
    margin: 5rem auto;
    text-align: center;
}
.contact form .input-box{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}
.contact form .input-box input, .contact form textarea{
    width: 100%;
    padding: 2.5rem;
    font-size: 1.8rem;
    color: var(--text-color);
    background: var(--bg-color);
    border-radius: 2rem;
    border: 2px solid var(--main-color);
    margin: 1.5rem 0;
    resize: none;
}
.contact form .btn{
    margin-top: 2rem;
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