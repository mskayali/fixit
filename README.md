# Fixit

Fixit is a jquery plugin which can be used to fix any element on the webpage.
For Demo : [Click here](http://itsprakash87.github.io/demo/fixit/index.html)


## Fixit : 

Fixit jquery plugin can be used to fix the element at a certain position when the webpage is scrolled and the element is to be hidden, so that the element stay visible on the webpage.
By passing the values of the different options provided, one can control the element.
This easy to use plugin prevent one from dealing with the jquery/javascript code.

## Install : 

````
npm install fix-it
````

## How to use

- Include jQuery and fixit.

```html
<script src="jquery.js"></script>
<script src="jquery.fixit.js"></script>
```

- Give an ID to the target element.(Always give an unique id to target element.)

```html
<div id = "fixthis"> Content to be fixed. </div>
```

- Add class to style the element if you want. (Avoid inline style and style by id for target element.)

```html
<div id = "fixthis" class = "myClass" > Content to be fixed. </div>
```

- Call fixit.

```html
<script>
  $(document).ready(function(){
    $("#fixthis").fixit();
  });
</script>
```

- You are done.

## Options

Following are the different options which can be passed to the function to control the target element.

- `topMargin`: (default: `0`) Margin in pixels between the page top and the element's top when it is fixed.

```html
<script>
  $(document).ready(function(){
    $("#fixthis").fixit({topMargin:10});
  });
</script>
```

- `addClassAfter`: (default: `'null'`) Name of the class which will be added to the element when "fixed". This class will be removed when the element is "unfixed".

```html
<script>
  $(document).ready(function(){
    $("#fixthis").fixit({topMargin:10, addClassAfter:"classToAdd"});
  });
</script>
```

- `sameDimension`: (default: `'true'`) Boolean value determining if the dimension of the element should be same after it is fixed. If any class name is passed, the values of width and height in the class will be ignored, if 'true'.

```html
<script>
  $(document).ready(function(){
    $("#fixthis").fixit({topMargin:10, addClassAfter:"classToAdd", sameDimension:true});
  });
</script>
```

- `zIndex`: (default: `0`) z-index value of the target element after it is fixed.

```html
<script>
  $(document).ready(function(){
    $("#fixthis").fixit({topMargin:10, addClassAfter:"classToAdd", sameDimension:true, zIndex : 50});
  });
</script>
```

## Events

Following are the custom events which are triggered.

- `fixed`: When the element get fixed.

```html
<script>
  $(document).ready(function(){
    $("#fixthis").fixit();
    $("#fixthis").on("fixed",function(){
		  // 	Things to do....
	  });
  });
</script>
```

- `unfixed`: When the element is back to its original location.

```html
<script>
  $(document).ready(function(){
    $("#fixthis").fixit();
    $("#fixthis").on("unfixed",function(){
		  // 	Things to do....
	  });
  });
</script>
```

