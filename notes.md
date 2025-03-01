# next for grok

## Styles

*   The color bar should show tick marks at the ends, labeled with the minimum and maximum primary-secondary products
*   mousing over a cell should show its unique, secondary weight value, and it should go back to displayin the PxS product at rest, whe your mouse goes away.

## functionality

the **matrix should compute** **products** **in each cell:** `**P[n]*S[n]**`

limit weights to `[-5, 5]`, including 0. Goes for both `P[n]` and `S[n]` weights.

*   _color scale should stay as the gradient from red to grey to green._
*   _gray represents the midpoint of the range, which would be 0 in the case of symmetric color mapping mode._
*   _in Live-color mode, grey will map to the midpoint of the range bounded by the min and max products in the set of all cells._

# 3rd-Shot

## Style
- fill each product-cell completely full of color
- dark theme (^. ^) 
- and make the colors

## function

- we should be able to save our table creations via browser-retained information, probably with cookies, but i'm not very aquainted with them, so you mightknow better
- rather than the weights being controlled via the +/- button fields (for S-weights you have them at the top, for P-weights, in the 2nd column), instead make it so that we can just click a cell to increment/decrement its value. right-click for ++, left click for --

## code

- ~~try and break the css into a seperate file~~
    - actually, that's what fucked up my last attempt at creating this tool, it got montrous and unmanageable very quickly...
- do all the math in integers
- prioritize truth over beauty—make the code light and solid

## Results!

| | Weight | S1 | S2 | S3 | S4 | sh |
|---|---|---|---|---|---|---|
| P1 | 1 | 1 | 1 | 1 | 1 | 1 |
| P2 | 3 | 3 | 3 | 3 | 3 | 12 |
| P3 | 1 | 1 | 1 | 1 | 1 | 1 |