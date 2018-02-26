# Reproduction repo for deepmerge bug /w webpack

## Installation
Run `npm install` to set up the project.

## Testing
Run `npm start` to start the dev server, and inject the following the devtools of your browser:

```javascript
(function() {
var s = document.createElement("script");
s.src = "http://localhost:8080/dist.js";
document.head.appendChild(s);
})();
```
