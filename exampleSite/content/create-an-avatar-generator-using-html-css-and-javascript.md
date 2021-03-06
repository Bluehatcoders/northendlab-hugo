**Project Introduction:** In this project we are going to create an avatar generator which will create an avatar with the name of users. Users can also download the avatar locally on their computer. We will make this project using **HTML**, **CSS** and **JavaScript**.

**File structure:**


- index.html
- style.css
- script.js

**HTML codes**: In the * index.html* file we will place these HTML codes.

```
<!DOCTYPE html>
<html lang="en">
  <!-- Head -->
  <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
        
        <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no, maximum-scale=1, shrink-to-fit=no">
        <title>Avatar Generator - Generate by Name</title>
        <meta property="og:title" content="Avatar Generator - Generate by Name">


        <meta property="og:description" content="Genearte your cool avatars with your name">
        <meta name="description" content="Genearte your cool avatars with your name">
        <link rel="shortcut icon" href="avatargeneratoricon.png" type="image/x-icon">
	<link rel="apple-touch-icon" href="avatargeneratoricon.png">
	<link rel="apple-touch-icon" sizes="76x76" href="avatargeneratoricon.png">
      
        <!-- Template core CSS -->
        
        <link href="template.min.css" rel="stylesheet">
       
        
    </head>
    <!-- Head -->

    <body>

        <div class="layout">

            <div class="container d-flex flex-column">
                <div class="row align-items-center justify-content-center no-gutters min-vh-100">
                    <div class="outputs" style="padding: 1.5rem 2.3rem;">
                        <img id="img" style="border-radius: 50%; width: 100%; vertical-align: super;"/>
            
                      </div>
                    <div class="col-12 col-md-5 col-lg-4 py-md-11">

    
                        <!-- Form -->
                        <form>
                            <!-- Email -->
                            <div class="form-group">
                                <label for="email" class="sr-only">Your First Name</label>
                                <input type="text" class="form-control form-control-lg" id="firstname" placeholder="Enter your First Name">
                            </div>

                            <!-- Password -->
                            <div class="form-group">
                                <label for="password" class="sr-only">lastname</label>
                                <input type="text" class="form-control form-control-lg" id="lastname" placeholder="Enter your Last Name">
                            </div>

                          

                            <!-- Submit -->
                            <button class="btn btn-lg btn-primary" id="generateAvatar" type="submit"><svg width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-check2-circle" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                                <path fill-rule="evenodd" d="M15.354 2.646a.5.5 0 0 1 0 .708l-7 7a.5.5 0 0 1-.708 0l-3-3a.5.5 0 1 1 .708-.708L8 9.293l6.646-6.647a.5.5 0 0 1 .708 0z"/>
                                <path fill-rule="evenodd" d="M8 2.5A5.5 5.5 0 1 0 13.5 8a.5.5 0 0 1 1 0 6.5 6.5 0 1 1-3.25-5.63.5.5 0 1 1-.5.865A5.472 5.472 0 0 0 8 2.5z"/>
                              </svg> Create</button>
                            <button class="btn btn-lg" id="generateAvatar" type="submit" style="display: inline; color: #fff;
                            background-color: #FFC107; border-color: #FFC107;"><svg width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-shuffle" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                                <path fill-rule="evenodd" d="M0 3.5A.5.5 0 0 1 .5 3H1c2.202 0 3.827 1.24 4.874 2.418.49.552.865 1.102 1.126 1.532.26-.43.636-.98 1.126-1.532C9.173 4.24 10.798 3 13 3v1c-1.798 0-3.173 1.01-4.126 2.082A9.624 9.624 0 0 0 7.556 8a9.624 9.624 0 0 0 1.317 1.918C9.828 10.99 11.204 12 13 12v1c-2.202 0-3.827-1.24-4.874-2.418A10.595 10.595 0 0 1 7 9.05c-.26.43-.636.98-1.126 1.532C4.827 11.76 3.202 13 1 13H.5a.5.5 0 0 1 0-1H1c1.798 0 3.173-1.01 4.126-2.082A9.624 9.624 0 0 0 6.444 8a9.624 9.624 0 0 0-1.317-1.918C4.172 5.01 2.796 4 1 4H.5a.5.5 0 0 1-.5-.5z"/>
                                <path d="M13 5.466V1.534a.25.25 0 0 1 .41-.192l2.36 1.966c.12.1.12.284 0 .384l-2.36 1.966a.25.25 0 0 1-.41-.192zm0 9v-3.932a.25.25 0 0 1 .41-.192l2.36 1.966c.12.1.12.284 0 .384l-2.36 1.966a.25.25 0 0 1-.41-.192z"/>
                              </svg> Random</button>
                            <a id="img1" style="display: inline; padding: .875rem 1.09rem; border-radius: 50%; color: white; background-color: green; border-color: #4CAF50;" download ><svg width="1em" height="1em" viewBox="0 0 16 16" class="bi bi-download" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                                <path fill-rule="evenodd" d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5z"/>
                                <path fill-rule="evenodd" d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3z"/>
                              </svg></a>
                      
                        </form>
                    </div>
                   
                </div> <!-- / .row -->
                
            </div>
        
        </div><!-- .layout -->
    

        <!-- Scripts -->
        <script src="bootstrap.bundle.min.js.download"></script>
        <script  src="script.js"></script>
        <!-- Scripts -->

    
</body></html>
``` 

