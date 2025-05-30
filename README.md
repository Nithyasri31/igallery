# Ex.08 Design of Interactive Image Gallery
## Date:18/05/2025

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
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <style>
        body {
    font-family: Arial, sans-serif;
    margin: 0;
    background-color: #f4f4f4;
}

.gallery {
    padding: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.thumbnail-container {
    display:flex;
    justify-content: center;
    gap: 100px;
    flex-wrap: wrap;
}

.thumbnail {
    width: 500px;
    height: 350px;
    object-fit: cover;
    cursor: pointer;
    transition: transform 0.3s;
}

.thumbnail:hover {
    transform: scale(1.1);
}

.lightbox {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.8);
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.lightbox-img {
    max-width: 80%;
    max-height: 80%;
    margin: 20px 0;
    border: 2px solid white;
    box-shadow: 0 0 10px black;
}

.caption {
    color: white;
    text-align: center;
    font-size: 18px;
}

.close {
    position: absolute;
    top: 20px;
    right: 20px;
    font-size: 30px;
    color: white;
    cursor: pointer;
}
    </style>
</head>
<body background="Pastel background.jpg">
    <h1 align="center"><font face="Kunstler Script" size="7">Beautiful Islands of the World</font></h1>
    <div class="gallery">
        <div class="thumbnail-container">
            <img src="image 1.jpeg" class="thumbnail" alt="Palawan,Philippines">
            <img src="image 2.jpeg" class="thumbnail" alt="Bali,Indonesia">
            <img src="image 3.jpeg" class="thumbnail" alt="Santorini,Greece">
            <img src="image 4.jpeg" class="thumbnail" alt="Bora Bora,French Polynesia">
            <img src="image 5.jpeg" class="thumbnail" alt="Seychelles">
            
        </div>
        <div class="lightbox">
            <span class="close">&times;</span>
            <img class="lightbox-img" src="" alt="">
            <div class="caption"></div>
        </div>
    </div>
    <script >
        const thumbnails = document.querySelectorAll('.thumbnail');
        const lightbox = document.querySelector('.lightbox');
        const lightboxImg = document.querySelector('.lightbox-img');
        const caption = document.querySelector('.caption');
        const closeBtn = document.querySelector('.close');

        // Event listeners for thumbnails
        thumbnails.forEach(thumbnail => {
            thumbnail.addEventListener('click', () => {
                lightbox.style.display = 'flex';
                lightboxImg.src = thumbnail.src;
                caption.textContent = thumbnail.alt;
            });
        });

        // Close button functionality
        closeBtn.addEventListener('click', () => {
            lightbox.style.display = 'none';
        });

        // Close lightbox on click outside image
        lightbox.addEventListener('click', (e) => {
            if (e.target !== lightboxImg) {
                lightbox.style.display = 'none';
            }
        });

    </script>
</body>
</html>

```
## OUTPUT:
![alt text](<Screenshot 2025-05-18 183656.png>)
![alt text](<Screenshot 2025-05-18 183717.png>)
![alt text](<Screenshot 2025-05-18 183727.png>)
![alt text](<Screenshot 2025-05-18 183737.png>)
![alt text](<Screenshot 2025-05-18 183745.png>)
![alt text](<Screenshot 2025-05-18 183757.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
