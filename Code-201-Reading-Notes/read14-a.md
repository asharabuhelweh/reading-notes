# **CSS**

# Transforms
1. **2D Transforms**

  * 2D rotate ,2D Scale,2D Translate 

  ```
  html>>>> <figure class="box-1">Box 1</figure>
  css>>>>>
   .box-1 { 
       transform: rotate(20deg);
       transform: scale(.75);
       transform: translateX(-10px);

       }

  ```

   and we can specify the scale for x ,y


   * and you can control the skew by `transform: skewX(5deg);` ,combining transform ,transform origin 
   `.box-1 {transform: rotate(15deg); transform-origin: 0 0;}` and Perspective
    `.box { transform: perspective(200px) rotate(45deg);}` you control for it's  depth and origin Value .


2. **3D Transforms**

it workes as  the same elements of 2D and in the same way but we have to give it value for z-axis dimensional and in addition in transform style On occasion three-dimensional transforms will be applied on an element that is nested within a parent element which is also being transformed and Backface Visibility

 ```
 <div class="rotate three-d">
<figure class="box">Box 1</figure>
css>>>>>>>>>
.rotate {
  transform: perspective(200px) rotateY(45deg);
   }
.three-d {
  transform-style: preserve-3d;
 }
 backface-visibility: hidden;
 ```


# Transitions

There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay
1. The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties
2. The duration in which a transition takes place is set using the transition-duration property
3. The transition-timing-function property is used to set the speed in which a transition will move
4.  The delay sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executin

```
.box {
  background: #2db34a;
  border-radius: 6px
  transition-property: background, border-radius;
  transition-duration: .2s, 1s;
  transition-timing-function: linear, ease-in;
  transition-delay: 0s, 1s;
}
.box:hover {
  background: #ff7b29;
  border-radius: 50%;
}

```


*  there is a shorthand property, `transition`, capable of supporting all of these different properties and values. Using the transition value alone, you can set every transition value in the order of transition-property, transition-duration, transition-timing-function, and lastly transition-delay ` transition: background .2s linear, border-radius 1s ease-in 1s`

# Animations

1. To set multiple points at which an element should undergo a transition, use the `@keyframes` rule
2. animations behave similarly to transitions. They include a duration, timing function, and delay if desired
3. On top of being able to set the number of times an animation repeats, you may also declare the direction an animation completes using the animation-direction property. Values for the animation-direction property include normal, reverse, alternate, and alternate-reverse
4. The animation-play-state property allows an animation to be played or paused using the running and paused keyword values respectivel
5. The animation-fill-mode property identifies how an element should be styled either before, after, or before and after an animation is run


```
.stage:hover .ball {
  animation-name: slide;
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-delay: .5s;
  animation-fill-mode: forwards;
}
.stage:active .ball {
  animation-play-state: paused;
}

```


* shorthand animation can be written out in a shorthand format. This is accomplished with one `animation` property, rather than multiple declarations. The order of values within the animation property should be animation-name, animation-duration, animation-timing-function, animation-delay, animation-iteration-count, animation-direction, animation-fill-mode, and lastly animation-play-state

`  animation: slide 2s ease-in-out .5s infinite alternate;`


1. Fade in `.fade{opacity:0.5;}  .fade:hover{opacity:1;}` 
2. Change color ` .color:hover{background:#53a7ea;} `
3. Grow & Shrink ` .grow:hover{-webkit-transform: scale(1.3);  -ms-transform: scale(1.3); transform: scale(1.3); }`
4. Square to circle `.circle:hover { border-radius:50%;}`
5. and others button style like  3D shadow , Swing, Inset border







