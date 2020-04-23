# GenerativePixelArt
Generative Pixel Art

# Functions for red, green, and blue channels - where the magic happens!
let redFunction = ["x"]
let greenFunction = ["y"]
let blueFunction = ["x"]
​
img.loadPixels();
for (let i = 0; i < xSize; i++) {
 for (let j = 0; j < ySize; j++) {
   let x = map(i, 0, xSize, -1, 1);
   let y = map(j, 0, ySize, -1, 1);
   let r = evaluateRandomFunction(redFunction, x, y);
   let g = evaluateRandomFunction(greenFunction, x, y);
   let b = evaluateRandomFunction(blueFunction, x, y);
   img.set(x, y, color(255 * r, 255 * g, 255 * b));
 }
}
img.updatePixels();
image(img, 0, 0, width, height);

 let r = evaluateRandomFunction(redFunction, x, y);
   let g = evaluateRandomFunction(greenFunction, x, y);
   let b = evaluateRandomFunction(blueFunction, x, y);
   img.set(x, y, color(255 * r, 255 * g, 255 * b));
