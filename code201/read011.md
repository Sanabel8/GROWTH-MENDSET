HTML
chapter16
Controlling sizes of images in CSS

* controll height and width like:

```img.large { 
width: 500px; 
height: 500px;}
```
* we added small medium large as atribute in the code html of img.
* ALIGNING IMAGES USING CSS first make aclass in the html =align-left then make css example:
```img.align-left {
float: left;
margin-right: 10px;}
```
* Centering images Using CSS
. In order to center an image, it should be turned into a blocklevel element using the display property with a value of block.  

example:
```img.align-center { 
display: block; 
margin: 0px auto;} 
```
* Background Image
like
```body {
background-image: url("images/pattern.gif");}
```
* Repeating Images
background-repeat have 4 values:
1.repeat 
2.repeat-x
3.repeat-y
4.no-repeat:. fixed . scroll
example:
```body {
background-image: url("images/tulip.gif");
background-repeat: no-repeat;
background-attachment: fixed;}
```
* Background Position when the image is not repeated we cnn use position , it have two values 
* shorthand background
1: background-color
2: background-image
3: background-repeat
4: background-attachment
5: background-position

```div {
 background:
 url(example-1.jpg)
 top left no-repeat,
 url(example-2.jpg) 
 bottom left no-repeat, 
 url(example-3.jpg) 
 centre top repeat-x;}
```
chapter19
* Search Engine Optimization (SEO)
* SEO is often split into two areas: on-page techniques and off-page techniques.
* Search engine optimization helps visitors find your sites when using search engines.
* In every page of your website there are seven key places where keywords (the words people might search on to find your site):
1: Page Title
2: URL / Web Address
3: Headings
4: Text
5: Link Text
6: Image Alt Text
7: Page Descriptions
* How to Identify Keywords and Phrases
1: Brainstorm
2: Organize
3: Research
4: Compare
5: Refine
6: Map
 
 
* The video and audio elements allow us to embed video and audio into web pages. As we showed in Video and audio content, a typical implementation looks like this:
```<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
</video>
```
* in css 
example:
```.controls {
  visibility: hidden;
  opacity: 0.5;
  width: 400px;
  border-radius: 10px;
  position: absolute;
  bottom: 20px;
  left: 50%;
  margin-left: -200px;
  background-color: black;
  box-shadow: 3px 3px 5px black;
  transition: 1s all;
  display: flex;
}
```




















































