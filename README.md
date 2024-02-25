# WEB
Progress into website creation for web portfolio
HTML:
---------------------------------------------------------------------------------------------------------------------
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equic="X-UA-Compatiblr" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Portfolio Website</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="header">
        <div class="container">
            <nav>
                <img src="Images/Logo.jpg" class="logo">
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">About</a></li>
                    <li><a href="#">Service</a></li>
                    <li><a href="#">Portfolio</a></li>
                    <li><a href="#">Contacts</a></li>
                </ul>
            </nav>
            <div class="header-text">
                <p>Student</p>
                <h1> Hi, I'm <span>Michael Potgieter</span><br>from South Africa.</h1>
            </div>
        </div>
    </div>
 <!----------------------------------about--------------------------------->   
 <div id="about">
    <div class="container">
        <div class="row">
            <div class="about-col-1">
                 <img src="Images/portfolio.jpg">
            </div>
            <div class="about-col-2">
                <h1 class="sub-title">About Me:</h1>
                <p>Programming is a transformative skill that empowers individuals to 
                   shape the digital landscape and solve complex problems. It serves 
                   as a creative outlet, allowing individuals to bring their ideas to 
                   life through the development of software, applications, and websites.
                    Beyond the realm of creativity, programming enhances logical thinking 
                    and problem-solving abilities, fostering a mindset that thrives on 
                    precision and efficiency.</p>

             <div class="tab-titles">
                <p class="tab-links active-link" onclick="opentab('skills')"> Skills</p>
                <p class="tab-links" onclick="opentab('experience')"> Experience</p>
                <p class="tab-links" onclick="opentab('education')"> Education</p>
             </div>
             <div class="tab-contents active-tab" id="skills">
                <ul>
                    <li><span>UI/UX</span><br>Designing Web/App Interfaces</li>
                    <li><span>Web Development</span><br>Web app Developments</li>
                    <li><span>App Development</span><br>Building Android/iOS apps</li>
                </ul>
             </div>
             <div class="tab-contents" id="experience">
                <ul>
                    <li><span>UI/UX3</span><br>Designing Web/App Interfaces3</li>
                    <li><span>Web Deve3lopment</span><br>Web app Deve3lopments</li>
                    <li><span>App Development3</span><br>Building Androi3d/iOS apps</li>
                </ul>
             </div>
             <div class="tab-contents" id="education">
                <ul>
                    <li><span>2023</span><br>HighSchool</li>
                    <li><span>2026</span><br>Software engineering</li>
                    <li><span>2027</span><br>Honours-Software engineering</li>
                </ul>
             </div>
            </div>
        </div>
    </div>
 </div>
 <!---------------------services--------------------------------------------- -->
 <div id="Services">
    <div class="container">
        <h1 class="sub-title">My Services:</h1>
        <div class="services-list">
            <div>
                <h3>Software Development</h3>
                <p> Services not yet avalible.</p>
                 <a href="#"> Learn  More </a>
            </div>
        </div>
    </div>
 </div>
<!-----------------------------------portfolio----------------------------------->
<div id="portfolio">
    <div class="container">
        <h1 class="sub-title">My Portfolio:</h1>
        <div class="work-list">
            <div class="work"></div>
            <img src="Images/webdesign.jpg">
            <div class="Layer">
                <h3>Website</h3>
                <p> The website I use as my portfolio I have coded myself.</p>
                <a href="https://github.com/UrExStacy/WEB">Visit My GitHub Repository</a>

            </div>
        </div>
        <div class="work"></div>
        <img src="Images/Code1.jpg">
        <div class="Layer">
            <h3>Programs</h3>
            <p> All my future projects/programs will be saved on GitHUB.</p>
            <a href="https://github.com/UrExStacy">Visit My GitHub Repository</a>
                <i class="fa-solid fa-link"></i>
            </a>
            
        </div>
    </div>
    </div>

</div>

<!-----------------------Contact--------------------------------->
<div id="contact">
    <div class="container">
        <div class="row">
            <div class="contact-left">
                <h1 class="sub-title">Contact Me</h1>
                <p> Mikkelmuis7@gmail.com</p>
                <p>0646514095</p>
                <p>@michael_potgieter_05</p>
            </div>
            <div class="contact-right"></div>
        </div>
    </div>
