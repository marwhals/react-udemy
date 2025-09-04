# Forms in React

---

## Challenges

- Form submission
  - Handling submission is relatively easy
  - Entered values can be managed via state
  - Alternatively, the can be managed via refs
  - Or via FormData and native browser features
- Input validation - more tricky
  - Need to provide a good user experience
  - Could validate on every keystroke -> errors may be shown too early
  - Can validate on lost focus -> errors may be shown too long
  - Can validate on form submission but errors may be shown too late

---

- Server serves the React app - JavaScript files + index.html to users visiting the website
- Browser automatically creates and sends a HTTP request with entered form data
- Add code to the react app to send collected data to a separate, standalone backend API