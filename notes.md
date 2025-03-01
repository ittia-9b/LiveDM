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

# 4rth Shot w/ Claude 3.7-sonnet-thinking

## function
- be sure to limit the P and S-weights to the range [-5, 5]. Right now, the S_n weights can't go below zero.
- every valid click that results in a weight change should trigger a complete update of every cell, and all the coloring of the table
    - this should fix the current bug where the un-hovered state of a cell, after you finish setting its S_n weight, will snap back to the previous, un-updated value until you go and click something else
- along with the .md generation, add a button to copy the output once it's rendered


## style
- give a nice tier-list iat the bottom ofthe page, another modality to show how the P_n x S_n combinations rank against one another 
- the entirety of each cell should be a hitbox for click-to-change.
- make the P_n weights settable by the click-to-change method, instead of the current popup text field

# 5th Shot w/ Claude 3.7-sonnet-thinking

## function
- i changed my mind about negative weights, just limit them all to ]0, 5] (not including PxS products, obvi)
- fix the bug where a S_n cell with S-weight of 0 doesn't result in a product equalling 0

## style
- prevent cells from jumping back to displaying product-values as long as the mouse cursor is hovering.
- prevent context menus from appearing
- adjust the symmetrical range mode to map values [0, 25] to [red, green]
- text within the matrix should be non-selectable
- the title, row labels, col labels should all be editable text fields, instead of initialized when creating the table or adding rows/cols
    - clicking add row/col will not prompt the user with a popup



# 6th Shot w/ Grok3 think

## function
- i changed my mind about the welcome page, let's have it actually just land on one page which has a title, short explination of how the tool is useful and to work with it. You can auto-populate 2 Primary and 2 Secondary conditions to initialize the matrix.
- fix the bug where adding a row or col wipes all currently stored data. It causes me grief. The matrix should keep the pre-filled values intact during row/col operations.
- also there is a bug where hitting remove (1) row/colends up removing a shitload of them, it is distressing.

## style
- restore the color gradient to red->grey->green, because it looks kinda yellow right now.
- adjust theway that P x S items that = 0 are rendered in the tier list. They do not look well rght now... the css is just a bit broken there to be _
- please, no more pop-ups