**CSS codes** : In the *style.css* file we will place these CSS codes.


```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}
body {
  display: flex;
  height: 100vh;
  width: 100%;
  align-items: center;
  justify-content: center;
}

input[type="text"] {
  padding: 0.5rem;
  border-radius: 0.3rem;
  border: none;
  margin: 10px 0;
  display: block;
  background: #e9e9e9;
}
img {
  border: 2px solid #f4f4f4;
  border-radius: 50%;
}
.inputs,
.outputs {
  padding: 0.5rem 1rem;
}
#generateAvatar {
  padding: 0.5rem;
  width: 100%;
  border-radius: 0.5rem;
  border: none;
  background-color: #7070ff;
  color: #f4f4f4;
  cursor:pointer;
}
@media screen and (max-width: 560px) {
  body {
    flex-direction: column-reverse;
  }
}

``` 

**JavaScript codes**: In the *script.js* file we will place these JS codes.


```
// selecting components
let firstname, lastname, generate, avatar, ctx, color;
firstname = document.getElementById("firstname");
lastname = document.getElementById("lastname");
generate = document.querySelector("form");

//creating canvas
avatar = document.createElement("canvas");
avatar.width = avatar.height = "200";
ctx = avatar.getContext("2d");
ctx.font = `${avatar.width / 2}px Arial`;
ctx.textAlign = "center";

//generating color
color = [
            "#5050ff",                                                             
            "#50ff53",                              "#7f8c8d",
            "#ff5050",                                  "#e74c3c",
            "#ff5000",                                      "#c0392b",
            "#ff0050",                                          "#22ffcc",                                    
  "#1abc9c", "#00ff50", "#2c3e50", "#ff7600", "#0050ff", "#9b59b6", "#e722ff", 
  "#1abc9c", "#50ff00", "#2c3e50", "#95a5a6", "#f39c12", "#d35400",  "#e722ff",
  "#2ecc71", "#5000ff", "#f1c40f", "#e74c3c", "#bdc3c7", "#7f8c8d",  "#638a04",
  "#3498db", "#ff0000", "#e67e22", "#7f8c8d", "#000fc7", "#a0ff22", "#7f8c8d",
            "#E91E63",                                          "#7f8c8d",
            "#34495e",                                      "#a901ff",
            "#16a085",                                  "#0176ff",
            "#27ae60",                              "#FFC107",
            "#2980b9",                          "#FF5722",
            "#8e44ad", 
   
];


//functions
//function to get name initials
function getInitials() {
  if (lastname.value == "") {
    let Initials = firstname.value[0].toUpperCase();
    return Initials;
  } else {
    let Initials = (firstname.value[0] + lastname.value[0]).toUpperCase();
    return Initials;
  }
}

//function to create avatar
function createAvatar(Initials) {
  let random = Math.floor(Math.random() * color.length);
  //clear canvas
  ctx.fillStyle = "#ffffff";
  ctx.fillRect(0, 0, avatar.width, avatar.height);

  //add background
  ctx.fillStyle = `${color[random]}50`;
  ctx.fillRect(0, 0, avatar.width, avatar.height);

  //add text
  ctx.fillStyle = color[random];
  ctx.fillText(Initials, avatar.width / 2, (66 / 100) * avatar.height);

  //generate as Image
  let dataURL = avatar.toDataURL();
  document.getElementById("img").src = dataURL;
  document.getElementById("img1").href = dataURL;
}
//Event Listener
generate.addEventListener("submit", (e) => {
  e.preventDefault();
  createAvatar(getInitials());
});



let emoji = ["????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????", "????"];
let finalresult = emoji[Math.floor(Math.random() * emoji.length)];
      

// Preloaded avatar for example
createAvatar(`${finalresult}`);
``` 

**Output:**


![ezgif7addba65f5c1b.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1610178815921/jlupeEyq-.gif)

See it live :-  https://generateavatar.netlify.app/


The Original article is publishing soon on Geekforgeeks. The article is under review on Geekforgeeks.org
