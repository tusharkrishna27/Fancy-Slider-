# Fancy-Slider-
characters animation sliders 
Overview
This project implements a fully functional, animated slider with interactive navigation and auto-sliding features. The slider displays multiple slides with images and text (featuring popular Marvel characters such as Black Widow, Captain America, Iron Man, and Thor) and includes transitions, blending effects, and a credits section. The functionality is supported by HTML for the structure, CSS for styling and animations, and JavaScript for interactive behavior and slide control.

File Breakdown
1. index.html
Structure & Semantics:
The HTML file provides the main document structure. It declares the document type and language, sets meta tags for character encoding and viewport responsiveness, and links to the CSS file.
Content:
The body contains a slider container (.demo-cont) that houses:
The slider component (.fnc-slider.example-slider), which contains a set of slides (.fnc-slide). Each slide has a unique blend class (e.g., m--blend-green, m--blend-dark, etc.) and is structured with an inner wrapper, mask, heading, and an action button labeled “Credits.”
A navigation bar (.fnc-nav) that includes background elements for the navigation and clickable controls that let the user select a specific slide.
A credits panel that slides in and out, displaying information about the creator (TUSHAR KRISHNA) and a reference to the original design concept.
Interactivity Hints:
The HTML includes comments explaining how to enable the global blend mode and how the slider expects specific images (with transparency or monotone backgrounds) for best blending results.

2. main.js
Core Functionality:
The JavaScript file handles all slider interactions and animations. It includes:
A helper function ($$) for element selection.
An initialization function (_fncSliderInit) that sets up slide and control IDs, manages the active and previous states of slides and navigation backgrounds, and handles the auto-sliding feature.
Slide Transitions & Controls:
The code listens for click events on navigation controls and updates the slider by performing smooth transitions. It uses CSS classes (such as m--active-slide, m--previous-slide, etc.) to trigger animations defined in the CSS.
Auto-Sliding:
Auto-sliding is implemented with a configurable delay. Once a slide transition completes, a timer is set to automatically transition to the next slide, unless the auto-sliding feature is blocked (e.g., after a manual click).
Additional Interactivity:
A click on the “Credits” button toggles the visibility of the credits panel.
A toggle control (global blend mode switch) allows users to activate a blend mode effect on the slider images.
The script concludes by initializing the slider on the element with the class .example-slider and setting the auto-sliding delay to 4000 milliseconds.


3. style.css
Visual Styling & Layout:
The CSS file is responsible for the layout, appearance, and animation effects of the slider. It defines styles for:
General Layout:
Ensuring that the slider fills the viewport (using 100vh for height) and that all elements are properly positioned using absolute and relative positioning.
Slide Appearance:
Each slide (.fnc-slide) has distinct background images and color blending modes. There are specific styles for mask effects, transitions, and text animations that create the smooth slide-in/out effects.
Transitions & Effects:
Detailed transition timings are set for various elements (slides, masks, headings, and navigation controls) to achieve the desired animated effect. The CSS leverages transformations, opacity changes, and clip-paths to create dynamic visuals.
Navigation Controls:
Navigation buttons are styled to include progress bars that animate during the auto-slide delay. Active and previous control states are visually differentiated.
Credits Panel & Colorful Switch:
The credits panel slides in from the right with its own styling, while the colorful switch (used for activating the global blend mode) features gradient backgrounds and animated transitions.
Overall, the CSS complements the JavaScript behavior to create a polished, interactive slider experience.
