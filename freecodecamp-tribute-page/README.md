# Freecodecamp Tribute Page

An example of the [Tribute Page exercise](https://www.freecodecamp.org/learn/responsive-web-design/responsive-web-design-projects/build-a-tribute-page) for Freecodecamp's responsive web design certification.

It can be viewed online at [codepen.io](https://codepen.io/jimholdaway/pen/wvGNJVK).

Files suitable for local development are found in `/local`.

The exericise has to satisfy the followiing user stories:

- **User Story #1**: My tribute page should have an element with a corresponding id="main", which contains all other elements.

- **User Story #2**: I should see an element with a corresponding id="title", which contains a string (i.e. text) that describes the subject of the tribute page (e.g. "Dr. Norman Borlaug").

- **User Story #3**: I should see a div element with a corresponding id="img-div".

- **User Story #4**: Within the img-div element, I should see an img element with a corresponding id="image".

- **User Story #5**: Within the img-div element, I should see an element with a corresponding id="img-caption" that contains textual content describing the image shown in img-div.

- **User Story #6**: I should see an element with a corresponding id="tribute-info", which contains textual content describing the subject of the tribute page.

- **User Story #7**: I should see an a element with a corresponding id="tribute-link", which links to an outside site that contains additional information about the subject of the tribute page. HINT: You must give your element an attribute of target and set it to _blank in order for your link to open in a new tab (i.e. target="_blank").

- **User Story #8**: The img element should responsively resize, relative to the width of its parent element, without exceeding its original size.

- **User Story #9**: The img element should be centered within its parent element.

## A note about the media queries

Though not necessary for passing the test by following the user stories, some media queries were included to make the text and image fluid in size in relation to the screen width.

The responsiveness and relative size of fonts and divisions was set by initially setting the `font-size` to 100% in the `:root` division. Setting the root font-size this way ensures that users that set their font-size themselves, such as users with visual impairments, are still able to. Then the main element, where all the user stories were required to be statisfied per Freecodecamp requirements, was set to `font-size: 1rem;`. This allowed all child elements to `main` able to have `font-size` and spacings independently set in the main css and `rem` to be proportional to the viewport width with a couple of simple media query calculations.

The calculations are adpated from a method published by [Mike Riethmuller](https://www.madebymike.com.au/writing/precise-control-responsive-typography/).

```css
main {
    font-size: 1rem;
}

@media screen and (min-width: 20rem) {
  main {
    font-size: calc( 1rem + (1.5 - 1) * ( (100vw - 20rem) / ( 100 - 20)));
  }
}

@media screen and (min-width: 100rem) {
  main {
    font-size: 1.5rem;
  }
}
```
