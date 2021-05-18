#Snowing animation created using HTML, CSS and JavaScript.

This project can be used on various webpages to add decoration - the snowflakes can be changed for whatever else is needed.

Constructing this project helped me to better learn and practice the following:
1) Css

A general walkthrough of the JavaScript code is given below.

First construct the createSnowFlake() function to create the snowflakes and set their positions/numbers/ and styles and then render it to the body using setInterval.
```JavaScript
function createSnowFlake(){
    const snowFlake = document.createElement('i');
    snowFlake.classList.add('fas');
    snowFlake.classList.add('fa-snowflake');
    snowFlake.style.left = Math.random() * window.innerWidth + 'px';

    document.body.appendChild(snowFlake);
}
setInterval(createSnowFlake, 100);
```


Now remove the snow flakes which have reached the screen bottom by way of a setTimeout() function.
```JavaScript
setTimeout(() => {snowFlake.remove()}, 7000)
```


To give a more realistic animation, an animation duration, opacity, and size are used.
```JavaScript
    snowFlake.style.animationDuration = Math.random() * 3 + 2 + 's';
    snowFlake.style.opacity = Math.random();
    snowFlake.style.fontSize = Math.random() * 10 + 10 + 'px'
```


***End walkthrough
