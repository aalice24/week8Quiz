# week8Quiz

# Week 8 Quiz

## Part 1 - Imaging Technique Inspiration

I intend to extend the ‘Wheels of Fortune’ artwork by Pacita Abad for the creative coding major project by incorporating animation. I find the pointillism imaging technique particularly suitable, especially La Baie (Saint-Tropez) by Paul Signac. His use of unblended strokes to illustrate the scenery creates a blurred effect from afar which can be further manipulated to reach the goal of animating the artwork. I intend to use this technique by illustrating larger shapes using small dots and creating motion by changing the colour of the dots and shifting it’s position. 

![Image of La Baie](assets/artwork_inspo.webp)

## Part 2 - Coding Technique Exploration

Object-oriented programming (OOP) particularly the Decorator Pattern coding would be ideal for implementing the animation of pointillism. OOP relies on the concept of class and objects and [Decorator Pattern](https://dev.to/alexmercedcoder/oop-design-patterns-in-javascript-3i98#decorator-pattern-in-javascript) is a type of structural design pattern in OOP that allows you to add in new properties to an existing object (dots) without changing its structure. This could be particularly useful in facilitating the animation effect as it gives the flexibility to implement dots in different positions, sizes, and colours. Here is an example of how Decorator Pattern in OOP can be used to create animated pointillism art. 

### Decorator Pattern Code Implementation Example 

```
class Coffee {
  cost() {
    return 5; // Base cost of a regular coffee
  }
}
Now, you want to add decorators to your coffee to customize it with additional options, such as milk and sugar:

javascript
Copy code
class MilkDecorator {
  constructor(coffee) {
    this.coffee = coffee;
  }

  cost() {
    return this.coffee.cost() + 2; // Adding the cost of milk
  }
}

class SugarDecorator {
  constructor(coffee) {
    this.coffee = coffee;
  }

  cost() {
    return this.coffee.cost() + 1; // Adding the cost of sugar
  }
}

const regularCoffee = new Coffee();
const coffeeWithMilk = new MilkDecorator(regularCoffee);
const coffeeWithMilkAndSugar = new SugarDecorator(coffeeWithMilk);

console.log(regularCoffee.cost()); // Output: 5
console.log(coffeeWithMilk.cost()); // Output: 7
console.log(coffeeWithMilkAndSugar.cost()); // Output: 8
```







