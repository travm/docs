# CSS
## Naming Convention
Our CSS will use hyphen-separation for all selectors. Please note that this only applies when names extend beyond a single word. It is not a requirement that all selectors have a two word minimum.

```css
#longer-name {}
#name {}
.longer-name {}
.name {}
```

## Code Organization
To improve maintainability and efficiency we will be implementing an object-oriented code structure for our CSS that is borrowed heavily by the ideas from [SmaCSS](http://smacss.com/). This will create a consistency and expectation for other team members when viewing your code.

### Base
Base styles are global defaults that will be used throughout the stylesheet to define how basic HTML elements look by default. This can be used along side [Normalize](http://necolas.github.io/normalize.css/) to set external defaults and then override those to your liking within your project.

Note: There are some varying opinions on how Normalize should be used. Some are in favor of using an external file, and others are not. To be clear: there is __nothing__ wrong with either preference. I prefer using Normalize as an external file in favor of keeping my stylesheet clean. Normalize and my project files are concatenated into a single file at build time and I simply override any Normalize defaults with my own in my stylesheet.  

### Layouts
Layouts separate and hold modules together to form pages. They are used to control and measure the widths of our main layout columns. 

Note: Not to be confused with a grid system which is a more standardized manner of organizing a layout. 

### Modules
Modules are modular elements that make up all of the content that can be reused throughout the design. This will more than likely make up a majority of your design and code. Remember, the key is to make our styles as reusable as possible!

### Modifiers
Modifiers change the look or behavior of an element or module. For example, when a user completes a form and it fails validation we can append a modifier class to change the input to a c class with a red background color.

Organizing your code into these sections with modularity in mind will help establish a consistency when viewing fellow team member’s code. This will allow us to stay DRY (Don’t Repeat Yourself) and efficient.

## Code Formatting
Readability is an important factor when considering maintainability and efficiency. There is an endless debate on whether single-line or multi-line code formatting is more readable. However, much of it is up to personal preference. To get the best of both worlds, use a mixture of single-line and multi-line code formatting. 

Each selector should start as a single-line until the style grows too large and becomes unwieldy. Once this happens, the selector should be broken into a multi-line format. This will keep a CSS readable while saving on horizontal space where possible.

## Property Ordering
Having a consistent order to our CSS properties is very important to maintainability. As you write CSS make sure to group your properties first by their type followed next by alphabetical ordering where it makes sense. For example: font, box model, positioning, text, etc. 

Here is an example of this ordering:
 
1. Font
  1. color
  2. font-family
  3. font-size
  4. line-height
  5. text-align

 2.  Display/Box Model
	1. width
	2. height
	3. margin
	4. padding
	5. background
	6. border
	7. box-sizing
	8. display
	9. overflow

3. Position
	1. position
  2. top, right, left, bottom
  3. z-index

4. Other
	1. cursor

## Pre-processing
It is my personal preference to stay as pure to the languages as possible. For a long time, there was no solid alternative to tools such as Sass or Less. However, now we have forward thinking pre-processors like [Myth](http://myth.io “Myth.io Website”) that act more like polyfills for proposed CSS specs that will be included in the future.

## Grids
Grids, while not necessary, can often be very useful tools for quickly designing layouts and keeping them consistent throughout a project.


