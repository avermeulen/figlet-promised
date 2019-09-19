# Figlet Promised 

A version of [Figlet](https://www.npmjs.com/package/figlet) with promises.

Created to make learning `Promises` and `async/await` approachable an fun.

## Use it like this

Use it with a `promise`.

```javascript
const figlet = require("figlet-promised");
figlet("Felix").then(function(result){
	console.log(result);
});
```

Use it with `async/await`.

```javascript
const figlet = require("figlet-promised");
async function runFiglet() {
	const result = await figlet("Felix");
	console.log(result);
}
runFiglet();
```

Use it with `Promise.all` to create multiple ascii decorated words.

```javascript
Promise
	.all([figlet("Luca"), figlet("Felix")])
	.then(function(results){

		results.forEach(function(name) {
			console.log(name);
		});
	});
```