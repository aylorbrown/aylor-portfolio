### Aylor Brown Portfolio 


![Aylor Brown](assets/Kapture-2020-02-06-at-6.40.24.gif)

## Challenges
I found a template that I liked and reverse-engineered it, adding my own features like a sticky header. 

The biggest development challenge was making the mobile site responsive and creating a div split in two with content on the right and left. Basically, each side takes up exactly half of the container, creating a distinct break between the one. After watching a few tutorials, I made a section parent with two div children.


```html
<section class="container">
        <div class="left-half">
            <a href="adoptandchill.html"><h1>Adopt and Chill</h1></a>  
        </div>

        <div class="right-half">
            <a href="adoptandchill.html">
            <img src="assets/adopt-and-chill-dog.png" alt="dog with weed leaves for eyes" class="img">
            </a>
        </div>
    </section>
```

I originally used fake tables with ```display:table``` and ```left:0``` for the left div and ```right:0``` for the right div. This solution worked in laptop mode, but broke down in mobile. I switched to my trusty friend flexbox. I turned the parent section into a flexible box with the child containers both taking up 50% of the width. I took out the ```left:0``` and ```right:0``` properties:

```css
section.container  {
    display: flex;
    width: 100%; 
}

div.left-half { 
    background-color: #c3a55c; 
    width: 50%;
    height: 100vh;
    overflow: hidden;
}

div.right-half { 
    background-color: #fbf591; 
    width: 50%;
    height: 100vh;
    overflow: hidden;
}
```
To make the images fill to the size of the container while keeping their aspect ration, I used:

```css
.img { 
    min-width: 100%; 
    min-height: 100%;
}
```

voila! The site is now mobile friendly! 

![Aylor Mobile](assets/aylor-mobile.png)




Me after conquering CSS media queries


![Solange dancing](https://media.giphy.com/media/hR2NxZlRDqEj6/giphy.gif)


## What's Next
- Adding more projects 
- Adding a 'last updated' bar at the bottom of the page 
- Adding Javascript elements like a scroll bar at the top that tracks the scroll progress 
- Adding my resume using Canvas to create fun elements 

## Author 
[Aylor Brown](https://aylorbrown.com)
