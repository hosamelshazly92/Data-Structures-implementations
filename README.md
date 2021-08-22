# Data-Structures-Implementations

JavaScript data structures implementations repository

## List ADT (Abstract Data Type)

A list is an ordered sequence of data

### Usage

| name       |   type   | description                                      |
| :--------- | :------: | :----------------------------------------------- |
| listSize   | property | Number of elements in list                       |
| pos        | property | Current position in list                         |
| length     | property | Returns the number of elements in list           |
| clear      | function | Clears all elements from list                    |
| toString   | function | Returns string representation of list            |
| getElement | function | Returns element at current position              |
| insert     | function | Inserts new element after existing element       |
| append     | function | Adds new element to end of list                  |
| remove     | function | Removes element from list                        |
| front      | function | Sets current position to first element of list   |
| end        | function | Sets current position to last element of list    |
| prev       | function | Moves current position back one element          |
| next       | function | Moves current position forward one element       |
| currPos    | function | Returns the current position in list             |
| moveTo     | function | Moves the current position to specified position |

Create List class implementation

```javascript
let movies = new List();

movies.append("The Dark Knight");
movies.append("Star Wars");
movies.append("The Matrix");
movies.append("The Godfather");
movies.append("Fight Club");
movies.append("Inception");

console.log(movies.toString());
// output ["The Dark Knight", "Star Wars", "The Matrix", "The Godfather", "Fight Club", "Inception"]
```

Implement List class iterator

```javascript
// reset to first position in the list
movies.front();

for (let i = movies.currPos(); i < movies.length - 1; i++) {
    console.log(movies.getElement());
    movies.next();
}
// output The Dark Knight Star Wars The Matrix The Godfather Fight Club Inception
```
