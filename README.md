# Header parallax using using CSS Perspective

### Demo
https://handsomemedia.github.io/Header-Parallax-CSS-Perspective/dist/

### Notes
- Seems to have more voodoo involved than [Intersection Observer method](https://github.com/HandsomeMedia/Header-Parallax-Int-Observer)
- Tested and confirmed not to work when applied to `<html>`.  See also https://stackoverflow.com/q/44370853
- Since scrolling must be handled by `<body>` instead of `<html>`, `window.scrollY` doesn't work.
- Also due to `<body>` scroll, Safari's smooth scrolling doesn't work without special handling.
- Doesn't work on Edge unless we apply a nasty hack: introduce a fixed-position element with top `z-index`.
- On browsers with a non-overlay scrollbar (primarily affects Windows), a gap is introduced approx half the width of the scroll bar.  This is less obvious in some cases, but clearly obvious here (on the left, on Windows): https://keithclark.co.uk/articles/practical-css-parallax/feature-detection/
- https://developer.microsoft.com/en-us/microsoft-edge/platform/issues/5084491/
- https://keithclark.co.uk/articles/pure-css-parallax-websites/
- https://developers.google.com/web/updates/2016/12/performant-parallaxing
- https://codepen.io/GabbeV/post/problems-with-pure-css-parallax
