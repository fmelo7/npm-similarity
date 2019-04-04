# similarity

Returns a difference between two strings using soundex, levenshtein distance or both.

## Installation

```sh
npm install npm-similarity --save
```

## Usage

```js
var similarity = require("npm-similarity")

  Similarity
    Similarity - Soundex
      ✓ Should have method soundex
      ✓ 0.0) Compare [] with []: [0000] and [0000] = true
      ✓ 0.1) Compare [] with [MARIA V C BATISTA]: [0000] and [M612] = false
      ✓ 1.0) Compare [MARIA VELOSO CAVALVANTI BATISTA] with []: [M614] and [0000] = false
      ✓ 1.1) Compare [MARIA VELOSO CAVALVANTI BATISTA] with [MARIA V C BATISTA]: [M614] and [M612] = false
    Similarity - Levenshtein Distance
      ✓ Should have method levenshteinDistance
      ✓ 0.0) Compare [] with []: 100% true
      ✓ 0.1) Compare [] with [MARIA V C BATISTA]: 5% false
      ✓ 1.0) Compare [MARIA VELOSO CAVALVANTI BATISTA] with []: 3% false
      ✓ 1.1) Compare [MARIA VELOSO CAVALVANTI BATISTA] with [MARIA V C BATISTA]: 54% false
    Similarity - combined Soundex and Levenshtein Distance
      ✓ 0.0) Compare [] with []: 0000 and 0000 = true: 100% true
      ✓ 0.1) Compare [] with [MARIA V C BATISTA]: 0000 and M612 = false: 25% false
      ✓ 1.0) Compare [MARIA VELOSO CAVALVANTI BATISTA] with []: M614 and 0000 = false: 25% false
      ✓ 1.1) Compare [MARIA VELOSO CAVALVANTI BATISTA] with [MARIA V C BATISTA]: M614 and M612 = false: 100% true
