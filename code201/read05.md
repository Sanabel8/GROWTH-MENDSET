```
html
chapter 5
* Images should...
  Be relevant
  Convey information
  Convey the right mood 
  Be instantly recognisable 
  Fit the color palette
* when you build site It's better to have image folder to store your images .
* images folder can contain subfolders (news, products ,interface).
* to add image we will use <img src ="link of image" alt="text description for image" title= "more ifo for pic"/>.
* to add hight and width for image <img src ="link of image" alt="text description for image" hight="600" width="200"/>.
* Where to Place Images in Your Code:1. before a paragraph
                                    2. inside the start of a paragraph
                                    3. in the middle of a paragraph
* align attribute : left , right.
* align vertically : top ,middle , bottom.
* Three Rules for Creating Images:1. save image in (jpeg ,git ,png )format.
                                  2. You should save the image at the same width and height it will appear on the website
                                  3. Use the correct resolution
* Tools to Edit & Save Images:. adobe photoshop (It is expensive)
                              . Adobe Fireworks 
                              . Pixelmator
                              . PaintShop Pro
                              . Paint.net
* Image Formats: JPEG

* Images created for the web should be saved at a resolution of 72 ppi
* The higher the resolution of the image, the larger the size of the file.
* <figure> :to contain image 
* <figcaption> : to add acaption to an image.
example:
<figure>
    <img src="images/otters.jpg" alt="Photograph of  two sea otters floating in water">
    <br />
    <figcaption>Sea otters hold hands when they sleep so they don't drift away from each 
                other.</figcaption>
</figure>

chapter11
color

to determine the color in css:

1.RGB value :HOW MUCH RED, GREEN and BLUE 
like  rgb (100,100,90)   from (0 to 225)

2.HEX code :These are six-digit codes that 
represent the amount of red, 
green and blue in a color
like  color:#ee3e80;

3.COLOR NAMES :from browser like color: DarkCyan; 


background color
in the body element choose background-color in the same three methode

every pixle on my screen is amix of red ,green and blue.




opacity (alpha value):
property which allows you to specify the opacity of an element from (0.0 -1.0)

hue:color circle from(0-360)

saturation: ia amount of gray in the color , 100%  is full saturation and 0% is shsde of gray.

lightness: the amount of black or white in the color .

hs1 color property allows you to specify color properties using hue, saturation, and 
lightnes


chapter 12
* Typeface Terminology: Serif , Sans-Serif ,Monospace
* the font weight :to emphasis the amount of white space (Light ,Medium ,Bold ,Black).
* font styles :(Normal ,Italic ,Oblique).
* Choosing a Typeface for your Website: Serif,Sans-Serif ,Monospace ,Cursive ,Fantasy)
for example, if you wanted serif type, you could write the following:
font-family: Georgia, Times, serif ,"Courier New";
* If a font name is made up of more than one word, it should be put in double quotes.

* SIZE OF TYPE: .font-size(pixels ,% , ems)
* font-weight : normal ,blod
* font-style: normal ,italic ,oblique
* text-transform :uppercase ,lowercase ,capitalize
* text-decoration : none ,undreline overline ,blink ,line-through
* text-align :( left , right , center , justify)
* pseudo-elements :first-letter, :first-line
Attribute Selectors
- Existence []    p[class]
- Equality  [=]   p[class="dog"]
- space     [~=]  p[class~="dog"] 
- Prefix    [^=]  p[attr^"d"]
- SubString [^=]  p[attr*"do"]
- Suffix    [$=]  p[attr$"g"]


JPEG vs PNG vs GIF

* use JPEG format :contain a natural scene or photograph where variation in colour and intensity is smooth.
* use PNG format : needs transparency or for images with text & objects with sharp contrast edges like logos.
* Use GIF format : for images that contain animations.
* compression :reduce the size of data and ensure faster transmission.
* types of compression (lossless and lossy).
* JPEG :  is a lossy compression , achieve compression ratios of 1:10 without perception , best suited for photographs and paintings of natural scenes, don’t support transparency .
* PNG is a lossless image format ,a great choice for images with text, logos and shapes with sharp edges ,  support transparency .
* GIF is also a lossless image format , mainly used only if the image contains animations,   support transparency .

```