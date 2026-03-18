#Coding Guidelines

```
/**
*
*@copyright : ToXSL Technologies Pvt. Ltd. < www.toxsl.com >
*@author : Shiv Charan Panjeta < shiv@toxsl.com >
*
* All Rights Reserved.
* Proprietary and confidential : All information contained herein is, and remains
* the property of ToXSL Technologies Pvt. Ltd. and its partners.
* Unauthorized copying of this file, via any medium is strictly prohibited.
*/

```

Project Names

```
• Project Names Must be Capitalized Strings
Preffered:
DemoProject
NotPreffered :
Demo Project or demo_project or DEMO PROJECT

```

Naming Guidelines :

```

• Names must be descriptive. Avoid abbreviations and acronyms. You should be able to read the code out loud, over the phone
 Folder Structure:

• Keep your project organized by separating concerns. For example:

bash
/assets
/components
/constants
/screens
/services
/utils

•Consider organizing by feature when your app grows large (e.g., using "components" or "features").
Always use common components

• Code Style and Formatting
Follow a Style Guide: Use a popular style guide such as Airbnb's React/JSX Style Guide.
ESLint and Prettier: Use ESLint to ensure consistent code style and Prettier to automatically format code.
Use Consistent Naming Conventions:

Use camelCase for variables and functions.
Use PascalCase for components and class names.
Use UPPERCASE for constants.

• Components
Functional Components: Prefer using functional components over class components, as they are simpler and easier to test.
Hooks: Always use React Hooks (useState, useEffect, etc.) for managing state and side effects.

Don’t use lifecycle methods like componentDidMount, componentDidUpdate, etc., in class components.
Avoid Inline Functions: Inline functions can hurt performance by causing unnecessary re-renders. Use useCallback to memoize functions when passing them down to child components.

• State Management
Local State: Use React's useState or useReducer for managing local component state.
Global State: For larger apps, use global state management tools like Redux, Context API, or third-party libraries like Recoil, MobX, etc.
Avoid Prop Drilling: Pass down state and functions via context to avoid prop drilling in deeply nested components.

• Styling
StyleSheet API: Always use StyleSheet.create() for defining styles in React Native to improve performance.
Avoid Inline Styles: Don’t use inline styles within the JSX. Always define styles in a separate object for better performance.
Use Flexbox Layout: Stick to Flexbox for layout, as it is the most flexible and consistent way to arrange elements across different screen sizes.

eg:-
const styles = StyleSheet.create({
container: {
flex: 1,
justifyContent: 'center',
alignItems: 'center',
},
});

• Navigation
Use React Navigation: For handling navigation, React Navigation is the most popular choice. Always use StackNavigator, TabNavigator, and DrawerNavigator appropriately.
Backhandler: Handle back navigation properly to ensure your app works well with both native Android and iOS.


• Handling Side Effects
Use useEffect for side effects like data fetching, subscriptions, or manual DOM manipulation.
Always clean up side effects inside useEffect with the return cleanup function to prevent memory leaks.

Example:-

useEffect(() => {
const fetchData = async () => {
const data = await fetchDataFromAPI();
setData(data);
};

fetchData();

return () => {
// cleanup (e.g., cancel network requests)
};
}, []);

• Performance Optimization
Memoization: Use React.memo for functional components and useMemo for expensive calculations to avoid unnecessary re-renders.
Lazy Loading: Use React.lazy and Suspense for loading components only when needed, especially for large screens.
Avoid Re-renders: Keep an eye on unnecessary re-renders. Use React.memo, PureComponent, and shouldComponentUpdate to optimize performance.
Virtualized Lists: Use FlatList or SectionList for rendering large lists efficiently, as they render only the items visible on the screen.


• Error Handling
Error Boundaries: Implement error boundaries for catching errors in components.
Try-Catch in Async Code: Always use try-catch for asynchronous code to gracefully handle errors.
Display Friendly Error Messages: Always provide user-friendly error messages in the UI, and avoid exposing stack traces to end users.


• Asynchronous Programming
Async/Await: Always use async/await syntax for working with asynchronous operations. Avoid using .then() and .catch() chains.
Avoid Blocking UI: Ensure that asynchronous tasks do not block the UI thread. Use background tasks or native modules if needed.

• API Calls
Use Axios or Fetch: For network requests, prefer libraries like axios or the built-in fetch.
Error Handling for Requests: Always handle errors gracefully, including network failures, timeouts, and invalid responses.
Debounce Input: If making API calls based on user input (e.g., search functionality), debounce the input to avoid making requests on every keystroke.

• Testing
Unit Tests: Write unit tests for your components using libraries like Jest and React Native Testing Library.
Integration Tests: Test interactions between components to ensure that they work together as expected.
End-to-End Testing: Use tools like Detox for end-to-end testing to simulate real user interactions.

• Platform-Specific Code
Platform-Specific Components: Use Platform.OS to write platform-specific code when necessary (e.g., for iOS or Android-specific behavior).

js
CopyEdit
import { Platform } from 'react-native';

const isIOS = Platform.OS === 'ios';

• Code Reviews & Collaboration
Pull Requests (PR): Use pull requests to ensure that code is reviewed and follows the coding guidelines.
Clear Commit Messages: Write clear and concise commit messages explaining the "why" behind the changes, not just the "what."
Collaborative Development: Use tools like GitHub, GitLab, or Bitbucket for version control and collaboration.

• Third-Party Libraries
Use third-party libraries only when necessary. Always check for well-maintained libraries with good documentation.
Examples include react-navigation, redux, axios, and react-native-gesture-handler.
```
