- 👋 Hi, I’m @Varun-kt
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Varun-kt/Varun-kt is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
National Education Society ®






Department of Computer Science & Engineering
Jawaharlal Nehru New College of Engineering
Shivamogga - 577 204

Mini Project Report 
ON

WEB PROGRAMMING LAB (21CSL481)


                                                   Submitted by

Name: YASHAS P	     USN:4JN21CS190


Submitted to
Sathyanarayana S B. E, M.Sc. (IT), M. Tech  
Assistant Professor, Dept. of CS&E,


Date:12/09/2023

 
ABSTARCT
Web programming is the process of creating websites, online stores, and other online services. Web programming languages like HTML, CSS, JavaScript, PHP, and Python are used to create these web-based applications.
Web programming is a multifaceted process that involves the development of websites, online stores, and various online services accessible through web browsers. It plays a pivotal role in shaping the digital landscape, as almost every aspect of the internet relies on web programming to some extent.
Web programming is a comprehensive process that involves the use of various programming languages and technologies to create web content, online stores, and interactive web-based applications. These technologies empower businesses, organizations, and individuals to establish a digital presence, engage with users, and offer a wide range of online services to meet the demands of the modern, interconnected world.
















          ACKNOWLEDGEMENT
On presenting the report on Wired LAN, Wireless LAN, and Cellular Telephony, I feel great to express my humble feelings of thanks to all those who have helped me directly or indirectly in the successful completion of this work.
 I would like to thank Mr. Satyanarayana S, Assistant Professor, Dept. of CS&E, who has helped a lot in completing this task, with his continuous encouragement and guidance throughout the work.
I would like to thank Dr. Jalesh Kumar, Professor and Head, Dept. of CSE, JNNCE, Shivamogga and Principal, JNNCE, Shivamogga for all their support and encouragement.
I am grateful to the Department of Computer Science and Engineering and our institution Jawaharlal Nehru New College of Engineering for imparting to me the knowledge with which I can do my best.
	Finally, I also would like to thank the whole teaching and non-teaching staff of Computer Science and Engineering Dept.
                                               
Thanking you all,





Program Code
//index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <link rel="stylesheet" href="style.css" />
    <title>Surprise</title>
  </head>
  <body>
    <div id="year" class="year"></div>

    <h1>Surprise starts in</h1>

    <div id="countdown" class="countdown">
      <div class="time">
        <h2 id="days">00</h2>
        <small>days</small>
      </div>
      <div class="time">
        <h2 id="hours">00</h2>
        <small>hours</small>
      </div>
      <div class="time">
        <h2 id="minutes">00</h2>
        <small>minutes</small>
      </div>
      <div class="time">
        <h2 id="seconds">00</h2>
        <small>seconds</small>
      </div>
    </div>

    <img
      src="./img/spinner.gif"
      alt="Loading..."
      id="loading"
      class="loading"
    />

    <script src="script.js"></script>
  </body>
</html>



//style.css
@import url('https://fonts.googleapis.com/css?family=Lato&display=swap');

* {
  box-sizing: border-box;
}

body {
  background-image: url('https://wallpapercave.com/wp/wp3910869.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
  height: 100vh;
  color: #ffffff;
  font-family: 'Lato', sans-serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin: 0;
  overflow: hidden;
}

/* Add a dark overlay */
body::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

body * {
  z-index: 1;
}

h1 {
  font-size: 60px;
  margin: -80px 0 40px;
}

.year {
  font-size: 200px;
  z-index: -1;
  opacity: 0.2;
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
}

.countdown {
  /* display: flex; */
  display: none;
  transform: scale(2);
}

.time {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 15px;
}

.time h2 {
  margin: 0 0 5px;
}

@media (max-width: 500px) {
  h1 {
    font-size: 45px;
  }

  .time {
    margin: 5px;
  }

  .time h2 {
    font-size: 12px;
    margin: 0;
  }

  .time small {
    font-size: 10px;
  }
}







//script,js
const days = document.getElementById('days');
const hours = document.getElementById('hours');
const minutes = document.getElementById('minutes');
const seconds = document.getElementById('seconds');
const countdown = document.getElementById('countdown');
const year = document.getElementById('year');
const loading = document.getElementById('loading');

const currentYear = new Date().getFullYear();

const newYearTime = new Date(`October 01 ${currentYear + 1} 00:00:00`);

// Set background year
year.innerText = currentYear + 1;

// Update countdown time
function updateCountdown() {
  const currentTime = new Date();
  const diff = newYearTime - currentTime;

  const d = Math.floor(diff / 1000 / 60 / 60 / 24);
  const h = Math.floor(diff / 1000 / 60 / 60) % 24;
  const m = Math.floor(diff / 1000 / 60) % 60;
  const s = Math.floor(diff / 1000) % 60;

  // Add values to DOM
  days.innerHTML = d;
  hours.innerHTML = h < 10 ? '0' + h : h;
  minutes.innerHTML = m < 10 ? '0' + m : m;
  seconds.innerHTML = s < 10 ? '0' + s : s;
}

// Show spinner before countdown
setTimeout(() => {
  loading.remove();
  countdown.style.display = 'flex';
}, 1000);

// Run every second
setInterval(updateCountdown, 1000);





Snapshot

 
