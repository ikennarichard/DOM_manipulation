Document Object Model (DOM) manipulation, using Javascript to manipulate elements of the DOM, practical examples to apply. by CodeLabs

Key Takeaways
- What the DOM is
- Methods to select elements in the Dom
- How to traverse the DOM
- How to manipulate the DOM
- Event Handling

The DOM is a property of the window object
Most nodes in the DOM tree have a parent, child, sibling relationship

- the querySelector and querySelectorAll is a powerful way to select elements.

How to select elements
//getElementByID()

const title = document.getElementById('main_heading');

// getElementByClassName()

const listItems =  document.getElementsByClassName('list_items');

// getElementByTagName()

const tagName = document.getElementsByTagName('li');

// querySelector()

const container = document.querySelector('div');
const allContainer = document.querySelectorAll('div');



**************Part 2

const title = document.querySelector('#main_heading');
title.style.fontSize = '3rem';
title.style.color = 'red';



//styling multiple elements

const listItems =  document.querySelectorAll('.list_items')

listItems.forEach(item =>{
    item.style.backgroundColor ='pink';
})


//creating elements

const ul = document.querySelector('ul');
const newList =  document.createElement('li');

//adding element
ul.append(newList);

//modifying text in html ()
const spanItem = document.querySelector('.list_items')

console.log(spanItem.innerHTML); //you should use this less
console.log(spanItem.textContent);
console.log(spanItem.innerText);

newList.innerText = 'The Lies of a Saint'


//modifying Attribute

newList.setAttribute('class', 'main_movie');

// const movie = document.querySelector('.main_movie')
// movie.style.backgroundColor = 'orange';

// newList.removeAttribute('class')
console.log(title.getAttribute('id'));

//modifying Classes

newList.classList.add('list_items')

console.log(newList.classList.contains('list_items'))

