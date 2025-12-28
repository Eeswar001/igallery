# Ex.08 Design of Interactive Image Gallery
## Date:

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
<title>Image Viewer</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>
body{
  background:#0f172a;
  color:white;
  font-family:Arial;
  text-align:center;
}

h1{
  margin-top:25px;
}

/* Image Box */
.container{
  width:70%;
  margin:auto;
  margin-top:40px;
}

img{
  width:100%;
  height:450px;
  object-fit:cover;
  border-radius:10px;
  border:3px solid white;
}

/* Counter */
#count{
  margin-top:15px;
  font-size:20px;
}

/* Buttons */
button{
  margin:25px 15px;
  padding:10px 25px;
  font-size:18px;
  border:none;
  border-radius:8px;
  cursor:pointer;
}

.prev{
  background:#ff4d6d;
  color:white;
}

.next{
  background:#1dd3b0;
  color:black;
}

button:hover{
  opacity:0.8;
}
</style>
</head>

<body>

<h1>Image Gallery</h1>

<div class="container">
  <img id="image" src="https://i.imgur.com/7yZ9FJR.jpeg">
  <p id="count">1 / 6</p>
</div>

<button class="prev" onclick="prev()">Previous</button>
<button class="next" onclick="next()">Next</button>

<script>
let images = [
  "https://images.deccanherald.com/deccanherald/import/sites/dh/files/article_images/2013/08/06/349547.jpg?w=1200&ar=40:21&auto=format%2Ccompress&ogImage=true&mode=crop",
  "https://th.bing.com/th/id/OIP.IRTh-PWIdLRsILbTJPnwJQHaGC?w=255&h=208&c=7&r=0&o=7&dpr=1.3&pid=1.7&rm=3",
  "https://i.etsystatic.com/9735629/r/il/419959/3977304265/il_300x300.3977304265_pel5.jpg",
  "https://th.bing.com/th/id/OIP.qNCzIImhuVydzkks8OmHbwHaFY?w=264&h=191&c=7&r=0&o=7&dpr=1.3&pid=1.7&rm=3",
  "https://webneel.com/daily/sites/default/files/images/daily/10-2018/16-scenery-oil-painting-autumn-arteet.jpg",
  "https://th.bing.com/th/id/R.5f94409cf83d22f15b821ec8bca5ac96?rik=70Kh8Q2dWwV3Hw&riu=http%3a%2f%2fwebneel.com%2fdaily%2fsites%2fdefault%2ffiles%2fimages%2fdaily%2f10-2018%2f2-landscape-oil-painting-chuckblackart.jpg&ehk=Qhfp4XtFAYIaKvwui0H2Q1ZEyf0jAplu07s%2biJCxdRw%3d&risl=&pid=ImgRaw&r=0"
];

let index = 0;
let img = document.getElementById("image");
let counter = document.getElementById("count");

function show(){
  img.src = images[index];
  counter.innerText = (index+1) + " / " + images.length;
}

function next(){
  index = (index + 1) % images.length;
  show();
}

function prev(){
  index = (index - 1 + images.length) % images.length;
  show();
}
</script>

</body>
</html>

```
## OUTPUT:
<img width="603" height="451" alt="image" src="https://github.com/user-attachments/assets/6d445f2a-6808-4669-ad33-b05f3c7bde8c" />
<img width="752" height="442" alt="image" src="https://github.com/user-attachments/assets/99a3dba0-7c59-4258-8ac4-e11f84b9f82c" />
<img width="756" height="457" alt="image" src="https://github.com/user-attachments/assets/4919bfdd-5815-4cea-97b0-67d0990443b9" />
<img width="753" height="446" alt="image" src="https://github.com/user-attachments/assets/2af092c1-b1c3-4390-84d7-6cc820b46eb7" />
<img width="742" height="447" alt="image" src="https://github.com/user-attachments/assets/78ef12f7-3d16-4ca6-ab45-d595bc9a10e3" />
<img width="743" height="463" alt="image" src="https://github.com/user-attachments/assets/14808b33-b9fd-48ea-b08a-13bbd5fd956d" />
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
