# WIP

## Javascript Testing

### Type of Tests
Unit Testing — Unit testing helps to check that individual unit of code (mostly functions) work as expected.
Integration Tests — Integration tests are tests where individual units/features of the app are combined and tested as a group.
End-to-End Tests — This test helps to confirm that entire features work from the user’s perspective when using the actual application.

### Tools in JS
Jest — a testing tool created by Facebook to test React apps or basically any JavaScript app
jest-cli — a CLI runner for Jest

Puppeteer — a Node library which provides a high-level API to control headless Chrome or Chromium over the DevTools Protocol. We’ll use this to carry out tests from a user’s perspective.

Headless testing is a way of running browser UI tests without the head, which in this case means that there’s no browser UI, no GUI of any sorts. This is useful since when running tests, especially in a CI environment, there is nobody “watching” the visuals, so there is no need to have the extra overhead of the browser GUI.

Conventions
“I’m using an attribute selector on data-testid. data-testid is a convention taken from React Native, which uses the testID prop to identify components in e2e tests. react-native-web took up that convention, and uses, yep, data-testid to identify components.”

### CI (kinda hooks)


### References:
- [Overview of JS Testing in 2018](https://medium.com/welldone-software/an-overview-of-javascript-testing-in-2018-f68950900bc3)
- [Test with Puppeteer](https://blog.logrocket.com/end-to-end-testing-react-apps-with-puppeteer-and-jest-ce2f414b4fd7)
- [Introduction to headless browser testing](https://blog.logrocket.com/introduction-to-headless-browser-testing-44b82310b27c)
- [Old but good practices for testing react apps](https://medium.com/@TuckerConnelly/good-practices-for-testing-react-apps-3a64154fa3b1)
- [Types of Software Testing](https://www.softwaretestinghelp.com/types-of-software-testing/)
- [Too long, didn’t read but worth to check when I have time](https://hacks.mozilla.org/2018/04/testing-strategies-for-react-and-redux/)