</div>



 <script>
    var tablinks = document.getElementsByClassName("tab-links");
    var tabcontents = document.getElementsByClassName("tab-contents");
 
    function opentab(tabname){
      for(tablink of tablinks){
         tablink.classList.remove("active-link");
      }
      for(tabcontent of tabcontents){
         tabcontent.classList.remove("active-tab");
      }
      event.currentTarget.classList.add("active-link");
      document.getElementById(tabname).classList.add("active-tab");
    }
 </script>
 

</body>
</html>
--------------------------------------------------------------------------------------------------------------------
CSS:
--------------------------------------------------------------------------------------------------------------------
*{
    margin: 0;
    padding: 0;
    font-family: "Poppins", sans-serif;
    box-sizing: border-box;
}

body{
    background: #080808;
    color: #fff;
}
#header{
    width: 100%;
    height: 100vh;
    background-image: url(Images/background.jpg) ;
    background-size: cover;
    background-position: center;
}
.container{
    padding: 10px 10%; 
}

nav{
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
}

.logo{
    width: 140px;

}
nav ul li{
    display: inline-block;
    list-style: none;
    margin: 10px 20px;
}

nav ul li a{
    color: #fff;
    text-decoration: none;
    font-size: 18px;
    position: relative;
}
nav ul li a::after{
    content: '';
    width: 0;
    height: 3px;
    background: #4169e1;
    position:absolute;
    left: 0;
    bottom: -6px;
    transition: 0.4s;
}
nav ul li a:hover::after{
    width: 100%;
}
.header-text{
    margin-top: 20%;
    font-size: 30px; 
}
.header-text h1{
    font-size: 60px;
    margin-top: 20px;
}
.header-text h1 span{
    color: #4169e1;
}
/* ----------------------------------about--------------------------------- */
#about{
    padding: 80px 0;
    color:#ffffff;
}
.row{
    display:flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
.about-col-1{
    flex-basis: 35%;
}
.about-col-1 img{
    width: 100%;
    border-radius: 15px;
}
.about-col-2{
    flex-basis: 60%;
}

.sub-title{
    font-size: 60px;
    font-weight: 600;
    color: #4169e1;
}

.tab-titles{
    display: flex;
    margin: 20px 0 40px;
}

.tab-links{
    margin-right: 50px;
    font-size: 18px;
    font-weight: 500;
    cursor: pointer;
    position: relative;
}

.tab-links::after{
    content: '';
    width: 0;
    height: 3px;
    background: #4169e1;
    position: absolute;
    left: 0;
    bottom : -8px;
    transition: 0.5;
}
.tab-links.active-link::after{
    width: 50%;
}
.tab-contents ul li{
    list-style: none;
    margin: 10px;
}
.tab-contents ul li span{
    color: #4169e1;
    font-size: 14px;
}
.tab-contents{
    display: none;
}
.tab-contents.active-tab{
    display: block;
}
/*----------------------------services------------------------*/
#services{
    padding: 30px 0;
}
.services-list{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
    grid-gap: 40px;
    margin-top: 50px;
}
.services-list div{
    background: #262626;
    padding: 40px;
    font-size: 13px;
    font-weight: 300;
    border-radius: 10px;
    transition: background-color 0.5s, transform 0.5s;
}

.services-list h2{
    font-size: 30px;
    font-weight: 500;
    margin-bottom: 15px;
}
.services-list div a{
    text-decoration: none;
    color: #fff;
    font-size: 12px;
    margin-top: 20px;
    display: inline-block;
}
.services-list div:hover{
    background: #4169e1;
    transform: translateY(-10px);
}
/*---------------------------------portfolio-----------------------------*/
#portfolio{
    padding: 50px 0;
}
.work-lis{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
    grid-gap: 40px;
    margin-top: 50px; 
}
.work{
    border-radius: 10px;
    position: relative;
    overflow:hidden;
}

.work img{
    width: 100%;
    border-radius: 10px;
    display: block;
}
