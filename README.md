# Ex.08 Design of Interactive Image Gallery
## Date:07/05/2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Image Gallery</title>
  <style>
    * {
      margin: 0px;
      padding: 0px;
      box-sizing: border-box;
    }

    body {
      background-image: url(bg.png);
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
    }

    .tit h1 {
      color: aliceblue;
      font-size: 46px;
      padding: 30px;
      text-align: center;
    }

    .c1 {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 30px;
      justify-items: center;
      padding: 30px;
    }

    .c1 img {
      width: 250px;
      height: 250px;
      object-fit: cover;
      cursor: pointer;
      transition: transform 0.3s;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
    }

    .c1 img:hover {
      transform: scale(1.05);
    }

    /* Popup styles */
    .popup {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-color: rgba(0, 0, 0, 0.8);
      display: none;
      justify-content: center;
      align-items: center;
      z-index: 999;
    }

    .popup img {
      width: 70%;
      max-width: 700px;
      border-radius: 20px;
      box-shadow: 0 0 30px rgba(255, 255, 255, 0.3);
    }
  </style>
</head>
<body>
  <div class="tit">
    <h1>IMAGE GALLERY</h1>
  </div>

  <div class="c1">
    <img src="https://picsum.photos/300/300?random=1" alt="Random Image" onclick="showPopup(this.src)" />
    <img src="https://picsum.photos/300/300?random=2" alt="Random Image" onclick="showPopup(this.src)" />
    <img src="https://picsum.photos/300/300?random=3" alt="Random Image" onclick="showPopup(this.src)" />
    <img src="https://picsum.photos/300/300?random=4" alt="Random Image" onclick="showPopup(this.src)" />
    <img src="https://picsum.photos/300/300?random=5" alt="Random Image" onclick="showPopup(this.src)" />
    <img src="https://picsum.photos/300/300?random=6" alt="Random Image" onclick="showPopup(this.src)" />
    <img src="https://picsum.photos/300/300?random=7" alt="Random Image" onclick="showPopup(this.src)" />
    <img src="https://picsum.photos/300/300?random=8" alt="Random Image" onclick="showPopup(this.src)" />
  </div>

  <!-- Popup Container -->
  <div class="popup" id="popup" onclick="hidePopup()">
    <img id="popupImage" src="" alt="Popup Image" />
  </div>

  <script>
    function showPopup(src) {
      const popup = document.getElementById("popup");
      const popupImg = document.getElementById("popupImage");
      popupImg.src = src;
      popup.style.display = "flex";
    }

    function hidePopup() {
      document.getElementById("popup").style.display = "none";
    }
  </script>
</body>
</html>
```


## OUTPUT:
![alt text](<Screenshot 2025-05-17 152025.png>)
![alt text](<Screenshot 2025-05-17 152044.png>)
![alt text](<Screenshot 2025-05-17 152057.png>)
![alt text](<Screenshot 2025-05-17 152112.png>)
![alt text](<Screenshot 2025-05-17 152124.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
