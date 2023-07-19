# hydra-extensions
List of community extensions and other libraries to use in Hydra

---

## How to load extensions

In the Hydra editor, you can load any external scripts, libraries or hydra-synth extensions using the following syntax at the top of your sketch:

```javascript
await loadScript("https://cdn.statically.io/gl/metagrowing/extra-shaders-for-hydra/main/lib/lib-noise.js")

warp(1)
	.diff(gradient(1).b().color(.25,-.25,.4))
	.modulateScale(whitenoise(1,1),.05)
	.blend(o0)
  	.out()
```

## List

### Libraries

| library      | description                                                       | url                                                                     |
|--------------|-------------------------------------------------------------------|-------------------------------------------------------------------------|
| p5.js        | p5.js is a JavaScript library for creative coding                 | already embedded in the editor                                          |
| three.js     | JavaScript 3D Library                                             | https://threejs.org/build/three.js                                      |
| paper.js     | Vector graphics framework that runs on the HTML5 Canvas           | https://unpkg.com/paper                                                 |
| Tone.js      | Web Audio framework for creating interactive music in the browser | https://unpkg.com/tone                                                  |
| Pizzicato.js | A web audio Javascript library                                    | https://cdnjs.cloudflare.com/ajax/libs/pizzicato/0.6.4/Pizzicato.min.js |

### Extensions

| extension           | description                                                         | url                                                                                      |
|---------------------|---------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| hydra-glsl          | Code glsl on the fly inside Hydra code                              | https://cdn.jsdelivr.net/gh/ritchse/hydra-extensions/hydra-glsl.js                       |
| hydra-pixels        | Read pixels from each hydra output                                  | https://cdn.jsdelivr.net/gh/ritchse/hydra-extensions/hydra-pixels.js                     |
| hydra-abbreviations | Abbreviations for all the functions                                 | https://cdn.jsdelivr.net/gh/ritchse/hydra-extensions/hydra-abbreviations.js              |
| hydra-canvas        | Useful functions to change canvas properties                        | https://cdn.jsdelivr.net/gh/ritchse/hydra-extensions/hydra-canvas.js                     |
| hydra-outputs       | Adds useful functions to change each output's frame buffer settings | https://cdn.jsdelivr.net/gh/ritchse/hydra-extensions/hydra-outputs.js                    |
| hydra-nowrap        | Disables all wrapping in Hydra                                      | https://cdn.jsdelivr.net/gh/ritchse/hydra-extensions/hydra-nowrap.js                     |
| hydra-fractals      | Useful functions for fractals (mirrors, etc)                        | https://cdn.jsdelivr.net/gh/ritchse/hydra-extensions/hydra-fractals.js                   |
| hydra-superdirt     | A Hydra extension for handling SuperDirt RMS events                 | https://cdn.jsdelivr.net/gh/munshkr/hydra-superdirt/index.js                             |
| lib-pattern         | Additional shaders inspired by op-art patterns                      | https://cdn.statically.io/gl/metagrowing/extra-shaders-for-hydra/main/lib/lib-pattern.js |
| lib-color           | Additional filters for mixing or manipulating colors                | https://cdn.statically.io/gl/metagrowing/extra-shaders-for-hydra/main/lib/lib-color.js   |
| lib-noise           | Noise shaders inspired by the work of F. Kenton Musgrave            | https://cdn.statically.io/gl/metagrowing/extra-shaders-for-hydra/main/lib/lib-noise.js   |
| lib-screen          | Shaders to apply to outputs (useful for feedback and final effects) | https://cdn.statically.io/gl/metagrowing/extra-shaders-for-hydra/main/lib/lib-screen.js  |
| lib-wave            | Additional periodic patterns (wave shapes)                          | https://cdn.statically.io/gl/metagrowing/extra-shaders-for-hydra/main/lib/lib-wave.js    |
| antlia-colors       | Use colors as arrays and apply many useful functions                | https://cdn.jsdelivr.net/gh/ritchse/hydra-antlia/antlia-colors.js                        |
| antlia-interact     | Extension to make interaction with mouse and keyboard easy          | https://cdn.jsdelivr.net/gh/ritchse/hydra-antlia/antlia-interact.js                      |
| antlia-maths        | Useful math functions to use in Hydra                               | https://cdn.jsdelivr.net/gh/ritchse/hydra-antlia/antlia-maths.js                         |
| antlia-shapes       | Useful geometric shapes                                             | https://cdn.jsdelivr.net/gh/ritchse/hydra-antlia/antlia-shapes.js                        |
