![](https://www.edureka.co/blog/wp-content/uploads/2019/09/CSS-Transition-1.png)

# CSS Transitions

CSS transitions allows you to change property values smoothly, over a given duration.

* `transition`
* `transition-delay`
* `transition-duration`
* `transition-property`
* `transition-timing-function`

### How to Use CSS Transitions?

To create a transition effect, you must specify two things:

* the CSS property you want to add an effect to
* the duration of the effect

**Note:** If the duration part is not specified, the transition will have no effect, because the default value is 0.

The following example shows a 100px * 100px red `<div>` element. The `<div>` element has also specified a transition effect for the width property, with a duration of 2 seconds:

```
div {
  width: 100px;
  height: 100px;
  background: red;
  transition: width 2s;
}
```

The transition effect will start when the specified CSS property (`width`) changes value.

```
div:hover {
  width: 300px;
}
```

Notice that when the cursor mouses out of the element, it will gradually change back to its original style.

![](https://daqxzxzy8xq3u.cloudfront.net/wp-content/uploads/2019/07/15114208/css-transition-illustration.jpg)
### Change Several Property Values
The following example adds a transition effect for both the width and height property, with a duration of 2 seconds for the width and 4 seconds for the height:

```
div {
  transition: width 2s, height 4s;
}
```

### Specify the Speed Curve of the Transition
The `transition-timing-function` property specifies the speed curve of the transition effect.

* `ease` - specifies a transition effect with a slow start, then fast, then end slowly (this is default)
* `linear` - specifies a transition effect with the same speed from start to end
* `ease-in` - specifies a transition effect with a slow start
* `ease-out` - specifies a transition effect with a slow end
* `ease-in-out` - specifies a transition effect with a slow start and end
* `cubic-bezier(n,n,n,n)` - lets you define your own values in a cubic-bezier function


Example
```
#div1 {transition-timing-function: linear;}
#div2 {transition-timing-function: ease;}
#div3 {transition-timing-function: ease-in;}
#div4 {transition-timing-function: ease-out;}
#div5 {transition-timing-function: ease-in-out;}
```

![](https://cdn.lynda.com/course/674608/674608-637199642299923950-16x9.jpg)
### Delay the Transition Effect
The `transition-delay` property specifies a delay (in seconds) for the transition effect.

```
div {
  transition-delay: 1s;
}
```


![](https://miro.medium.com/max/1400/1*spiB7DFGUs_-2HOo589Eug.png)

# CSS3 Transforms

Transforms allow us to move or change the appearance of an element on a 2D plane

There are four different types of transforms: `Rotate`, `Skew`, `Scale` and `Translate`

## Rotate
The rotate transform rotates an element clockwise or counterclockwise by a specified number of degrees (deg). A positive value (90deg) will rotate the element clockwise and a negative value (-100deg) will rotate the element counterclockwise.

![](https://www.vanseodesign.com/blog/wp-content/uploads/2011/11/transform.png)

```
element {
  transition: transform 1s ease-in-out;
}
element:hover {
  transform: rotate(90deg);
  transform: rotate(-30deg);
}
```

## Skew
The skew transform tilts an element based on values provided on the X and Y axes. A positive X value tilts the element left, while a negative X value tilts it right. A positive Y value tilts the element down, and a negative Y value tilts it up. If an axis isn’t specified and only skew is stated then that is equivalent to skewX. Also you can include both X and Y axes to tilt the element’s angles.

![](https://www.sanjaywebdesigner.com/articles/wp-content/uploads/2019/07/transform-skew-html-css-in-delhi-india.jpg)
```
element {
  transition: transform 0.3s ease;
}
element:hover {
  transform: skew(90deg); 
  transform: skewX(90deg);
  transform: skewY(-50deg);
  transform: skew(90deg, -50deg);
}
```

## Scale
The scale transform increases or decreases the size of an element. A number larger than 1 will increase the size of the element and a decimal less than 1 will decrease the size of the element. For example, 2 would make the element twice its original size, whereas 0.5 would make the element half its original size. The size of an element can be scaled by the X-axis, Y-axis or both. The shorthand scale() will effect both axes at the same time.

![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/74953e3d-618f-4225-97e0-cec2d97f8764/transform-scale.png)

```
element {
  transition: transform 1s ease;
}
element:hover {
  transform: scaleX(0.5);
  transform: scaleY(2);
  transform: scale(0.5);
  transform: scale(0.5, 2);
}
```

## Translate
The translate transform moves an element right, left, up or down. A positive X value moves the element to the right and a negative X value moves the element to the left. A positive Y value moves the element downwards and a negative Y value moves the element upwards.

![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/487ec0ca-416c-42dc-bb8d-bda2da819e84/transform-translate.png)

```
element {
  transition: transform 0.5s linear;
}
element:hover {
  transform: translateX(15px);
  transform: translateY(50px);
  transform: translate(15px, -40px);
}
```
