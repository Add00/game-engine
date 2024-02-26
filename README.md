# litecanvas

Lightweight HTML5 canvas engine suitable for small games and animations.

> **litecanvas** is a game engine to enjoy programming: there is no fancy interface, no visual helpers, no gui tools... just coding.

You can [try our online playground](https://litecanvas.github.io) or install via NPM:

```
npm install @litecanvas/litecanvas
```

### Features

-   **Tiny**: only `4KB` gzipped.
-   **Simple API**: just few functions to draw shapes and some utilities to other things like sounds and math.
-   **Offline-first**: You can install the [playground] as webapp and use anywhere at any time.
-   **Predefined color palette**: just use a number (from 0 to 15) to choose a color.
-   **Predefined sounds**: 16 picked sounds created with [ZzFX](https://killedbyapixel.github.io/ZzFX/).

## Getting Started

```js
import litecanvas from '@litecanvas/litecanvas'

litecanvas({
    // you can setup some configurations here
    // learn more in the cheatsheet
})

function init() {
    // run once before the game starts
    color = 3
    posx = CENTERX
    posy = CENTERY
}

function update() {
    // called at 60 fps by default
    // use to update your things
    if (TAPPED) {
        // example: tap to change the position
        posx = TAPX
        posy = TAPY
    }
}

function draw() {
    // use to draw your things
    clear(0) // clear the screen
    circfill(posx, posy, 50, color) // draw a circle
}
```

## Docs

Learn more in the [cheatsheet](https://litecanvas.github.io/about.html).

## Demos

Try some demos in our playground:

-   [Pong](https://litecanvas.github.io?c=eJx9VE1z2jAQvftXbE82wRSDoe3ghA7TEuDQlEmYEo6KLbCmxmZsETJtyG%2FvriS7hqE9YHa1u2%2FffkiJkDxk6TMrnN8WwEFEMh6A3%2FVc1GIuNrEcQO%2BTUlkqBUsEKwawZknBXevYCCxrx6Il3ECn6wUkT0nuK%2FGRRE8fr1Du%2BShHvJBkIHtgPbEkIe3L%2BG4xvjcHq%2BpgBS2YjmeT6QLa0NPWB%2FGLmxykjtJNQjpBi1ylVNJKS8WO8wjFLvEowiw3volY8wJFP7Akf5EG1O9iQet9GkqRpbDfRUxyJ5INoOaINTgmDCEakHO5z9MA2m3YsC2H7Jnnny10xIOYpRHSEuluLwsTuxjN57O7iQYDKBvx9kaWR6xUdbINXewqwNEgbREWZMzJipAGS3X3HfJQKCWk6XnC853ycLXZBe%2B91z9BjbLUlugoa9CoMpOrCHPO03qua6rY4HtB3dLUvIewnH1dTCsnpZmiSn893CZUYxya6ZYFlOvQ%2BaBy6AOa5Eejl2PT%2Fy2aMB0X6xfHPylQz07Fwy4rBA3UKhM0sW%2B0K1eg1%2BMKIhlYZTZtXZ1ZNexThsthYHFDTvpksOvV6Sa8vpq815WtWgJF4wZatUJMHfWWXQw0G34WpnmGMQ9%2FapphliSioH0%2BCBmfrlFl0%2BRd3QG3ylaX9ELRVVbfpfpOG2eEqkLUVWvSA%2FCXomc4HmuXLMrZwdEgIS5grpxObtuQVk8nyXko1yJJnMtkXMzW0OlCkYfK81%2BFdXzjSdff6Xsu0E%2FRdsF3oXwV6l7d0k0RQ%2FGyW19Z7Nv5w8DGfXBQoB3wGurcUDwCxzfU1EVh%2BLRuUscOeSp5bmP8VtCk7DqyeSbd8nlEr8no2xi%2B%2FxjfY4j%2FP19kQtRtVeIAiFlZbTWWP%2F4LrO4%3D)
-   [Shapes](https://litecanvas.github.io?c=eJyFVe9v2jAQ%2FZ6%2F4r5MJCVlSVrarhuaphYNPmxFHVI3VdXkBgNWgxPFpoCm%2Fu87%2FwgJJNkQEhf73b3ndxeTMEljwl%2BJcD3Hma95LFnKgXEmXQ%2F%2BOABCEklhAAHGhC%2BSIhZsRoWNJd1KkrAFdzsx5ZLmHR86z6mU6arj4X7COBVyl1A39IGvk8SH0XD8dTSF93AVeM5bhXqdzZDQkrM5uNMvk8nw1jyXcrpdE72DD7j%2BthfXRUW9IDooOcvJxhaME0py90yJytZi6apA5oSLeZqv3Jvh9%2Bnw%2FqcPJvjlA%2BrVdRVObJiMl%2BBq4kJPTASF4FrHoJnuaSyFLqw%2BzzklLyUyrCJvWI56WrFRFXv3SpJW5Nl1GZ9X4n4lvqjEl0Xloon6SBW2SZrsFilvJbyqSvsh0dJjoOpIlmbGYByP0lvb%2BVOIApySKclAproOpHJJcxBLklGBExSh%2FVderZPWX%2B1%2FQiVsUP%2FD%2BHY6wmEK1TTmCJizJHFPN7iEVYrfjf5eKkkbOBlA2LvsW3wLtl%2Bn3zetXUCMEC0ADxgUdQ45FaTcDus0tt%2FtJCkCilOeYNm%2B0u7D%2FqHppCrnH%2FjzuoxyEPZK8mMlGWK0khV5ofd0sU5IbvPsEfWY%2BZB7eNTAsyn%2FhxtpKqnBIDN1jar6x6I01tTuGxkXByqO9jVvpIiPxq9B8daHXamYzNha2JsGXZNIwbhUb9jj035t%2BnD3ezLGtQiJvhG57E3GDu7iFQSuOgtT1%2BpH%2FPlkCmPY7RYXjqnY07fXFrqWEyvFqXBdhoGp76EROtvzanm7ap5gvD3vzXEOU038GDx5zRshbuh3Sq5zbgE1D7XfxjnJskbjGOdU9dTKxHdyv7UiW2ueSsajhC12NxmKyQd2mjzFxPC%2FJILBAKHwueC9NkIqUIJQ13YNJTDll9LR3BzrL2lrgu0bsWbXjfsLhsMfyA%3D%3D)
-   [Shockwaves](https://litecanvas.github.io?c=eJyNU0lr3DAUvvtXvN7kjuPRdIEwjQOFDJ1AoYUEcig5OJLcUatKRpInY4L%2Fe7V5aebSi6236FuenwW3jNTyWBv0kgE0nRCGaMbkFqzuWJENeZYJZkE9%2FWLEGqjgx2NIENVJy7RL4CxrOkksVxK6ltaWIWpz8HjrNbAj0z3gcgOGESWpAaVhgzH84ULwlHOtvAG0%2B%2Fr5%2B93uBi4m9Gt%2FM2I5de4m8txcUnbyzJ%2FS8Qo%2BpuNqNXYDOCNOzN1Bkd%2FP9ZGhPOSH8JzlJ9IsVgKH02SCZVDN6HyEdWE5uwy3hsUAqK6fUewlgtUabTZugv%2BB23bmkBR6iogTK6pF50Rn5iLnxFDBt0BQ1sbwnxK9DAWYsdvDeZZWGaRrSTnCBTzc3tzv8wKmxH53%2B2V%2Fn4%2FNpmWMOtxYv8Su4x3GOJW9lzKYcEHupUYtE6e76RWetoAL9%2B7TW9eUdyYFT0pTph84tYctvA8pooTSW%2Fjgz0HB1m9PKHn1pwL6cYT2wE3p9%2BI0h70Lez88f%2BHVdsalC20LYrhyizUvkWa20zKCUWasVv0%2FixQK0QSsqhjGSb0FaueWJcNFlWhj4xou87E76FwsEYDg0tH2gp0pjTII1ySW3Cyi52KpKgVhjvnEMDqZtzr93uOnbLhw%2FwdCKofqGhS8qaK5BDFkfwESRkCr)

## Inspirations

-   [floopy](https://github.com/lpagg/floppy): a micro game engine for beginners.
-   [PICO-8](https://www.lexaloffle.com/pico-8.php): fantasy console for making, sharing and playing tiny games.
-   [sweetie-16](https://lospec.com/palette-list/sweetie-16): a sweet 16 colors palette.
