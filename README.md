# Ninja-Array
### Array extension for TypeScript

The main advantage of this package - is Array.prototype extension

You don't need to use some specific object like `let a = new MySuperArray()`

Compatible with TypeScript. IDE will offer you available methods, 
including the following.

<img width="638" alt="Снимок экрана 2020-02-28 в 11 14 12" src="https://user-images.githubusercontent.com/17552441/75522634-7d3d2f00-5a1b-11ea-8d00-376b56efd3e1.png">

### Installation:
- run `yarn add ninja-array`

### Usage
- Add `import 'ninja-array';` to your root `index.js`
- You're perfect! Your Array is upgraded!

```typescript
const array = [1, 2, 3];

console.log(array.first);         // -> 1
console.log(array.last);          // -> 3
console.log(array.removeLast(2)); // -> [1]
```

### Available things:
```typescript
  // Returns last element of array
  last: T;

  // Returns first element of array
  first: T;

  // Returns true if length == 0
  isEmpty: boolean;

  // Returns true if length > 0
  isNotEmpty: boolean;

  // Returns the element of array at the specified position
  get(position: number): T

  // Inserts element at specific position
  // position = 0  by default
  insert(element: T, position?: number): void

  // Removes all elements
  clear(): void

  // Removes elements at the specified indices
  remove(...indices: number[]): T[]

  // Removes N last elements of the array
  // count = 1 by default. 
  // You can omit the count if want to remove the last item
  removeLast(count?: number): T[]

  // Removes N first elements of the array
  // count = 1 by default. 
  // You can omit the count if want to remove the first item
  removeFirst(coun?: number): T[]

  // Removes and returns the last element of an array
  popLast(): T

  // Removes and returns the first element of an array
  popFirst(): T

  // Swaps elements at the specified indices
  swap(a: number, b: number): void

  // Returns true if array contains the specified element
  contains(element: T): boolean

  // Returns true if array contains all of specified elements
  containsAll(...elements: T[]): boolean

  // Returns array without duplicate
  // [1, 1, 2, 2] -> [1, 2]
  collapse(): T[]

  // Returns union of two arrays
  // [1, 2, 3].merge([4, 5]) -> [1, 2, 3, 4, 5]
  merge(array: T[]): T[]

  // Returns difference of two arrays
  // [1, 2].diff([1, 2, 3]) -> [3]
  diff(array: T[]): T[]

  // Returns true if arrays are identical, including order
  // [1, 2, 3] == [1, 2, 3], 
  // but [1, 2, 3] != [3, 2 ,1]
  identical(array: T[]): boolean

  // Returns true if arrays contents are equal, despite order
  // [1, 2, 3] == [1, 2, 3], 
  // but [1, 2, 3] == [3, 2 ,1]
  equal(array: T[]): boolean

```

Feel free for contributing 🤗
