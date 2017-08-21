# Javascript

## Flujos de control

### foreach

```javascript
$.each(<variable>,function(){
 /// codigo
});
```

## TIPS

### Peticiones ajax

```javascript
$.ajax({
  url: "lorem.ipsum.com/dolor",
  type: "POST",
  dataType:'json',
  delay:250,
  cahe: false,
  data : {
   "dato" : 1
  },
  success : function(){
  }
});
```
### Array to json

```javascript
 var array = [1,2,3];
 var json = JSON.stringify(array);
```
### Json to array

```javascript
 var json = JSON.parse(array);
```
