# Frontend Mentor - Intro component with sign up form

![Design preview for the Intro component with sign up form coding challenge](./design/desktop-preview.jpg)

### Screenshots

![Desktop view](./images/desktop.jpg)
![Desktop error view](./images/desktop-error.jpg)
![Mobile view](./images/mobile.jpg)
![Mobile error view](./images/mobile-error.jpg)

## The challenge

Your challenge is to build out this introductory component and get it looking as close to the design as possible.

You can use any tools you like to help you complete the challenge. So if you've got something you'd like to practice, feel free to give it a go.

Your users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Receive an error message when the `form` is submitted if:
  - Any `input` field is empty. The message for this error should say *"[Field Name] cannot be empty"*
  - The email address is not formatted correctly (i.e. a correct email address should have this structure: `name@host.tld`). The message for this error should say *"Looks like this is not an email"*

### Links

- Solution URL: [Github](https://github.com/atulanand206/fem-signup-intro)
- Live Site URL: [Netlify](https://fem-signup-intro.netlify.app/)

## My process

- After plugging in the HTML semantics, assigned the font weights, colors, margins and paddings to get the layout looking as close to the prototype.
- Plugging in the simple flex to have the split layout in the desktop version.
- Using transform to scale for the buttons hover effect.
- Using solid box-shadow for the bottom shadow of buttons and form.
- Introduced custom properties for font-weights which streamlined the fonts to a certain extent.
- Using `:focus` selector for the active form field.
- Tried using the data-error and container::after for validation, but wasn't able to make it go away if validation resulted in success.
- Introduced sibling divs for showing the errors.
- Weird width sizes for the input siblings elements does not make me happy.
- Following css helped me get rid of js dependency.
```css
.form__input:focus ~ * {
	display: block;
}

.form__input:valid ~ * {
	display: none;
}

.form__input ~ * {
	display: none;
}
```

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

- How to create component just using CSS in a simple div include sizing and placement.
- Using CSS sibling selector to set attributes to all siblings based on pseudo selectors.
- Benefits of required attribute for form validation.

### Continued development

- Trick CSS selectors
- Width of containers.

### Questions for clarification

- It's tricky to set width and margin of components created just usiing CSS from a plain div. How to proper set width of custom CSS components?
- Ways of error handling without the need of javascript?
- What is landmark = "" in firefox accessibility?

## Author

- Atul Anand

## Acknowledgments

Thanks to [Kevin Powell](https://www.youtube.com/channel/UCJZv4d5rbIKd4QHMPkcABCw) for the focused YT tutorials.
