# Disclaimer
These are my personal notes taken from the [Design For Non-Designers](https://open.sap.com/courses/dfnd1-2) course by openSAP.

The lesson was [Goran highlights basic design and layout elements](https://open.sap.com/courses/dfnd1-2/items/3LEDEQqsMiFPsH1wfcnhQZ).

# Grids
- most designs are organized in grids
- predictable
- organisation
- structure
- easier to design
- easier to code

![](assets/basic_design/grid_structure.png)

_Elements are layed out onto an invisible grid_

# Internal Structure
- various elements which are equaly spaced

![](assets/basic_design/equaly_spaced_elements.png)

_A card containing multiple equaliy spaced elements (30px)_

![](assets/basic_design/font_alignment.png)

_Fonts are aligned against their base-line_

![](assets/basic_design/squares_holding_the_layout.png)

_Another point of view: little 30x30 px squares hold the layout in place_

# Whitespaces
- helps focus
- tranmits the message of the letter
- removes nerby clutter
- allows the central piece of content to function
- visually separates

![](assets/basic_design/parking_sign_pure.png)

_Whitespaces are important_

![](assets/basic_design/parking_sign.png)

_Whitespace helps trasmitting the letter_

## Whitespace between elements
![](assets/basic_design/whitespace_between_cards_too_narrow.png)

_No separation between the two cards is noticable_

![](assets/basic_design/whitespace_between_cards_good.png)

_The cards are now recognizable as two separate things_

![](assets/basic_design/too_much_whitespace.png)

_Too much whitespace becomes a third element_


# Alignment
## Symmetry and organisation
- We perceive symmetry as beauty.
- We recognise neat & organized as trustworthy.
- -> It's just the way our brains are hardwired.

![](assets/basic_design/symmetry_is_beautyful.png)

_Symmetry is beautiful - so our brain says_

## Left Alignment
 
![](assets/basic_design/left_alignment.png)

_When aligning left spacing from top, bottom and left are equal_

## Central Alignment
 
![](assets/basic_design/central_alignment.png)

_On central alignment spacing from all sides is equal_

## Right Alignment
 
![](assets/basic_design/right_alignment.png)

_When aligning right spacing from top, bottom and the right are equal_

## Cross Page Alignment

![](assets/basic_design/cross_page_alignment.png)

_Alignment rules also hold true on full page layouts_

## Font Base-Line Alignment

![](assets/basic_design/font_base_line_alignment.png)

_Text is often times aligned to the base-line_

## General Rule
- Alignment is more important than pixel perfect size.

# Interaction
- If something is clickable it should show that it is clickable.
- -> The cursor should change when hovering over a button.
- Also, some visual action should happen on click as well.


- Any clickable element should have a clear design how it looks in these three stages
    - normal
    - hover
    - click

![](assets/basic_design/three_stages.png)

_The three different stages of an element should be easy to distinguish._

# Transitions
- If an element appears on screen it should transition and not appear instantaneously.
- element appears: fade in
- element disappears: fade out
- but don't get too creative here
- if elements scale, also scale them visually. Don't let them just appear.
- If it moves on screen - move it - don't just hide it here and show it there.

Do not do the unexpected!

![](assets/basic_design/unexpected_design.png)

_Unexpected design puts people into hospital - looks like juice but is multi purpose cleaner_

# Screen performance

![](assets/basic_design/less_than_100ms_ui_response.png)

_Less than 100 ms UI response time feels natural_

- __UI response is not application response__
- popping the window is not the same as showing data in that window

## Data Loading Example

![](assets/basic_design/data_loading_before.png)

_A click here loads data from the backend_

![](assets/basic_design/data_loading_on_click.png)

_When clicking a popup with a little animation (pulsating circle) appears_

![](assets/basic_design/data_loading_final.png)

_When the data has arrived from the backend the animation disappears and the record is shown_

Idea: Use the animation time to load the data.

Goal: The UI should always respond instantaneously keeping the user occupied while data is fetched.

## Browser animations are 60 frames per second
- UI should move at 60 frames per second
- Why:
    - persistance of vision & phi phenomenon
    - browsers are unintelligent

Details:
- 24 fps is minimum frame rate, used in movies (cost efficient)
- 48 fps - for some the images feel to real/ too life like

For convinient animations with 24 fps _motion blur_ is required but this is not supported by the browser or CSS.