# Image Comparison Slider

Improved [codyhouse version](https://codyhouse.co/gem/css-jquery-image-comparison-slider/).

## Changes

  - removed unused scss,  mixins etc
  - removed bourbon dependency
  - relevant styles extracted into separate file
  - global styles changed so they  don't conflict with your page styles (for example fonts for image labels were set in body!)
  - improved  variable names ($color-1 ->  $image-comparison-slider__drag-button-color)
  - better javascript (far less cpu usage) thanks to Nazarkin Roman (https://gist.github.com/NazarkinRoman/4086b39dc6d02d25f459)
  - more (check commits for details)

##  Licence

As far as I am concerned  licence is [MIT](http://opensource.org/licenses/MIT).  
Codyhouse people have their own [terms](https://codyhouse.co/terms/).


## How to Use

### HTML

    <figure class="cd-image-container">
      <img src="img/img-original.jpg" alt="Original Image">
      <span class="cd-image-label" data-type="original">Original</span>

      <div class="cd-resize-img"> <!-- the resizable image on top -->
        <img src="img/img-modified.jpg" alt="Modified Image">
        <span class="cd-image-label" data-type="modified">Modified</span>
      </div>

      <span class="cd-handle"></span>
    </figure> <!-- cd-image-container -->

### CSS and Javascript Dependencies

You need these lines in your head:

    <link rel="stylesheet" href="css/image-comparison-slider.css">
    <script src="js/modernizr.js">
    
These lines can also go in head or immediatelly before closing body tag:

    <script src="js/jquery-2.1.1.js"></script>
    <script src="js/jquery.mobile.custom.min.js"></script>
    <script src="js/image-comparison-slider.js"></script> 



### SCSS (changing colors, fonts)

All stuff that can be easily changed is in file `scss/_image-comparison-slider__settings.scss`

You can change color of drag handle when inactive and when active (touched or clicked), color of image labels, font family & size of image label and bounce-in animation duration. 

#### How to compile SCSS

You need to have installed some variant of sass. Easiest is probably to [install ruby](https://www.ruby-lang.org/en/documentation/installation/)  and then in command line type:

    gem install sass

Now when you have sass installed all you need to do is open  command line, go to root directory of the project (using cd command) and type:

     sass --watch scss:css

This is telling sass to  watch scss folder and compile into css folder. As soon as you save any scss, css will be recompiled automatically. To stop, press CTRL+C or close command line window.
