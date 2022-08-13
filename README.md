- 👋 Hi, I’m @MSami625
- 👀 I’m interested in programming and all stuff regarding technology.
- 🌱 I’m currently learning programming and science.
- 💞️ I’m looking to collaborate for creating some good and useful stuff.


<!---
MSami625/MSami625 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Typing Text Animation | Dev Mode</title>

  <!-- CSS -->
  <style>
  /* ---------GOOGLE FONTS------ */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;800&display=swap');

/* ---------VARIABLES--------- */
:root{
  /* FONTS */
  --font: 'Poppins', sans-serif;

  /* COLORS */
  --background-color: #9176FF;
  --color: #FFDE59;
}


/* ----------BASE----------- */
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: var(--font);
}

body{
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: var(--background-color);
  overflow: hidden;
}

ul,
li{
  text-decoration: none;
  list-style: none;
}


/* ----------TEXT------------*/
.container{
  display: flex;
  justify-content: center;
  align-items: center;
}

.static-text{
  color: #fff;
  font-size: 80px;
  font-weight: 600;
}

.dynamic-texts{
  margin-left: 15px;
  height: 120px;
  overflow: hidden;
}

.dynamic-text{
  font-size: 80px;
  font-weight: 800;
  color: var(--color);
  text-shadow: 0 5px 10px rgba(0,0,0,.2);
  letter-spacing: 2px;

  position: relative;
  top: 0;

  animation: slide-texts steps(3) 12s infinite;
}

.dynamic-text span{
  display: inline-block;
  position: relative;
}

.dynamic-text span::before{
  content: '';
  width: 100%;
  height: 100%;
  background-color: var(--background-color);
  position: absolute;
  left: 0;

  animation: typing steps(12) 2s infinite alternate;
}

.dynamic-text span::after{
  content: '';
  width: 100%;
  height: 100%;
  width: 3px;
  background-color: var(--color);
  position: absolute;
  left: 0;

  animation: typing steps(12) 2s infinite alternate,
             blink 800ms infinite;
}


@keyframes slide-texts{
  to{
    top: -360px;
  }
}

@keyframes typing{
  100%{
    left: 100%;
    margin: 0 -50px 0 50px;
  }
}

@keyframes blink {
  50%{
    background-color: transparent;
  }
}
  </style>

</head>
<body>

  <div class="container">

    <span class="static-text">I'am a</span>
    <ul class="dynamic-texts">
      <li class="dynamic-text"><span>Developer</span></li>
      <li class="dynamic-text"><span>Designer</span></li>
      <li class="dynamic-text"><span>Frontend</span></li>
    </ul>
  </div>

</body>
</html>
