# READ 03

## Responisve Web Design

- the practice of building a website suitable to work on every device and every screen size.

- responsive design: continually and fluidly change based on different factors, such and viewport width. the favored design method.

- adaptive websites: are built to a group of preset factores. 

### flexible Layouts

- The practice of building the layout of a website with flexible grid, capable of dynamically resizing to any with.

- built with relative lengths: vw, vh, vmin, vmax.

- dont use fixed measurement units.

***target % context = result***
ex. 1.858736059%; /*  10px ÷ 538px = .018587361 */

### MEDIA QUERIES

- Media queries provide the ability to specify different styles for individual browser and device circumstance.

#### Initializing media queries

- it is recommend to use the @media rule inside of an existing style sheet to avoid any additional HTTP requests.

- media types include: all, screen, print, tv, and braille.

- logical operators in media queries: *and, not, only*

- and allows and extra condition to be added

- not negates the query, specifying any query but the one identified.

- only hides the styles from devices and browsers that don't support media queries. 

### MOBILE FIRST

- using styles targeted at smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows.

### FLEXIBLE MEDIA

- One quick way to make media scalable is by using the max-width property with a value of 100%. Doing so ensures that as the viewport gets smaller any media will scale down according to its containers width.


## FLOATS

- Floated elements remain a part of the flow of the web page. 

- There are four valid values for the float property. Left and Right float elements those directions respectively. None (the default) ensures the element will not float and Inherit which will assume the float value from that elements parent element.

- **clear** has four valid values as well. Both is most commonly used, which clears floats coming from either direction. Left and Right can be used to only clear the float from one direction respectively. None is the default, which is typically unnecessary unless removing a clear value from a cascade.
