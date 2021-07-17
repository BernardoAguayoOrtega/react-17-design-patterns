###### tags: `react 17 design patterns` `react 17`
# Differentiating between declarative and imperative programming
The easiest way to approach this is to think about imperative programming as a way of describing how things work, and declarative programming as a way of describing what you want to achieve.
## imperative
- Find a glass and collect it from the shelf.
- Place the glass under the tap.
- Pull down the handle until the glass is full.
- Hand me the glass.
## declarative 
"Can I have a beer, please?"

Imagine a simple UI component such as a toggle button. When you click it, it turns green (on) if it was previously gray (off), and switches to gray (off) if it was previously green (on).

The imperative way of doing this would be as follows:

```javascript=
const toggleButton = document.querySelector('#toggle')

toogleButton.addEventListener('click', () => {
  if (toggleButton.classList.contains('on')) {
    toggleButton.classList.remove('on')
    toggleButton.classList.add('off')
  } else {
    toggleButton.classList.remove('off')
    toggleButton.classList.add('on')
  }
})
```
It is imperative because of all the instructions needed to change the classes. In contrast, the declarative approach using React would be as follows:
```jsx
// To turn on the Toggle
<Toggle on />

// To turn off the toggle
<Toggle />
```

In declarative programming, developers only describe what they want to achieve, and there's no need to list all the steps to make it work. The fact that React offers a declarative approach makes it easy to use, and consequently, the resulting code is simple, which often leads to fewer bugs and more maintainability.
