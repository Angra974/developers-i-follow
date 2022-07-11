---
author: "Ritika Agrawal"
handle: "@RitikaAgrawal08"
source: "https://twitter.com/RitikaAgrawal08/status/1526669231278141440"
date: "May 18, 2022 1:01 AM"
likes: 50
retweets: 4
replies: 9
---
![RitikaAgrawal08](https://pbs.twimg.com/profile_images/1536045260253515776/BNiSS_c1_normal.jpg)
Ritika Agrawal ([@RitikaAgrawal08](https://twitter.com/RitikaAgrawal08)) - May 18, 2022 1:01 AM

🔸Let's make an Item Quantity Counter in 8 Simple Steps using CSS and JS🔸

A Thread🧵⬇️ [pic.twitter.com/cLb1TAcI47](https://twitter.com/RitikaAgrawal08/status/1526669231278141440/video/1)

1. HTML Structure
I've a container div which has 2 <i> tags for font awesome icons - plus and minus & a div with class "itemCount" which initially has value 1 

⬇️ [pic.twitter.com/wldiv59E77](https://twitter.com/RitikaAgrawal08/status/1526669237594767360/photo/1)

![3_1526645748276035584](https://pbs.twimg.com/media/FS-8ODPagAAHndO.jpg)

2. Styling container
▪️Initially container is just a blue circle for which I've used below👇 CSS properties.

▪️transition is added because using JS I'm adding a class to container which increases its width. 

▪️So transition property will increase width smoothly

⬇️ [pic.twitter.com/zYEWwhgj2R](https://twitter.com/RitikaAgrawal08/status/1526669242762133505/photo/1)

![3_1526646490718162944](https://pbs.twimg.com/media/FS-85RDaUAAuEIS.jpg)

3. Styling icons & itemCount div
▪️These are the CSS properties used👇

▪️grid is used to center the icons & number inside these div tags

▪️itemCount is initially hidden via visibility property

⬇️ [pic.twitter.com/DaQoGvXlM3](https://twitter.com/RitikaAgrawal08/status/1526669248864866304/photo/1)

![3_1526647078960922624](https://pbs.twimg.com/media/FS-9bgbagAASKPb.jpg)

4. Adding expand class
▪️To get desired styling when container is clicked I am using below👇 CSS Properties
▪️expand class will be added to container via JS & using descendant selector I've joined icons & itemCount to add properties on them when container is clicked

⬇️ [pic.twitter.com/HNaib1Ltnj](https://twitter.com/RitikaAgrawal08/status/1526669254493601792/photo/1)

![3_1526648232147058688](https://pbs.twimg.com/media/FS--eoYagAArnJE.jpg)

5. Adding JS
▪️using getElementById I've selected "container" div with Id "counter" , "itemCount" div with Id "itemQuantity" & both icons

▪️I've added a click event listener on container div to
    - add expand class to container
    - add click events to both icons

⬇️ [pic.twitter.com/ohIioTQZTg](https://twitter.com/RitikaAgrawal08/status/1526669259983978496/photo/1)

![3_1526649264654684160](https://pbs.twimg.com/media/FS-_auxakAARQBE.jpg)

6. These 2 functions are attached to click events on icons -> 
   - plusIcon uses incrementQuantity
   - minusIcon uses decrementQuantity

▪️quantity variable takes in value of itemCount div, increments or decrements it by 1 then with innerHTML on itemCount it is displayed

⬇️ [pic.twitter.com/E40cic1AJV](https://twitter.com/RitikaAgrawal08/status/1526669265927294976/photo/1)

![3_1526655102949670912](https://pbs.twimg.com/media/FS_EukHaQAAWSu5.jpg)

Understanding stopPropagation()
▪️ JS handles nested events in 2 phases - capturing & bubbling

Suppose we've button inside div & both have a click event attached & then we click on button

▪️with capturing, event on div(parent) is executed 1st & then event on button(child)

⬇️

▪️with bubbling, event on button will execute first & then will div tag event
▪️capturing executes events starting from parent then goes to its children elements
▪️bubbling executes from child and goes upto to parents

bubbling phase is the default that browsers use

⬇️

In our code I've a click event on both icons & container

▪️container click event adds expand class to it

▪️with click event on minusIcon I not only want to decrement item count but also remove expand class from container when count is 0

⬇️

▪️But If I click on minusIcon when count is 0 it will remove expand class but click event on container will execute too and thus add the class back 

▪️to solve this, we are using event.stopPropagation() to stop the events from bubbling upwards

⬇️

7 Adding animation on itemCount
▪️to get that effect when number changes I'm using ::before class of itemCount div

CSS properties used are👇

⬇️ [pic.twitter.com/8unGsMRIeZ](https://twitter.com/RitikaAgrawal08/status/1526669279470690304/photo/1)

![3_1526667291165077504](https://pbs.twimg.com/media/FS_P0AwaMAABGUI.jpg)

8. Adding animateCount() 

▪️this is the function I am calling in both incrementQuantity() & decrementQuantity() functions with required parameters to add or replace the CSS classes mentioned in previous tweet

⬇️ [pic.twitter.com/43jyBTmZ1r](https://twitter.com/RitikaAgrawal08/status/1526669284474503168/photo/1)

![3_1526667552692523008](https://pbs.twimg.com/media/FS_QDPBaUAAAyr2.jpg)

That's it our Item Quantity Counter is ready!!

🔸Thank you for reading!!🔸

[@CodePen](https://twitter.com/CodePen) - [codepen.io/RitikaAgrawal0…](https://codepen.io/RitikaAgrawal08/full/RwQpjWj)

[Thread link](https://twitter.com/RitikaAgrawal08/status/1526669231278141440)