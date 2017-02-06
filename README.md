# dzayerjs
Javascript library for algeria cities , build , search , count

#install
```html
<script type="text/javascript" src="dzayerjs.js"></script>

```
#wilaya
```javascript
var alger = dzayer.wilaya(16);
var guelma = dzayer.wilaya('guelma');
```
#commune
```javascript
var frenda = dzayer.commune('frenda');
console.log(frenda.name);//return Frenda

var wilaya = frenda.origin();// tiaret
```


#search
```javascript
//wilayas
var results = dzayer.search( 'al'); // return wilayas
//comunes
var results2 = dzayer.search('ain',true); //return Object
```

#distance

calculate distance between 2 places
```javascript
var bouira = dzayer.wilaya('bouira') ,
adrar = dzayer.wilaya('adrar') ,
distance = dzayer.distance(adrar,bouira); // return 1186 
var distance_m = dzayer.distance(adrar,bouira,'m'); // return 1186396
``` 
#Closest
shows the closest point 
```javascript
// example : closest wilaya to algiers : blida
var x = dzayer.w(15) ,
closest = dzayer.closest(x);
console.log(closest.name) ; //return the closest w to tizi ouezzo
```

#Furthest 
```javascript
     // example 1
  var w1 = dzayer.wilaya(11) ; // tamanrasset
  var w2 = dzayer.furthest(w1);
  console.log(w2.name); //return Annaba

    // example 2
   var w = dzayer.commune('adrar').origin() ;
  var furthest =dzayer.furthest(w);
  console.log(furthest.name); //return El Taref

``` 


