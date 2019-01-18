# CSS Secrets: Better Solutions to Everyday Web Design

This respository cotains solutions and explanations with details about advanced concepts in CSS3. 

## What are the 3 main Principles of writing a good HTML and CSS code, in order to build amazing websites? 

```Sass
    (1) - Responsive Design;
    (2) - Maintanable and scalable code;
    (3) - Web Performance; 
 ```  

### 1. Responsive Design
It means we build websites that work and render correctly across all screen sizes on all devices. A responsive design includes: 
- Fluid layouts
- Media Querries
- Responsive Images
- Correct Units
- Desktop-firs vs mobile-first strategy

### 2. Maintanable and scalable code
Writing maaintanable and scalable code means to write code that is CLEAN, easy to understand, supports future growth and above all is REUSABLE. In order to write maintanable and scalable code we need to think about our CSS Arhitecture, how to organize organize our files, how to name our classes and how to structure our HTML markup.
- CLEAN
- Easy to Understand
- Reusable
- Growth
- How to Organize Files
- How to Name classes
- How to structure HTML
 
### 3. Web Performance
Last but not least is the Web Performance, making an Website or App more performant means to make it faster and smaller in size, so that the user downloads less data. Now there are many factors which might affect performance and some of them have nothing to do with our code, but some of the things we can do is to make as little HTTP requests as possible, write as less code, compress our code and use a preprocessor as SASS. The biggest impact that we can have on performance is to actually reduce the use of images, because images are what makes up by far the biggest part of the size of a website. We can do so by using only images that are really necessary for a website or app and also by compressing them so that we use less bandwidth for the final user. 
- Less HTTP Requests
- Less Code
- Compress Code
- Use a CSS Preprocessor
- Less images
- Compress images
        
## How CSS works behind the scenes? 
When the user opens a page, the browser starts to load the initial HTML file. It then takes the loaded HTML code and parses it which basically means that it decodes the code line by line. From this process the Browser builds the so called DOCUMENT OBJECT MODEL or DOM, which basically describes the entire web document, like a family tree, with parents, siblings and children elements. Document Object Model is where the entire HTML code is stored. As the Browser parses the HTML, it also finds, the stylesheets included in the HTML head and it starts loading them as well. And just like HTML, CSS is also parsed, but the parsing of CSS is a bit more complex. 

During the CSS parsing phase there are two mains steps: 
```Sass
    (1) - 1st Step is Resolving Conflicting CSS Declarations through a process known as a CASCADE;
    (2) - 2nd Step in the CSS parsing, is to process the final CSS Values 
                Example: converting a margin defined in percentage uinits in pixels, etc..;
```

When the 2 steps get completed, the final CSS is also stored in a tree like structure called the CSS Object Model - CSSOM, similar to the DOM. 

HTML + CSS parsed and stored, **form** together the RENDER TREE. Now in order to render the page the Browser use something called the Visual Formatting Model. The algorithm calculates and uses a bunch of stuff like the box model, floats and postioning. 
VFO has a lot to do with the way we write our code. After VFO has done its work the Website it's finally rendered, or painted to the screen and the process is completed.

## CSS parsing Phase - Quick Review - CSS Terminology
A Css Rule consist of a Selector and a Declaration Block: 

<p align="center">
   <img src="https://www.tutorialchip.com/wp-content/uploads/2010/12/CSS-Rules-Part1.jpg">
</p>



## The Anatomy of 'C' in CSS - CASCADE and SPECIFICTY what you need to know:
  - Cascade is the process of combining different style sheets and resolving conflicts between different CSS rules and declarations, when more than one rule applies to a certain element. A declaration for a certain style property like font size, can appear in several stylesheets and also several times inside one single style sheet. Css can come from different sources. The declarations that we put in our stylesheets are divided in 3 main categories: 
	- Author declarations;
	- User declarations, CSS coming from the user(e.g. user changes the CSS in the Browser).
	- Browser(user agent) declarations - for instance if we use an anchor tag or link and we don't syle it at all it is usually rendered with blue text and underline, called the user agent CSS because it is set by the browser. 

So in the end, Cascade combines the CSS declarations coming from all these different sources 
But how does Cascade resolve all the conflicts when more than one rule applies? - Well what it does is to looks at:

	IMPORTANCE(WEIGHT) > SPECIFICITY > SOURCE ORDER

in order to determine which one takes precedence. First the Cascade starts by giving the conflicting declarations different importance's based on where they are declared, so based on their source. The most important declarations are user declarations marked with the keywork !important. 


## BEST PRACTICE RULES:
- CSS declarations marked with !important have the highest priority;
- Use !important as a last resource. It's better to use correct specificities, essential for  **maintanable** Code;
- Inline Styles will always have priority over styles in external style sheets;
- A selector that contains **1** ID is more specific than one with 1000 Classes;
- A selector that contains **1** CLASS is more specific than one with 1000 Elements;
- The universal selector * has **no** specificity value **(0, 0, 0, 0)**, which means that all other selectors has a precedence over it;
- As a Good practice is better to rely on **specificity** than on the **order** of selectors;
- Rely on **order** when using 3rd-party stylesheets - always put your author style sheets last;


### How are Values processed in the CSS parsing phase?
Each CSS property have something called the "initial value", which is simply the value used if there is no cascaded value. So basically if we do not declare a value and if neither the Browser nor the user define a value, then the inital value will be used; Different properties have different initial values (e.g. padding has a inital value of 0 px); For font-size the Browser has a default value of 16px; so this will be the default inital value for all elements; if there is a font-size declaration for another element in rem(relative unit) - like p { font-size: 1.5rem } - this value will be converted by the engine into px - 24px( 1.5 * 16px) - the rem unit is always relative to the root font size;
Some properties in CSS inherit the computed value of their parent elements; 


### How the CSS Engine Converts UNITS from Relative to Absolute(PX):  
- Relative UNITS are FUNDAMENTAL to build modern responsive layouts;
- Each CSS property has a initial value, used if nothing is declared ( and if there is no inheritance);
- Browsers specify a **ROOT** font-size for each page(usually 16px);
- Percentanges and relative values are always converted to pixels in order for CSS Engine to be able to render the page on the screen;
- Percentages are measured relative to their parent's font-size, if used to specify font-size;
- Percentages are measured relative to their parent's width, if used to specify lengths;
- **em** are measured relative to their parent font-size, if used to specify font-size;
- **em** are measured relative to the current font-size, if used to specify lengths;
- **rem** are always measured relative to the document's root font-size;
- **vh** and **vw** are simply percentage neasyrenebts of the viewport's height abd width;

