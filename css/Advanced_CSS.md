## **Advanced CSS Topics**  

### **Shadows** 

#### π π³οΈ **Box Shadows**

**`box-shadow`** is the standard CSS **property** to get you going and it can have a value comprising several parts as shown in the example below

```css
box-shadow: 5px 5px 3px 1px #999
``` 

- **The first value is the horizontal offset**
     => how far the shadow is nudged to the right (or left if itβs negative)

- **The second value is the vertical offset**
    =>  how far the shadow is nudged downwards (or upwards if itβs negative)

- **The third value is the blur radius**
    => the higher the value the less sharp the shadow. (β0β being absolutely sharp). This is optional β omitting it is equivalent of setting β0β.

- **The fourth value is the spread distance.** 
     => the higher the value, the larger the shadow (β0β being the inherited size of the box). This is also optional β omitting it is equivalent of setting β0β.

- **The fifth value is a color.** Thatβs optional, too.


####  **Inner shadows**

 - You can also apply shadows to the inside of a box by adding βinsetβ to the list.

 
 ```css
 box-shadow: inset 0 0 7px 5px #ddd;
 ```

#### **Text Shadows**

- `box-shadow`, as its name implies, only has eyes for boxes. Fickle beast. But you can also apply shadows to the outline of text with (surprise!) **`text-shadow`**.

 ```css
 text-shadow: -2px 2px 2px #999;
 ```

**Similarly to box-shadow:**

- The first value is the horizontal offset
- The second value is the vertical offset
- The third value is the blur radius (optional)
- The fourth value is the color (optional, although omitting this will make the shadow the same color as the text itself)
  
### **Media Queries**

**`@media`** π at-rules are used to target styles at specific media, such as **screen** or **print**  etc.

**Example:**

```css
@media screen {

    body { font: 12px arial, sans-serif }
    #nav { display: block }

}

``` 


**You can also add `browser-size` specific media queries** 

**Example:**

```css
@media screen and (max-width: 1000px) {

    #content { width: 100% }

}
``` 

**You can also add device-specific media queries.** 

**Example:** 

```css
@media screen and (min-device-height: 768px) and (max-device-width: 1024px) {

    /* You can apply numerous conditions separated by "and" */

} 
```

