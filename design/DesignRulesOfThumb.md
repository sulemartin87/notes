# Design Rules of Thumb

## Never forget C-R-A-P!

* **Contrast**
    - Don't go halfway with contrast. Either make elements very similar or very different to make their relationships clear.
* **Repetition**
    - Establish elements as having the same relationship by using consistent styles between then.
* **Alignment**
    - Ensure elements are aligned with each other in a purposeful way to give the layout structure and focus.
    - Avoid defaulting to center aligned text.
* **Proximity**
    - Similar with contrast, don't go halfway. Put elements close or far awy to establish their relationship.

## Hierarchy

* Combine different font sizes and colors to establish a hierarchy of importance.
    - Important text is larger, bolder, and darker
    - Secondary text is smaller, thinner, and lighter
    - Aim for 2-3 different shades of gray that still contrast well against the background
    - Aim for 2 font weights, a normal and heavy one (not lower than 400!)

## Typography

* Rounded fonts pair well with rounded shapes, and squared
* Always letter-space your uppercase text.
* Save "display fonts" for headers, since their extra design personality only really works for large, short lines of text. Use simpler, more common font families for body text since they're built to be more readable and decrease eye strain.
* Use unitless measures for line-heights, since it better scales with different font sizes. For example, a `1.25` line-height for an `16px` font size will create a line-height of `20px`.
* Keep text lines between 45 and 75 characters long (including spaces and punctuation).

## Colors

* Find colors that match the same descriptors that you would give your typeface and your overall brand.
* Think of colors in terms of Hue, Saturation, and Brightness. This makes it easier to adjust them.
    - **Use one of more base colors as a starting point**, and adjust the hue for a more suitable tone.
    - Modify saturation and brightness in opposite directions to increase contrast.
        - White text = more saturation, less brightness
        - Dark text = less saturation, more brightness
* Be wise when selecting supporting colors.
    - Colors of two adjacent hues (red and orange) with high saturation don't look well together.
    - Find [the base color's triad color scheme](https://color-wheel-artist.com/triad-color-scheme/) on the color wheel (adjacent colors to the base complimentary color), since they're different but not too different.
* When matching colors to fonts, start by defining different adjectives and emotions. Pair everything else from there.
* When laying translucent black on other colors: the less luminous the color is, the more opaque the black must be to appear.
* Never use gray text on colored backgrounds to reduce contrast and importance! It's better to just make it slightly closer to the background color (either pick a specific color or white/black with reduced opacity)
* Don't always give buttons a background color. Buttons low on the hierarchy can use a transparent one.
    - Secondary buttons can just have borders, tertiary buttons can have no background or border.

Need to find good colors? Try [Dribble's Color Search](https://dribbble.com/colors/) or [The New Defaults](https://dudleystorey.github.io/thenewdefaults/).

## Borders/Shadows

* Borders/Shadows too close in luminosity (converted to grays of respective lightness) to their containers appear too strong. So a shadow with the same luminosity as a colored container will be too strong and look bad.
* The less luminous a container color is, the darker a shadow or border must be
* Box-shadows work better for more serious elements, cartoon-ish borders better for less serious ones.
* Offset your shadows. Shadows going in one direction look more natural than evenly-spaced blurs around an object.
* Don't rely too much on borders to create contrast or space, as they can quickly feel cluttered. More often aim for box shadows, different background colors, or extra spacing.
* Accent borders are an easy way to add visual flair, for components or entire layouts.

## Icons

* Try to "draw icons with the same pen," or have typography styles mirrored by the fonts
    - Sharp-cornered fonts shouldn't use icons with rounded edges
    - Aim for similar stroke weights
    - This is especially important when icons are inline with text, such as in buttons
* Don't take icons designed to be small and increase their size too much, they'll look unnatural. Either use icons designed to be bigger, or put them in a larger shape with a background color.

## Resources

* [The King Vs Pawn Game of UI Design](http://alistapart.com/article/the-king-vs-pawn-game-of-ui-design)
* [The Non-Designers Design Book](https://www.amazon.com/Non-Designers-Design-Book-4th/dp/0133966151)
* [Seven Practical Tips for Cheating Design](https://medium.com/refactoring-ui/7-practical-tips-for-cheating-at-design-40c736799886)
* [Design Principles for Developers: Processes and CSS Tips for Better Web Design](https://css-tricks.com/design-principles-for-developers-processes-and-css-tips-for-better-web-design/)
