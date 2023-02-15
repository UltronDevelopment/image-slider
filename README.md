# Image-Slider
An image slider is a web design element that allows you to display a series of images or slides in a specific area of a webpage, usually in a slideshow format. The purpose of an image slider is to showcase multiple images in a limited space and allow website visitors to view them in a sequence by sliding the images horizontally or vertically.

Image sliders typically include a set of navigation buttons or indicators, such as dots or arrows, that enable users to move forward or backward through the slides. The slider may also automatically cycle through the slides after a set interval of time, or allow users to set the time duration themselves.

Image sliders can be used to display a variety of content, such as product images, portfolio items, or photographs. They are a popular way to add visual interest and interactivity to a webpage and to help highlight key messages or content. However, it's important to use them judiciously and considerately, as they can sometimes be distracting or slow down page load times.

# Changeable options

To adjust the animation duration you should set the -webkit-animation-duration & animation-duration section in the css to the desired speed

```css
        .fade {
        -webkit-animation-name: fade;
        -webkit-animation-duration: 5.0s; /* This one here */
        animation-name: fade;
        animation-duration: 5.0s; /* This one here */
        }
```       
However, you still have to change the speed in JavaScript

If you setTimeout(show Slides, 5000); (last line) set to 6000, the animation duration is 6 seconds

````js
        var slideIndex = 0;
        showSlides();
        
        function showSlides() {
          var i;
          var slides = document.getElementsByClassName("mySlides");
          for (i = 0; i < slides.length; i++) {
            slides[i].style.display = "none"; 
          }
          slideIndex++;
          if (slideIndex > slides.length) {slideIndex = 1} 
          slides[slideIndex-1].style.display = "block"; 
          setTimeout(showSlides, 5000); // Change image every 5 seconds
        }
````

Hopefully the rest is clear if there are any problems you can always open a ticket on our [discord](https://discord.gg/rgAXuVrxxs)
