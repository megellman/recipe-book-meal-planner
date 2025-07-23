🚀 Project: CLI Recipe Book & Meal Planner

### 📌 User Story
AS A home cook  
I WANT to save and view recipes and create meal plans for the week  
SO THAT I can organize my cooking and grocery shopping efficiently

### ✅ Acceptance Criteria
GIVEN a command-line application that accepts user input  
WHEN I start the application  
THEN I am prompted to enter a recipe name, ingredients, and cooking instructions  
WHEN I finish adding a recipe  
THEN I am presented with a menu to add another recipe, view saved recipes, create a meal plan, or exit  
WHEN I choose to view saved recipes  
THEN I see a list of all recipe names and can select one to view its details  
WHEN I choose to create a meal plan  
THEN I am prompted to select recipes for each day of the week  
WHEN I finish planning meals  
THEN an HTML file is generated showing the weekly meal plan with recipe names and links to their full details  
WHEN I click on a recipe name in the HTML meal plan  
THEN I see the recipe's ingredients and instructions

### 📝 Requirements & Key Skills Tested
✅ Object-Oriented Programming:  
Implement Recipe, MealPlan, and optionally a GroceryList class

✅ Class inheritance and constructors:  
Recipe is a base class with name, ingredients, instructions  
MealPlan stores recipes for each day  
Could extend classes if adding categories of recipes (e.g. BreakfastRecipe, DinnerRecipe)

✅ CLI with Inquirer to gather user inputs  
✅ File I/O to save recipes to JSON and read them later  
✅ HTML generation to output the meal plan in a readable webpage (similar to team profile HTML output)  
✅ Testing with Jest for each class and utility function  
✅ Git, clean folder structure, .gitignore, README with usage instructions

### 🔧 Suggested Directory Structure
.
├── __tests__/             // Jest tests  
│   ├── Recipe.test.js  
│   ├── MealPlan.test.js  
│   └── (optional) GroceryList.test.js  
├── data/                  // stores recipes as JSON files  
├── dist/                  // generated HTML meal plan  
├── lib/                   // classes: Recipe.js, MealPlan.js  
├── src/                   // template helper code for generating HTML  
├── .gitignore  
├── index.js               // runs the application  
└── package.json           

### 💻 Example Class Design

**Recipe.js**  
```js
class Recipe {
  constructor(name, ingredients, instructions) {
    this.name = name;
    this.ingredients = ingredients; // array of strings
    this.instructions = instructions;
  }

  getName() {
    return this.name;
  }

  getIngredients() {
    return this.ingredients;
  }

  getInstructions() {
    return this.instructions;
  }

  getSummary() {
    return `${this.name}: ${this.ingredients.length} ingredients`;
  }
}

module.exports = Recipe;
