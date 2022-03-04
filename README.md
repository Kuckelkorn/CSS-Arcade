# CSS Arcade machine

assignment for the course CSS to the rescue.

**When using this application make sure that you are using Safari Technology Preview. If it has been a while look here for the status of the implementation of `:has()`
[mdn browser compatibility](https://developer.mozilla.org/en-US/docs/Web/CSS/:has#browser_compatibility)**

## Week 1

This week we had to choose what our final assignment would look like. I've chosen to create my own arcade machine with a top down view. The challenges for this assignment for me are working the selectors and making different selectors impact a different part of the site.

### Inspiration

![Arcade Machine](./assets/arcade.jpg)
![Hud Elements](./assets/hud.jpeg)

## Week 2

### Wednesday 16th of February

Today I started working with a simple layout of the site and started working with the new CSS :has pseudo selector. I was able to make a section change colour independently from the selected checkbox. Even managed to have two different checkboxes in different forms have an impact on the same section. The only struggle right now is to have 3 checkboxes have an impact on the section.

### Thursday 17th of February

Styled my checkboxes, added a slider in the footer. I also was able to have multiple checkboxes have an impact on the section in the middle. The next steps are to improve the styling and actually have different scenes displaying in the middle instead of just changing the colour.

![Final design after week 2](./assets/week2.png)

## Week 3

### Wednesdag 2nd of March

Today I had to fix an issue with the way `:has()` is written, previously I was able to chain multiple `:has()`'s like this:

```css
main:has(form:first-child:has(input:first-child:checked) ~ form:last-child:has(input:first-child:checked)) section {
  background-color: darksalmon;
}
```

unfortunately when I returned to work this week this way of writing no longer works after hours of searching and asking for help I found this article on [CSS tricks](https://css-tricks.com/the-css-has-selector/) that displayed a different way of chaining.

```css
main:has(form:first-child input:nth-child(2):checked):has(form:last-child input:last-child:checked) section div:nth-child(3){
  display: none;
}
```

I also was able to make the slider working with the code provided by the lecturers.

### Thursday 3rd of March

Today I started working on more screens I could display when pressing multiple buttons and cleaned up some code for future convenience. So I included some divs that I could hide and show when a combination of checkboxes are checked and left unchecked.

And made two kind of animations, one is displayed on default and the other is being shown when a combination of checkboxes are checked.
