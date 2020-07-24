# Dynamic-Word-Tag-Cloud-Generator-With-jQuery-And-CSS3---jQWCloud

This plugin does not belong to me i have taken it from https://www.jqueryscript.net/text/Word-Tag-Cloud-Generator-jQWCloud.html

* Create a container element in which you want to generate the word cloud.
Create a div with id wordCloud for an example

* Insert jQuery JavaScript library and the jQWCloud.js into your html page.
<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous">
</script>
<script src="jQWCloud.js"></script>


* Prepare your words & tags to be presented in the word cloud.

const myData = [
  {word: 'Prashant', weight: 40},
  {word: 'Sandeep', weight: 39},
  {word: 'Ajinkya', weight: 11, color: 'green'},
  {word: 'Rishi', weight: 27},
  {word: 'Kuldeep', weight: 36},
  {word: 'Vivek', weight: 39},
  {word: 'Saheer', weight: 12, color: 'green'},
  {word: 'Lohit', weight: 27},
  {word: 'Anirudh', weight: 36},
  {word: 'Raj', weight: 22},
  {word: 'Mohan', weight: 40},
  {word: 'Yadav', weight: 39},
  {word: 'India', weight: 11, color: 'green'},
  {word: 'USA', weight: 27},
  {word: 'Sreekar', weight: 36},
  {word: 'Ram', weight: 39},
  {word: 'Deepali', weight: 12, color: 'green'},
  {word: 'Kunal', weight: 27},
  {word: 'Rishi', weight: 80},
  {word: 'Chintan', weight: 22}          
];

* The JavaScript to generate a basic word cloud in the page.

$("#wordCloud").jQWCloud({
  words: myData
});

* Customize the word cloud with the following options.

$("#wordCloud").jQWCloud({

  // title
  title: 'JQ WOrd Cloud',

  // min/max font size
  minFont: 10,
  maxFont: 50,

  // font offset
  fontOffset: 0,

  // shows the algorithm of creating the word cloud
  showSpaceDIV: false,

  // Enables the vertical alignment of words
  verticalEnabled: true,

  // color
  cloud_color: null,

  // font family
  cloud_font_family: null,

  // color of covering divs
  spaceDIVColor: 'white',

  // left padding of words
  padding_left: null,

  // classes with space to be applied on each word
  word_common_classes: null
  
});

* Callback functions available.
$("#wordCloud").jQWCloud({
  word_click : function(){},
  word_mouseOver : function(){},
  word_mouseEnter : function(){},
  word_mouseOut : function(){},
  beforeCloudRender: function(){},
  afterCloudRender: function(){}
});
