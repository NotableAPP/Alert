CREATE ALERTS LIKE
 [this](screenshot/IMG_20210502_094934.jpg)
***
See the latest preview [here](https://notableapp.github.io/Alert/index.html)
# Getting started
```html
<link rel="stylesheet" href="https://rawcdn.githack.com/NotableAPP/Alert/ad1d80a15959b5f7357657d3732160cbc6fafc06/cdn/TeDlert.css">
<script src="https://rawcdn.githack.com/NotableAPP/Alert/ad1d80a15959b5f7357657d3732160cbc6fafc06/cdn/TeDlertmain.js"></script>
```
```javascript
/* Creating simple alert */
var bsted = Ted();
bsted.alert({
 content:`Welcome to Gboard clipboard, any text you copy will be saved here.`,
 title:`Getting started with Gboard`,
});
/*✅ DONE*/
```
# All Params
|Param|type|default|example|global set methods|
|---|---|---|---|---|
|`title`|string|none|`"Gboard clipboard"`|`Ted().globalSet({title:"title goes here"})`|
|`content`|string|none|`"Welcome to Gboard clipboard, any text you copy will be saved here."`|none|
|`mode`|string(dark or light)|`"light"`|`"dark"`|`<meta name="ted-globalmode" content="dark">`&`Ted().globalSet({mode:'dark'});`|
|`theme`|string(primary, danger,success and warning)|`"primary"`|`"danger"`|none|
|`html`|Boolean|`false`|`true`|`Ted().globalSet({html:true});`|
|`closeBtn`|Boolean|`true`|`false`|none|
|`btns`|array|none|`[{val:'#1',fun:(e)=>{del(e)},}]`|none|
## creating complex alerts for web projects like progrssive web apps
```html
<!-- setting up default mode for the file with this meta tag -->
<meta name="ted-globalmode" content="dark"> <!-- or <meta name="ted-globalmode" content="light"> -->
<!-- It will help you to avoid javascript and use html only to set up dark mode for alerts -->
```
***OR***
You are also able to create 3 default Params
```javascript
var boost = Ted();
boost.globalSet({
   title:'your default title',
   mode:'your default mode',
   html:true ,/* default is false */
   });
boost.alert({
 content:'yeah use only a param',
});
```
# fully filled Params
```javascript
var attributes = {
title:'Gboard clipboard',
Content:`Touch and hold a clip to pin it. Unpinned clips will be deleted after 1 hour.`,
html:false,
mode:'dark',
closeBtn:true,
btns:[
{
val:"#1",
fun: function (e){
del(e);/*deletes alert*/
},
},
],
}
```
for more information get attributes.json file
# btns
btns is Param which creates custom button with there custom click event functions
```js
[
{
val:'#button',
fun:(e)=>{
del(e);
}
}
]
```
|Param|default|type|used for|
|---|---|---|---|
|`val`|undefined|string|buttons value|
|`fun`|none|function|Triggers on click of button|
***
