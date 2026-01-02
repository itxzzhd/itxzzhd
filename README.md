<div align="center">

<img src="https://avatars.githubusercontent.com/u/195712986?v=4" width="100"/>

<h1 style="font-family: serif; letter-spacing: 4px;">
h1t3s7
</h1>

</div>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> My self </title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

  <div>   
    
                          <div class="typing-container">
                          <span id="typing-text"></span>

  </div>

                         
   
  </div>        


               <h2> 



                        Hi, my name is Hitesh. <br>
                        I truley intrested and passionate about devlopment and cyber security.<br>
                        I love to learn new things and explore new technologies.
                        


                                                      </h2>


    <script src="script.js"></script>

</body>
</html>





  const texts = ["Welcome", "સ્વાગત છે"];
  let index = 0;
  let charIndex = 0;
  let isDeleting = false;
  const speed = 100;
  const delay = 1500;

  const typingElement = document.getElementById("typing-text");

  function typeEffect() {
    const currentText = texts[index];

    if (isDeleting) {
      typingElement.textContent = currentText.substring(0, charIndex--);
    } else {
      typingElement.textContent = currentText.substring(0, charIndex++);
    }

    if (!isDeleting && charIndex === currentText.length + 1) {
      setTimeout(() => isDeleting = true, delay);
    } else if (isDeleting && charIndex === 0) {
      isDeleting = false;
      index = (index + 1) % texts.length;
    }

    setTimeout(typeEffect, isDeleting ? speed / 2 : speed);
  }

  typeEffect();




body {

    background-color: rgb(0, 0, 0);
    font-family: Arial, sans-serif;
    color: #333333;
    margin: 20px;              
                           } 
                  

h2 {

      font-size: small;
      color: #dddddd;
      margin: 10px 0;
      padding: 5px 0;
      text-align: left;
      line-height: 1.6;
      margin-left: 500px;
      

                          }




.typing-container {
  text-align: center;
  font-size: 40px;
  font-weight: bold;
  color: #ffffff;
  margin-top: 20px;
  height: 60px;
}

#typing-text::after {
  content: "|";
  margin-left: 5px;
  animation: blink 1s infinite;
}

@keyframes blink {
  0%, 50%, 100% { opacity: 1; }
  25%, 75% { opacity: 0; }
}


