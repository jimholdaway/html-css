# Freecodecamp Survey Form

An example of the [Survey Form exercise](https://www.freecodecamp.org/learn/responsive-web-design/responsive-web-design-projects/build-a-survey-form) for Freecodecamp's responsive web design certification.

It can be viewed online at [codepen.io](https://codepen.io/jimholdaway/pen/rNeOmNN).

Files suitable for local development are found in `/local`.

The exericise has to satisfy the followiing user stories:

- **User Story #1:** I can see a title with id="title" in H1 sized text.

- **User Story #2**: I can see a short explanation with id="description" in P sized text.

- **User Story #3:** I can see a form with id="survey-form".

- **User Story #4:** Inside the form element, I am required to enter my name in a field with id="name".

- **User Story #5:** Inside the form element, I am required to enter an email in a field with id="email".

- **User Story #6:** If I enter an email that is not formatted correctly, I will see an HTML5 validation error.

- **User Story #7:** Inside the form, I can enter a number in a field with id="number".

- **User Story #8:** If I enter non-numbers in the number input, I will see an HTML5 validation error.

- **User Story #9:** If I enter numbers outside the range of the number input, which are defined by the min and max attributes, I will see an HTML5 validation error.

- **User Story #10:** For the name, email, and number input fields inside the form I can see corresponding labels that describe the purpose of each field with the following ids: id="name-label", id="email-label", and id="number-label".

- **User Story #11:** For the name, email, and number input fields, I can see placeholder text that gives me a description or instructions for each field.

- **User Story #12:** Inside the form element, I can select an option from a dropdown that has a corresponding id="dropdown".

- **User Story #13:** Inside the form element, I can select a field from one or more groups of radio buttons. Each group should be grouped using the name attribute.

- **User Story #14:** Inside the form element, I can select several fields from a series of checkboxes, each of which must have a value attribute.

- **User Story #15:** Inside the form element, I am presented with a textarea at the end for additional comments.

- **User Story #16:** Inside the form element, I am presented with a button with id="submit" to submit all my inputs.

## A note about the media queries

Though not necessary for passing the test by following the user stories, some media queries were included to make the text and form responsive in size in relation to the screen width.

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
