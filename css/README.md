# CSS files

## landingPage.css
This file contains the css for the landing page.

## laptop.css
Contains the css for drawing the laptop

## variables.css
Contains the global css custom-properties. Use these properties to generate a consistent design on all the pages.

**Precaution**: landingPage.css and laptop.css contain some of the custom-properties defined in variables.css.
Before changing anything, double check if any other property gets affected.

## How to use the properties in variables.css
- The properties are defined in the :root element, so, these can be accessed anywhere.
- Theme colors are defined in rgb format. To use them, you may use any of these formats - 
```
color: rgb(var(--color_name));
```
or
```
color: rgba(var(--color_name), opacity);
```
For e.g.,
```
background-color: rgba(var(--primary-0), 0.8);
```
- Dynamic font sizes are defined in px format. These font sizes change with the change in screen width. To use them , simply use - 
```
font-size: var(--font_size);
```
For e.g.,
```
font-size: var(--h1font-size);
```
- A side margin is defined but is not used anywhere right now. That is defined for future use (if there is any need to use it).

## Formula for defining dynamic font-sizes
```
--variable: calc(<minSize>px + (<maxSize> - <minSize>) * (100vw - <minScreen>px)/(<maxScreen> - <minScreen>);
```
Here,

> minScreen = minimum Screen size that you want to consider
>
> maxScreen = maximum Screen size that you want to consider
>
> minSize = size of the element when screen size is minScreen
>
> maxSize = size of the element when screen size is maxScreen
