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
In a Browser when the user opens a page, the browser starts to load the initial HTML file. It then takes the loaded HTML code and parses it which basically means that it decodes the code line by line. From this process the Browser builds the so called DOCUMENT OBJECT MODEL or DOM, which basically describes the entire web document, like a family tree, with parents, siblings and children elements. So this Document Object Model is where the entire HTML code is stored. Now as the Browser parses the HTML, it also finds, the stylesheets included in the HTML head and it starts loading them as well. And just like HTML, CSS is also parsed, but the parsing of CSS is a bit more complex. 

During the CSS parsing phase there are two mains steps: 
```Sass
    (1) - 1st Step is Resolving Conflicting CSS Declarations through a process known as a CASCADE;
    (2) - 2nd Step in the CSS parsing, is to process the final CSS Values 
                Example: converting a margin defined in percentage uinits in pixels, etc..;
```

When the 2 steps get completed, the final CSS is also stored in a tree like structure called the CSS Object Model - CSSOM, similar to the DOM. 

HTML + CSS parsed and stored, these together **form** the RENDER TREE. Now in order to render the page the Browser use something called the Visual Formatting Model. The algorithm calculates and uses a bunch of stuff like the box model, floats and postioning. 
VFO has a lot to do with the way we write our code. After VFO has done its work the Website it's finally rendered, or painted to the screen and the process is finished.




