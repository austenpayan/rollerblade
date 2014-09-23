rollerblade
===========

####A jQuery plugin for creating an interactive 360º image rotator.

###[Demo](http://www.iamapioneer.com/plugins/rollerblade)

With Rollerblade, you can easily give your webpage visitors a great 360º viewing experience with your product, images, or anything else you can think of.

##The Setup.
First, include rollerblade.css at the top of your page with your CSS. Or, since the contents of that file are so small, simply copy and paste the rollerblade.css contents into your main CSS file.

Next: Rollerblade targets a container element with an image element inside that has the class of "rollerblade-img". Make the src of the image the path to the first image in your rotator.
```html

<div id="target">
  <img class="rollerblade-img" src="path/to/first/image.jpg">
</div>

```

##Initiate.
Make sure jQuery is included in your page, and then select the container element and call the rollerblade method. At the very minimum, you have to pass in an array of image urls as a property of the options object. The property must be called 'imageArray'.

```javascript
  
  $(document).ready(function(){
  
    // You can specify an array of images outside of the rollerblade method,
    // and then pass it in, as so:
    
    var arrayOfImages = [
      'path/to/image/1.jpg',
      'path/to/image/2.jpg',
      'path/to/image/3.jpg',
      'path/to/image/4.jpg',
      'and/so/on.jpg'
    ]
    
    $("#target").rollerblade({imageArray:arrayOfImages});
    
    // OR you can create the array directly in the options object, as so:
    
    $("#target").rollerblade({imageArray:[
      'path/to/image/1.jpg',
      'path/to/image/2.jpg',
      'path/to/image/3.jpg',
      'path/to/image/4.jpg',
      'and/so/on.jpg'
    ]});
  
  })
  
```

##Options
Rollerblade accepts the following options:

| Property Name | Type | Values | Description | Default |
|---------------|------|---------|-------------|--------|
| sensitivity   | int  | Any integer | The lower the number, the more sensitive the rotator will be. The number value represents distance in pixels between each frame change.| 35 |
| drag          | bool | true/false | Determines if the rotator is draggable. If set to false, image will rotate on any mouse movement along the X axis of the page. | true |
| auto          | bool | true/false  | Determines if rotator should spin by itself. Default is set to false. If set to true, rotator will spin and user interaction will be disabled. | false |
| edgeStop          | bool | true/false  | Determines if the rotator should keep on rotating when the first or last image is reached. | false |
