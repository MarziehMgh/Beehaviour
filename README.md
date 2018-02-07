# Beehaviour
![headerbee.gif](headerbee.gif)

A project made by

- Francesca Binda
- Valentina Caiola
- Margherita Motta

During the Creative Coding course at Politecnico di Milano

## 1.Idea

### Bees...behaviour
The honey bee dance language is a dance through which bees communicate with each other about where the food sources are. It is considered by many as one of the most intriguing communication systems in the animal world. This natural phenomenon is not widely known, but it is very interesting since it is based on precise rules. Bees perform different types of dance depending on the distance of the food from the hive. The dances analyzed in our project are round dance, sickle dance and waggle dance.

In our project, the user has to choose a food source by clicking on it. This action will allow the user to learn information about that specific food source. Furthermore, depending on the position of the latter, the user will be asked to perform one of the three dances mentioned above. 


## 2.Development and libraries

Our project is designed to be used only on computers, in particular it can only be used in full screen. We mostly used Javascript with p5.js to code. The library that allowed us to create animations is p5.play.js, created by Paolo Pedercini.


## 3.Problems & Solutions

### Performances

Problem: At first, we created a few but very complex functions that were enough to perform the tasks that we needed, but the code was very slow.

Solution: We created much many functions that perform much smaller tasks, and this makes the code less heavy and much more fast.


### Modal window

Problem: 
At the beggining, we found it difficoult to use a modal on top of the current page, so we initially thought of making more than one page.

Solution: 
We created a boolean called isModalActive and a variable called modalStatus. By performing different actions, like clicking on a pollen sources, the value of the modalStatus variable changes. We then created if and else conditions that calls different function depending on the modalStatus. These functions actually describe the way in which objects must be displayed

```function draw(){
   if (isModalActive()) {
        drawOverlay();
        if (modalStatus == 0) {
            drawModal0();
            buttondance.display();
            buttonclose.display();
        } else if (modalStatus == 1) {
            drawModal1();
            buttonclose.display();
        } else if (modalStatus == 2) {
            drawModal2();
            buttonclose.display();
        }
     }
   }
    
// 
    function drawModal1() {
    plants[activePlantIndex].showModal1();
    if (plants[activePlantIndex].showPoints) {
        drawPoints();
    }
}
```


### Use of the draw

Problem: 
We had to find a way to use the draw function in a smart way. We understood that we tended to put everything that we needed in the draw, but that made it a really complex and unreadable function.

Solution: 
We used the draw in the easiest way possible. We only used to draw to call a variety of other display functions, which are separated one from the other to make the more eady to read.

### Click indicator

Problem: 
We had to find a way to make it clear to the user that he could only click on certain kinds of trees and flowers, but we also wanted the user to "explore" the landscape without knowing by the start we to look at.

Solution: 
We decided that to understand where to click, the user had to move the mouse around. We thought that a function that makes the clickable object bigger by moving the mouse over it was a simple but effective way to suggest where to click without ruining the visualization of the landscape. 




