<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Portafolio</title>
    
    <link rel="stylesheet" href="https://unpkg.com/aos@next/dist/aos.css" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>

    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600&display=swap');
        *{
    
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
    text-decoration: none;
    scroll-behavior: smooth;
    }
    
    body{
    width: 100%;
    height: auto;
    background-color: black;
    overflow-x: hidden;
    }
    
    /*Custom scroll bar CSS */
    
    ::-webkit-scrollbar{
    width: 10px;
    }
    
    ::-webkit-scrollbar-track{
    background: #f1f1f1;
    }
    
    ::-webkit-scrollbar-thumb{ 
    background: #b74b4b;
    border-radius: 12px;
    transition: all 0.3 ease;
    }
    
    ::-webkit-scrollbar-thumb:hover{
    background: #b74b4b;
    }
    
    /*navbar styling*/
    nav{
        width: 100%;
        height: 10vh;
        
        }
        
        .nav-container{
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: space-around;
        align-items: center;
        }
        
        .logo{
        color: white;
        font-size: 2rem;
        font-weight: bold;
        }
    
        .logo span{
        color: #b74b4b;
        text-shadow: 0 0 10px #b74b4b;
        }
        .hamburg,
        .cancel{
        cursor: pointer;
        position: absolute;
        right: 15px;
        top: 10px;
        color: white;
        opacity: 0;
        pointer-events: none ;
        font-size: clamp(2.5rem, 0.5rem + 5vw, 3rem);
        }
        .nav-container .links{
        display: flex;
        }
        
        .nav-container .links a{
        position: relative;
        font-size: 1.2rem;
        color: white;
        margin: 0 20px;
        text-decoration: none;
        font-weight: 550;
        transition: 0.3s linear;
        }
        
        .nav-container .links a::before{
        position: absolute;
        content: "";
        bottom: -3px;
        left: 0;
        width: 0%;
        height: 3px;
        background-color: #b74b4b;
        transition: 0.2s linear;
        }
        
        .nav-container .links a:hover::before{
        width: 100%;
        }
        
        .nav-container .links a:hover{
        color: #b74b4b;
        }
        
        .dropdown{
        z-index: 100;
        position: absolute;
        top: 0;
        transform: translateY(-500px);
        width: 100%;
        height: auto;
        backdrop-filter: blur(4px) brightness(40%);
        box-shadow:  0 0 20px black;
        transition: 0.2s linear;
        }
        
        .dropdown .links a{
        display: flex;
        color: white;
        text-decoration: none;
        justify-content: center;
        padding: 15px 0;
        align-items: center;
        transition: 0.2s linear;
        }
        
        .dropdown .links a:hover{
        background-color: #b74b4b;
        }
        
        section{
        width: 100%;
        min-width: 90vh;
        }
    
        section .main-container{
         display: flex;
         justify-content: space-evenly;
         padding-left: 100px;
         align-items: center;
        
     }
        .main-container .image{
         width: 500px;
         height: 80vh;
         border-radius: 100%;
         overflow: hidden;
         box-shadow: 0 0 50px #b74b4b;
        }
        
        .main-container .image img{
         width: 100%;
        }
        
        .main-container .image:hover{
         animation: animate 1.5s ease-in-out infinite;
        }
        
        @keyframes animate {
        0%{
               scale: 1;
        }
    
        50%{
             scale: 1.05;
        }
    
        100%{
              scale: 1;
        }
        }
        
        .main-container .content{
        color: white;
        width: 40%;
        
        }
        .content h1{
        font-size: clamp(1rem, 1rem + 5vw, 1.8rem);
        }
    
        .content h1 span{
        color: #b74b4b;
        text-shadow: 0  0 10px #b74b4b;
        }
    
        .content .typewriter{
        font-size: clamp(1rem, 1rem + 5vw, 2.5rem);
        font-weight: 600;
        }
    
        .content .typewriter-text{
        color: #b74b4b;
        text-shadow: 0 0 10px #b74b4b;
        }
    
        .content p{
        font-size: clamp(0.4rem , 0.2rem + 9vw, 1rem);
        margin: 10px 0;
        }
    
        .social-links i{
        display: inline-flex;
        justify-content: center;
        align-items: center;
        width: 3rem;
        height: 3rem;
        background-color: transparent;
        border: 0.2rem solid #b74b4b;
        border-radius: 50%;
        color: #b74b4b;
        margin: 5px 15px;
        font-size: 1.5rem;
        transition: 0.2s linear;
        }
    
        .social-links i:hover{
        scale: 1.3;
        color: black;
        background-color: #b74b4b;
        filter: drop-shadow(0 0 10px #b74b4b);
        }
    
        .content button{
        width: 50%;
        height: 6vh;
        margin: 30px;
        background-color: #b74b4b;
        color: white;
        border: none;
        outline: none;
        font-size: 120%;
        font-weight: 700;
        border-radius: 5px;
        transition: 0.2s linear;
        }
    
        .content button:hover{
        scale: 1.1;
        color: #b74b4b;
        border: 2px solid #b74b4b;
        background-color: transparent;
        font-weight: 700;
        box-shadow: 0 0 40px #b74b4b;
        }
        
        /*About Section style*/
       
        section.content{
         width: 80%; 
         margin: 0px auto;
         font-family: 'Poppins', sans-serif;
        
         }
        
        .about .about-details{
         display: flex;
         justify-content: space-between;
         align-items: center;
         }
        
        section .title{
              display: flex ;
              justify-content: center;
               margin-bottom: 40px;
        }
        
        section .title span{
         color: white;
         font-size: 30px;
         font-weight: 600;
         position: relative;
         padding-bottom: 8px;
        }
        
        section .title span::before,
        section .title span::after{
         content: "";
         position: absolute;
         height: 3px;
         width: 100%; 
         background: #b74b4b;
         left: 0;
         bottom: 0;
        }
        
        section .title span::after{
         bottom: -7px;
         width: 70%;
         left: 50%;
         transform: translateX(-50%);
        }
        
        .about .about-details.left{
            width: 45%;
        }
        .about .left img{
         height: 400px;
         width: 400px;
         object-fit: cover;
         border-radius: 12px;
        }
        .about-details .right{
         width: 55%;
         color: white;
         text-align: right;
         margin: auto;
         
    
        }
        section .topic{
         color: white;
         font-size: 25px;
         font-weight: 500;
         margin-bottom: 10px;
         
        }
        
        .about-details .right p{
        text-align: justify;
        color: white;
        }
        
        section .button{
        margin: 16px 0;
        }
        
        section .button button{
        outline: none;
        padding: 8px 16px;
        border-radius: 4px;
        font-size: 25px;
        font-weight: 400;
        background: #b74b4b;
        color: #fff;
        border: 2px solid transparent;
        cursor: pointer;
        transition: all 0.4s ease;
        }
        
        section .button button:hover{
        border-color: #b74b4b;
        background-color: #fff;
        color: #b74b4b;
        }

        .skills{
            background: black;
        }
        .skills .content{
            padding: 40px 0;
        }
        .skills .skills-details{
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .skills-details .text{
            width: 50%;
            margin: 0 30px;
        }
        .skills-details p{
             color: white;
             text-align: justify;
             
        }
         .skills .skills-details .experience{
             display: flex;
             align-items: center;
             margin: 0 30px;
        }  
    .skills-details .experience .num{
        color: white;
        font-size: 80px;
    }
    .skills-details .experience .exp{
        color: white;
        margin-left: 20px;
        font-size: 18px;
        font-weight: 500;
        margin: 0 6px;
    }
    .skills-details .boxes{
        width: 45%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
    .skills-details .box{
        width: calc(100%/ 2- 20px);
        margin: 20px  0;
    }
    .skills-details .boxes .topic{
     font-size: 20px;
     color: #b74b4b;
    }
    .skills-details .boxes .per{
     font-size: 60px;
     color: #b74b4b;
    }

    .services .boxes{
     display: flex;
     flex-wrap: wrap;
     justify-content: space-between;
}
    .services .boxes .box{
        margin: 20px 0;
        width: calc(100% /3 - 20px);
        text-align: center;
     border-radius: 12px;
     padding: 30px 10px ;
     box-shadow: 0 5px 10px rgba(0,0,0,0.12) ;
     cursor: default;
     color: white;
     transition: all 0.4s ease;
    }
    .services .boxes .box:hover{
    background: #b74b4b;
    color: #fff;
    }
    .services .boxes .box .icon{
     height: 50px;
     width: 50px;
     background: #b74b4b;
     border-radius: 50%;
     text-align: center;
     line-height: 50px;
     font-size: 18px;
     color: #fff;
     margin: 0 auto 10px auto;
     transition: all 0.4s ease;
    }
    
    .boxes .box:hover .icon{
    background-color: #fff;
    color: #b74b4b;
    }
    
    .services .boxes .box:hover .topic,
    .services .boxes .box:hover p{ 
    color: white;
    transition: all 0,4s ease;
    }
    
    .services .boxes .box:hover .topic,
    .services .boxes .box:hover p{
    color: #fff;
    }
    .contact{
    background: black;
    }
    .contact .contact{
    margin: 0 auto;
    padding: 30px 0;
    }
    .contact .text{
    width: 80%;
    text-align: center;
    margin: auto;
    color: white;
    }
    
    footer{
    background: #b74b4b;
    padding: 15px 0;
    text-align: center;
    font-family: 'poppins', sans-serif;
    }
    footer .text span{
    font-size: 17px;
    font-weight: 400;
    color: #fff;
    }
    
    footer .text span a{
    font-weight: 500;
    color: #FFF;
    }
    
    footer .text span a:hover{
    text-decoration: underline;
    }
    .scroll-button a{
    position: fixed;
    bottom: 20px;
    right: 20px;
    color: #fff;
    background: #b74b4b;
    padding: 7px 12px;
    font-size: 18px;
    border-radius: 6px;
    box-shadow: rgba(0,0,0,0.15);
    display: none;
    }
    
    .social-icons {
            margin-top: 20px;
        }

        .social-icons a {
            color: white;
            font-size: 2rem;
            margin: 0 15px;
            transition: color 0.3s ease;
        }

        .social-icons a:hover {
            color: #e08adc;
        }

        .response-form {
            margin-top: 20px;
            display: none;
        }
    
    @media (max-width:1000px) {
    .about .about-details{
    justify-content: center;
    flex-direction: column;
    }
    .about.about-details.left{
    display: flex;
    justify-content: center;
    width: 100%;
    }
    .about-details.right{
    width: 90%;
    margin: 40px 0;
    }
    .services.boxes .box{
    margin: 20px 0;
    width: calc(100%/2 - 20px);
    }
    }
    
    @media(max-width:900px){
    .about .left img{
    height: 350px;
    width: 350px;
    }
    }
    
    
    @media (max-width:968px) {
    nav .logo{
    position: absolute;
    top: 16px;
    left: 15px;
    font-size: 1.5rem;
    }
    section .main-container {
    padding-left: 0px;
    display: flex;
    flex-direction: column;
    }
    .nav-container .links{
    display: none;
    }
    .hamburg,
    .cancel{
    
    opacity: 1;
    pointer-events: visible;
    }
    .main-container .content{
    margin-top: 20px;
    width: 80%;
    
    }
    .social-links i{
    width: 2.5rem;
    height: 2.5rem;
    font-size: 1.5rem;
    }
    
    .main-container .image{
    z-index: -1;
    width: 50%;
    height: 60%;
    }
    .skills .skills-details{
    align-items: center;
    justify-content: center;
    flex-direction: column;
    }
    .skills-details .text{
    width: 100%;
    margin-bottom: 50px;
    }
    .skills-details .boxes{
    justify-content: center;
    align-items: center;
    width: 100%;
    }
    .services .boxes .box{
    margin: 20px 0;
    width: 100%;
    }
    .contact .text{
    width: 100%;
    }
    }
    
    @media (max-width:500px){
    main-container .image{
    width: 50%;
    height: 60%;
    margin-bottom: 0px;
    }
    .main-container .content{
    width: 80%;
    }
    .main-container button{
    margin-top: 15px;
    }
    
    .skills-details .boxes .per{
    font-size: 50px;
    color: #b74b4b;
    }
    }
    
   


    </style>    
</head>
     <body>
   
         <nav>
         <div class="nav-container">
                 <div class="logo" data-aos-duration="1500" >
                 <span> JEPK</span>
            </div>
            <div class="links">
                <div class="link" data-aos="fade-up" data-aos-duration="1500" data-aos-delay="100"><a href="#main-container">Home</a></div>
                <div class="link" data-aos="fade-up" data-aos-duration="1500" data-aos-delay="200"><a href="#about">About</a></div>
                <div class="link" data-aos="fade-up" data-aos-duration="1500" data-aos-delay="300"><a href="#skills">Skills</a></div>
                <div class="link" data-aos="fade-up" data-aos-duration="1500" data-aos-delay="400"><a href="#services">Services</a></div>
                <div class="link" data-aos="fade-up" data-aos-duration="1500" data-aos-delay="500"><a href="#contact">Contact</a></div>
        </div>
        <i class="fa-solid fa-bars hamburg" onclick="hamburg()"></i>
    </div>
        <div class="dropdown">
            <div class="links">
                <a href="#">Home</a>
                <a href="#">About</a>
                <a href="#">Skills</a>
                <a href="#">Service</a>
                <a href="#">Contact</a>
                <i class="fa-solid fa-xmark cancel" onclick="cancel()"></i>
            </div>
        </div>
    </nav>
    <section>
        <div class="main-container">
            <div class="image" data-aos="zoom-out" data-aos-duration="3000">
                <img src="C:\Users\JaideepKaurVirk\Downloads\image.jpg" alt="">
            </div>
            <div class="content">
                <h1 data-aos="fade-left" data-aos-duration="1500" data-aos-delay="700">Hey I'm <span>Creatify</span></h1>
                <div class="typewriter" data-aos="fade-right" data-aos-duration="1500" data-aos-delay="900">I'm a <span class="typewriter-text"></span><label for="">|</label></div>
                <p data-aos="flip-down" data-aos-duration="1500" data-aos-delay="1100">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Fugit quasi commodi quia rerum, iste corporis expedita in excepturi nesciunt repellendus quisquam amet provident ad mollitia debitis odit voluptatem necessitatibus tempora.</p>
                <div class="social-links">
                    <a href="#" data-aos="fade-up" data-aos-duration="1500" data-aos-delay="1300"><i class="fa-brands fa-github"></i></a>
                    <a href="#" data-aos="fade-up" data-aos-duration="1500" data-aos-delay="1400"><i class="fa-brands fa-facebook"></i></a>
                    <a href="#" data-aos="fade-up" data-aos-duration="1500" data-aos-delay="1500"><i class="fa-brands fa-linkedin"></i></a>
                    <a href="#" data-aos="fade-up" data-aos-duration="1500" data-aos-delay="1600"><i class="fa-brands fa-twitter"></i></a>
                </div>
                <div class="btn" data-aos="zoom-in" data-aos-duration="1500" data-aos-delay="1800">
                    <button>Hire me</button>
                </div>
            </div>
        </div>
    </section>


<section class="about" id="about">
    <div class="content">
        <div class="title"><span> About Me</span></div>
        <div class="about-details">
            <div class="left">
                <img src="C:\Users\JaideepKaurVirk\Downloads\DALL·E 2024-12-13 21.05.24 - A realistic portrait of a young woman with straight dark hair, neutral expression, and natural makeup, wearing a simple and modern outfit. The backgro.webp" alt=""/>
            </div>
            <div class="right">
              <div class="topic"> Designing Is My Passion</div>  
              <p>Hi! I'm [JEPK], a passionate web designer and developer with [10 years] of experience creating modern, functional, and visually stunning websites. My goal is to transform ideas into impactful digital experiences, ensuring every project reflects my clients' unique vision.

                I specialize in web design, app development, and creative solutions that stand out for their innovation and attention to detail. I'm always exploring the latest trends in design and technology to stay ahead of the curve.

              </p>
              <div class="button">
                <button>Download CV</button>
              </div>
            </div>
        </div>
    </div>
</section>

<section class="skills" id="skills">
    <div class="content">
        <div class="title"> <span> My Skills</span></div>
        <div class="skills-details">
            <div class="text">
             <div class="topic">
                Skills Reflects Our Knowledge
             </div>
             <p data-aos="fade-right">Over the years, I've honed my skills in web development and design to deliver high-quality projects that meet and exceed client expectations. My expertise spans various technologies and frameworks, ensuring dynamic, responsive, and visually appealing results. </p>
            <div class="experience">
             <div class="num">10</div>  
             <div class="exp">
                Years Of <br/>
                Experiance
             </div> 
            </div>
            </div>
           <div class="boxes">
            <div class="box">
              <div class="topic">HTML</div> 
              <div class="per">90%</div> 
            </div>
            
                <div class="box">
                  <div class="topic">CSS</div> 
                  <div class="per">80%</div> 
           </div>
           
            <div class="box">
              <div class="topic">JavScript</div> 
              <div class="per">70%</div> 
       </div>
       
        <div class="box">
          <div class="topic">PHP</div> 
          <div class="per">60%</div> 
         </div>
     </div>
      </div>
     </div>
       
</section>

<section class="services" id="services">
    <div class="content">
        <div class="title"><span>My Services</span></div>
        <div class="boxes">
         <div class="box">
           <div class="icon">
            <i class="fas fa-desktop"></i>
           </div> 
           <div class="topic"> Web Devlopment</div>
           <p> I create modern, responsive, and user-friendly websites that are tailored to meet your unique needs. My goal is to help you establish a strong online presence and connect effectively with your audience. </p>
         </div>
         <div class="box">
            <div class="icon">
             <i class="fas fa-paint-brush"></i>
            </div> 
            <div class="topic"> Graphic Design</div>
            <p> I bring ideas to life through creative and eye-catching graphic designs. Whether it's branding or promotional materials, I ensure every design reflects your vision and stands out.</p>
          </div>
          <div class="box">
            <div class="icon">
             <i class="fas fa-chart-line"></i>
            </div> 
            <div class="topic"> Digital marketing</div>
            <p> I develop tailored digital marketing strategies to increase your brand's visibility, drive engagement, and help you reach your target audience on various online platforms.</p>
          </div>    
          <div class="box">
            <div class="icon">
             <i class="fas fa-android"></i>
            </div> 
            <div class="topic"> Icon Design</div>
            <p> I design unique and professional icons that align with your brand’s identity, enhancing the visual appeal and usability of your applications or websites. </p>
          </div> 
          <div class="box">
            <div class="icon">
             <i class="fas fa-camera-retro"></i>
            </div> 
            <div class="topic"> Photography</div>
            <p> I capture high-quality photographs that tell your story, evoke emotions, and leave a lasting impression. Whether personal or professional, I’ll help you preserve moments beautifully. </p>
          </div>
          <div class="box">
            <div class="icon">
             <i class="fas fa-tablet-alt"></i>
            </div> 
            <div class="topic"> Apps Devlopment</div>
            <p> I design and build innovative and user-friendly mobile applications to bring your ideas to life. From concept to launch, I’m here to create tools that make a difference. </p>
          </div>

        </div>
    </div>
</section>

<section class="contact" id="contact">
    <div class="content">
       <div class="title">
        <span>Contact Me</span>
       </div> 
       <div class="text">
        <div  class="topic">Have Any Project?</div>
        <p>Feel free to reach out if you have a project in mind or simply want to discuss your ideas. I’ll be happy to collaborate and provide the best solutions tailored to your needs.
        </p>
        <button id="button">Chat on WhatsApp</button>
        </div>
       </div>
    </div>
</section>




<footer>
    <p>© 2024 My portafolio | All rights reserved </p>
    <div class="social-icons">
        <a href="https://www.instagram.com" target="_blank"><i class="fab fa-instagram"></i></a>
        <a href="https://www.twitter.com" target="_blank"><i class="fab fa-twitter"></i></a>
        <a href="mailto:example@example.com"><i class="fas fa-envelope"></i></a>
        <a href="tel:+1234567890"><i class="fas fa-phone-alt"></i></a>
    </div>
</footer>


    <script src="https://unpkg.com/aos@next/dist/aos.js"></script>
    <script>
      AOS.init({offset:0});
    </script>
    
    <script>
        function hamburg(){
    const navbar = document.querySelector(".dropdown")
    navbar.style.transform = "translateY(0px)"
}
function cancel(){
    const navbar = document.querySelector(".dropdown")
    navbar.style.transform = "translateY(-500px)"
}
// Typewriter Effect
const texts = [
    "DEVELOPER",
    "DESIGNER",
    "YOUTUBER"
]
let speed  =100;
const textElements = document.querySelector(".typewriter-text");
let textIndex = 0;
let charcterIndex = 0;
function typeWriter(){
    if (charcterIndex < texts[textIndex].length){
        textElements.innerHTML += texts[textIndex].charAt(charcterIndex);
        charcterIndex++;
        setTimeout(typeWriter, speed);
    }
    else{
        setTimeout(eraseText, 1000)
    }
}
function eraseText(){
    if(textElements.innerHTML.length > 0){
        textElements.innerHTML = textElements.innerHTML.slice(0,-1);
        setTimeout(eraseText, 50)
    }
    else{
        textIndex = (textIndex + 1) % texts.length;
        charcterIndex = 0;
        setTimeout(typeWriter, 500)
    }
}
window.onload = typeWriter
    </script>

<script>
    // Replace with your phone number (including country code) and a custom message
    const phoneNumber = "34632859206"; // Example: Spain +34 123 456 789
    const message = "Hello, I would like to know more about your services!";

    // Redirect to WhatsApp when the button is clicked
    document.getElementById("button").addEventListener("click", () => {
      const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
      window.open(whatsappUrl, "_blank");
    });
  </script>
   
    </header>
</body>
</html>
