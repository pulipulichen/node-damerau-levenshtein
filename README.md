[![NPM](https://nodei.co/npm/damerau-levenshtein.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/damerau-levenshtein/)

https://github.com/pulipulichen/node-damerau-levenshtein

I use algorithm kindly provided by TheSpanishInquisition here: <http://jsperf.com/damerau-levenshtein-distance>.

All credits goes there. I have only packed it into Node module.

It provides a function that takes two string arguments and returns a hash like this:

```` javascript
{
  steps: 5,       // Levenstein demerau distance
  relative: 0.7,  // steps / length of the longer string
  similarity: 0.3 // 1 - relative
}
````

Please see [tests](./test/test.js) for more insights.

----------

# Browserify

http://browserify.org/

````
npm install -g browserify
````

````
browserify browserify.js -o node-damerau-levenshtein.js
````

https://pulipulichen.github.io/node-damerau-levenshtein/node-damerau-levenshtein.js

```` javascript
console.log(levenshtien("國軍程式不敵iPhone 禁止入營", "iPhone鎖功能APP早出現 科技界不解：為什麼國軍做不到？"));
// {steps: 29, relative: 0.9354838709677419, similarity: 0.06451612903225812}
````