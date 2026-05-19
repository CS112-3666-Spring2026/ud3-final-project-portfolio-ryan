[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=23951597)
# Unit Deliverable 3 - Final Project

Feel free to edit this file to contain a description of your project, as well as your UML diagram and GUI wireframe images. You can simply add them to your project directory and use a relative path, or upload them to [imgur](https://imgur.com/upload).

Use [Markdown](https://gist.github.com/cuonggt/9b7d08a597b167299f0d) to format appropriately. 

## Demo
# Unit Deliverable 3 - Final Project

## Project Description

My final project is a Recipe Manager GUI application. The goal of the project is to help users save, organize, and view recipes in one place. A user can store recipe names, categories, prep time, cook time, favorite status, and basic recipe notes.

The project uses object-oriented programming with a main `Recipe` model class and planned child classes such as `DessertRecipe` and `DinnerRecipe`. The GUI is designed around a main recipe list and a details panel so the user can quickly browse saved recipes.

## Demo

Demo GIF/image will be added here after the final JavaFX project is completed.

## UML Diagram

```mermaid
classDiagram
    class Recipe {
        -name : String
        -category : String
        -prepMinutes : int
        -cookMinutes : int
        -favorite : boolean

        +Recipe()
        +Recipe(name : String, category : String, prepMinutes : int, cookMinutes : int, favorite : boolean)
        +Recipe(original : Recipe)
        +setName(name : String) : boolean
        +setCategory(category : String) : boolean
        +setPrepMinutes(prepMinutes : int) : boolean
        +setCookMinutes(cookMinutes : int) : boolean
        +setFavorite(favorite : boolean) : void
        +setAll(name : String, category : String, prepMinutes : int, cookMinutes : int, favorite : boolean) : boolean
        +getName() : String
        +getCategory() : String
        +getPrepMinutes() : int
        +getCookMinutes() : int
        +isFavorite() : boolean
        +getTotalMinutes() : int
        +toString() : String
        +equals(other : Object) : boolean
    }

    class DessertRecipe {
        -servedCold : boolean
        +DessertRecipe()
        +DessertRecipe(name : String, category : String, prepMinutes : int, cookMinutes : int, favorite : boolean, servedCold : boolean)
        +isServedCold() : boolean
        +setServedCold(servedCold : boolean) : void
        +toString() : String
        +equals(other : Object) : boolean
    }

    class DinnerRecipe {
        -mainProtein : String
        +DinnerRecipe()
        +DinnerRecipe(name : String, category : String, prepMinutes : int, cookMinutes : int, favorite : boolean, mainProtein : String)
        +getMainProtein() : String
        +setMainProtein(mainProtein : String) : boolean
        +toString() : String
        +equals(other : Object) : boolean
    }

    class MealPlan {
        -planName : String
        -recipes : Recipe[]
        -numRecipes : int
        +MealPlan()
        +addRecipe(recipe : Recipe) : boolean
        +removeRecipe(name : String) : boolean
        +toString() : String
    }

    class DuplicateRecipeException {
        +DuplicateRecipeException()
        +DuplicateRecipeException(message : String)
    }

    Recipe <|-- DessertRecipe
    Recipe <|-- DinnerRecipe
    MealPlan o-- Recipe
    DuplicateRecipeException -- MealPlan
Place the animated image of your project demo here!
+--------------------------------------------------+
|                 Recipe Manager                   |
+--------------------------------------------------+
| Search: [________________________]               |
| Category: [All Categories v]                     |
+----------------------+---------------------------+
| Recipe List          | Recipe Details            |
|                      |                           |
| - Chicken Tacos      | Name: Chicken Tacos       |
| - Brownies           | Category: Dinner          |
| - Pasta              | Prep Time: 15 minutes     |
| - Salad              | Cook Time: 20 minutes     |
|                      | Total Time: 35 minutes    |
|                      | Favorite: Yes             |
+----------------------+---------------------------+
| [Add Recipe] [Edit Recipe] [Delete] [Favorite]   |
+--------------------------------------------------+
## UML Diagram
+--------------------------------------------------+
|                 Recipe Manager                   |
+--------------------------------------------------+
| Search: [________________________]               |
| Category: [All Categories v]                     |
+----------------------+---------------------------+
| Recipe List          | Recipe Details            |
|                      |                           |
| - Chicken Tacos      | Name: Chicken Tacos       |
| - Brownies           | Category: Dinner          |
| - Pasta              | Prep Time: 15 minutes     |
| - Salad              | Cook Time: 20 minutes     |
|                      | Total Time: 35 minutes    |
|                      | Favorite: Yes             |
+----------------------+---------------------------+
| [Add Recipe] [Edit Recipe] [Delete] [Favorite]   |
+--------------------------------------------------+
+--------------------------------------+
|              Add Recipe              |
+--------------------------------------+
| Recipe Name:   [__________________]  |
| Category:      [__________________]  |
| Prep Minutes:  [__________________]  |
| Cook Minutes:  [__________________]  |
| Favorite:      [ ]                   |
|                                      |
|           [Save]   [Cancel]          |
+--------------------------------------+
Place your UML diagram image here! Make sure they're updated to be accurate to your final project!

## Wireframe

Place your wireframe image(s) here! Make sure they're updated to be accurate to your final project!