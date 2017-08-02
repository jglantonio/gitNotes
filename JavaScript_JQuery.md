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
$.ajax{
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
}
```
