# hello-ref 👋
This Javascript\jQuery project grabs the value of `?ref=` from a URL and present a custom message based on the source. The main use case I planned this script for is for when I share things from my blog [(shameless plug 😬)](http://slashproject.co?ref=github) I'd have the option to present a custom call to action based on the source. 

![alt text](demo.png)

## Installation 
- Prerequisite: Import jQuery to your project 
- Include `hello-ref.js` in your project 
- Include `hello-ref.css` in your project 
- Add the following HTML at the place you'd like to have your message displayed:

```html
    <div class = "hello-ref">
      <div class = "hello-ref-text"></div>
    </div>
```

## How to add additional ref sources 

Currently hello-ref that is on this repo supprots custom messages for Facebook, Twitter, Product Hunt and gitHub but it's super easy to add additional ref sources:

The script uses `switch` and `case` methods to control the text and the css class that will determine the design of the custom message. 

so first of all we should define a css class on `hello-ref.css` - 

```css
  .hello-ref-github {
  background-color: #6e5494;
  border-color: #6e5494; 
  }
```

And then include it as a `case` in the javascript file

```javascript
  case 'producthunt': //this is the name that will be parsed out of ?ref=
      $('.hello-ref').show();
      $('.hello-ref').addClass('hello-ref-producthunt'); // Your css class goes here
      $('.hello-ref-text').text('Hi Product Hunt people 👋 this text is brought to you by Hello-Ref plugin');
      break;
```
🎉
