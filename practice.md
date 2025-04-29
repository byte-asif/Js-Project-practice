## Practicing DOM in js

# Project link [click me](https://stackblitz.com/edit/dom-project-chaiaurcode-dqmqucrd?file=1-colorChanger%2Fchaiaurcode.js,1-colorChanger%2Findex.html)

## Solution Code

# Practice problem 1
``` javascript

const buttons=document.querySelectorAll('.button');
const body= document.querySelector('.body');

buttons.forEach (function(button){

  button.addEventListener('click', function(e){
    if(e.target.id === 'grey'){
      console.log("its grey");
      document.body.style.backgroundColor = e.target.id;

    };

    if(e.target.id === 'white'){
      console.log("its white");
      document.body.style.backgroundColor = e.target.id;
    };
    if(e.target.id === 'blue'){
      console.log("its blue");
      document.body.style.backgroundColor = e.target.id;
    };
    if(e.target.id === 'yellow'){
      console.log("its yellow");
      document.body.style.backgroundColor = e.target.id;
    };


  });
} )

```


#practice problem 2

```javascript

const form = document.querySelector('form');
// this usecase will give you empty
// const height = parseInt(document.querySelector('#height').value)

form.addEventListener('submit', function (e) {
  e.preventDefault();

  const height = parseInt(document.querySelector('#height').value);
  const weight = parseInt(document.querySelector('#weight').value);
  const results = document.querySelector('#results');

  if (height === '' || height < 0 || isNaN(height)) {
    results.innerHTML = `Please give a valid height ${height}`;
  } else if (weight === '' || weight < 0 || isNaN(weight)) {
    results.innerHTML = `Please give a valid weight ${weight}`;
  } else {
    const bmi = (weight / ((height * height) / 10000)).toFixed(2);
    //show the result
    results.innerHTML = `<span>${bmi}</span>`;
  }
});



```