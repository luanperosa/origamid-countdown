# Origamid-countdown-christmas

## See how many days are left until christmas

## The purpose of this project is to demonstrate the basic understanding of Oriented Object Programming. 

### Targets

- [ ] Learn how to refactor functions and parameters to Classes and Methotds
- [ ] Documentation the mais concepts on the README to simplify the studies

### How can see the result of this code? Just click bollow and open console of Brower

[Click here!](https://luanperosa.github.io/origamid-countdown/)


Firstly, it follows a common javascript function called Button using a prototype, this function receives parameters that are used in the prototype to create the method.

```javascript
    function Button(text, background) {
      this.text = text;
      this.background = background;
    }

    Button.prototype.element = function() {
      const buttonElement = document.createElement('button');
      buttonElement.innerText = this.text;
      buttonElement.style.background = this.background;
      return buttonElement;
    }
```

Now we can see this function refactored for class 
```javascript 
    class Button {
      constructor(text, background, color) {
        this.text = text;
        this.background = background;
  }
      element() {
        const buttonElement = document.createElement('button');
        buttonElement.innerText = this.text;
        buttonElement.style.background = this.background;
        buttonElement.style.color = this.color;
        return buttonElement;
      }
}
```

As we can see, the function becames atributes in constructor and prototype becames method.

To access the constructor we need instantiate a object of class, after instantiate it is possible to access the methods using ```.element()```, instantiate a object of class you need use ```new```, bellow we will see an example. Attencion that we need to call the method using (). 
It is possible declare parameters in method, but the betther practice is not declare anyparameters, it's betther declare your atributes in constructor to uses in method.
Don't forget uses ```this```, this is reference of object class, actualy this is return by default in constructor. In method you need to uses this if you need to call the atributes of this class. 
The constructor always is called when you instantiate a object of class, therefore you can call methods in constructor that you want execute by default in class, but this is not recommended, we will see another example to resolve this problem. 
