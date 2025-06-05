# Projects related to DOM

## project link
[Click here ](https://stackblitz.com/edit/dom-project-chaiaurcode?file=index.html)

## project 1

```javascript
console.log("hitesh")
const buttons = document.querySelectorAll('.button');
const body = document.querySelector('body');

buttons.forEach(function(button){
  console.log(button);
  button.addEventListener('click',function(e){
    console.log(e);
    console.log(e.target);
   // if(e.target.id === 'grey'){
      body.style.backgroundColor = e.target.id;
   // }
  })

});


```

## project 2
# solution

```javascript
const form = document.querySelector('form');

form.addEventListener('submit', function (e) {
  e.preventDefault();

  const height = parseInt(document.querySelector('#height').value);
  const weight = parseInt(document.querySelector('#weight').value);
  const results = document.querySelector('#results');
  if (height === '' || height < 0 || isNaN(height)) {
    results.innerHTML = `Please give a valid height: ${height}`;
  } else if (weight === '' || weight < 0 || isNaN(weight)) {
    results.innerHTML = `Please give a valid weight: ${weight}`;
  }else {
    const bmi = (weight / ((height / 100) ** 2)).toFixed(2);
    results.innerHTML = `<span>Your BMI is: ${bmi}</span>`;
  }

});
```
## project 3
# solution

```javascript
const clock = document.getElementById('clock');
//const clock = document.querySelector('#clock')
setInterval(function(){
  let date = new Date();
//console.log(date. toLocaleTimeString());
clock.innerHTML = date.toLocaleTimeString();

},1000);

```
