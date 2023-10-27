# hydra-extensions
Repository of community extensions and examples for hydra-video-synth. Files are loaded directly from this repository to the list of extensions at https://hydra.ojack.xyz.

#### The categories of entries are as follows:
- **extensions:** scripts that extend the main functionality of hydra-synth, such as adding glsl functions or javascript utility functions. Also includes scripts to help hydra work with other libraries.
- **external-libraries:** code for directly loading other libraries into the hydra editor
- **examples:** groups of examples illustrating specific functionality within hydra
- **[WIP] editor add-ons:** adds UI elements and other functionality to the editor

# Guidelines for adding an extension or example:

```json
 {
        "name": "Op-art patterns",
        "description": "Additional fragment shaders inspired by op-art patterns",
        "documentation": "https://gitlab.com/metagrowing/extra-shaders-for-hydra#op-art-patterns",
        "author": "Thomas Jourdan",
        "thumbnail": "op-art.png",
        "load": "await loadScript(\"https://cdn.statically.io/gl/metagrowing/extra-shaders-for-hydra/main/lib/lib-pattern.js\")",
        "examples": [
            "https://hydra.ojack.xyz/?code=JTJGJTJGJTIwbGljZW5zZWQlMjB3aXRoJTIwQ0MlMjBCWS1OQy1TQSUyMDQuMCUyMGh0dHBzJTNBJTJGJTJGY3JlYXRpdmVjb21tb25zLm9yZyUyRmxpY2Vuc2VzJTJGYnktbmMtc2ElMkY0LjAlMkYlMEFhd2FpdCUyMGxvYWRTY3JpcHQoJTIyaHR0cHMlM0ElMkYlMkZjZG4uc3RhdGljYWxseS5pbyUyRmdsJTJGbWV0YWdyb3dpbmclMkZleHRyYS1zaGFkZXJzLWZvci1oeWRyYSUyRm1haW4lMkZsaWIlMkZsaWItcGF0dGVybi5qcyUyMiklMEElMEFhJTIwJTNEJTIwKCklMjAlM0QlM0UlMjAwLjEzNyUyMColMjB0aW1lJTNCJTBBc3BpcmFsKDIuMCUyQyUyMDUuMCUyQyUyMDAuMykucm90YXRlKCgpJTIwJTNEJTNFJTIwLTIuMCUyMColMjBhKCkpLm91dChvMCklMEFzcGlyYWwoMi4wJTJDJTIwNS4wJTJDJTIwMC4zKS5yb3RhdGUoYSkuZGlmZihjb25jZW50cmljKDEwMC4wJTJDMC4yNSUyQzAuMjUpKS5vdXQobzEpJTBBc3BpcmFsKDIuMCUyQyUyMDUuMCUyQyUyMDAuMykucm90YXRlKGEpLm11bHQoc3BpcmFsKDEuMCUyQyUyMDMuMCUyQyUyMDAuMykpLm91dChvMiklMEFzcGlyYWwoMS4wJTJDJTIwNS4wJTJDJTIwMC4xKS5yb3RhdGUoYSkuZGlmZihicmljaygpKS5vdXQobzMpJTBBcmVuZGVyKCklMEElMEElMEE%3D"
        ]
    },
```
- **name**: title of the extension as it will appear in the editor. Make sure there is no existing extension with the same name
- **description**: SHORT description of what it does
- **documentation**: link to documentation (for extensions, addons, external libraries)
- **author**: include extension author, original library author(s)
- **thumbnail**: ! should be 60px by 60px
- **load**: script for loading external script. make sure to escape quotation marks with '\' to be valid json. i.e.
  ```js
  await loadScript("https://cdn.statically.io/gl/metagrowing/extra-shaders-for-hydra/main/lib/lib-pattern.js")
  ```
should be
```json
"await loadScript(\"https://cdn.statically.io/gl/metagrowing/extra-shaders-for-hydra/main/lib/lib-pattern.js\")"
```
- **examples**: array of hydra links to example usage for this extension. Some guidelines for writing examples:
    - comment the code
    - include example author name in the comments
    - nice to include some very simple, barebones examples as well as slightly more complicated ones
    - think of beginners / those not so familiar with hydra --- stick to hydra core functions whenever possible and minimize using more specialized things such as custom functions, arrays, audio input, etc. unless relevant to the specific extension
