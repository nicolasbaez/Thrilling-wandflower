# Thrilling-wandflower
We come from outer space

![buh](https://github.com/nicolasbaez/Thrilling-wandflower/blob/main/xp008.gif)
```javascript
w = 500;
h = w / 2;
k = 0;
setup = (_) => createCanvas(w, w, WEBGL);
draw = (_) => {
  background(0);
  noStroke();
  rotateY(k);
  rotateX(k / 2);
  rotateX(k / 4);
  directionalLight(
    map(sin(k), -1, 1, 0, h),
    0,
    map(cos(k), -1, 1, 0, h),
    0,
    0,
    -1
  );
  sphere(h * 0.666, 3, 2);
  k += 0.03;
};
function keyPressed() {
  if (key === "s") {
    saveGif("xp008.gif", 838, { delay: 0, units: "frames" });
  }
}
