# 🔍 First Element Finder

A lightweight JavaScript utility that searches through an array and returns the first element that satisfies a given condition — or `undefined` if none is found.

---

## 📦 Installation

No dependencies required. Just copy the function into your project:

```bash
# Clone the repo
git clone https://github.com/lorddrago12/First-Element-Finder.git
cd First-Element-Finder
```

Or simply copy `findElement.js` directly into your project.

---

## 🚀 Usage

```javascript
import { findElement } from './findElement.js';

// Find first even number
findElement([1, 2, 3, 4], x => x % 2 === 0); // → 2

// Find first string longer than 2 characters
findElement(["a", "bb", "ccc"], s => s.length > 2); // → "ccc"

// No match — returns undefined
findElement([1, 3, 5], x => x % 2 === 0); // → undefined
```

---

## 📖 API Reference

### `findElement(arr, func)`

| Parameter | Type       | Description                                              |
|-----------|------------|----------------------------------------------------------|
| `arr`     | `Array`    | The array of numbers or strings to search through        |
| `func`    | `Function` | A callback that receives each element and returns a boolean |

**Returns:** The first element for which `func(element)` returns `true`, or `undefined` if no match is found.

---

## 💡 How It Works

The function iterates through each element in the array and passes it to the provided callback. As soon as the callback returns `true`, that element is returned immediately. If the loop completes without a match, `undefined` is returned.

```javascript
function findElement(arr, func) {
  for (let i = 0; i < arr.length; i++) {
    if (func(arr[i])) {
      return arr[i];
    }
  }
  return undefined;
}
```

---

## 🧪 Examples

```javascript
// Numbers
findElement([10, 20, 35, 40], x => x % 3 === 0); // → 30... wait → 35 (35 % 5 === 0) — customize your condition!

// Strings
findElement(["apple", "banana", "kiwi"], s => s.startsWith("b")); // → "banana"

// Mixed checks
findElement([4, 7, 12, 19], x => x > 10); // → 12
```

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m 'Add my feature'`
4. Push to the branch: `git push origin feature/my-feature`
5. Open a pull request

---
