Overview

This project will guide you through using Redux for state management in a React application. You will learn about custom hooks and have the opportunity to explore a new technology of your choice.
Concepts and Objectives

    Redux
        Understand the role of Redux and its differences from context.
        Learn about the key terms: Store, Reducer, Action, Action Builder, Connect.
        Set up Redux with a store and reducers.
        Create actions and initialize/update state in reducers.

    Advanced Redux (Ducks)
        Use the Provider component to house the Redux store.
        Connect components to the Redux store.
        Use mapStateToProps and mapDispatchToProps.
        Split store state using combineReducers.
        Add middleware to the Redux store.
        Use middleware to manage async actions.

    Custom Hooks
        Create custom hooks for simplified and reusable code.

    Tech Exploration Day
        Pick a new technology and learn it.

Project Features
MVP Features

    User Search and Results
        User can input a search term and see relevant results.
        User can select a country to view details.
        Display country’s overview, weather, and symbols information.

    Design
        Implement Redux Toolkit for state management.
        Configure displayCountry and potentialCountries slices.
        Properly configure the Redux store and ensure accurate state updates.

Steps to Complete the Project
1. Overview and Setup

Goal: Understand the application architecture and set up the starter code.

Steps:

    Download the starter code and run npm install and npm start.
    Review the component architecture and understand the data flow.

2. Set Up Redux for potentialCountries State

Goal: Manage global state for the list of potential countries.

Steps:

    Install dependencies: npm install react-redux @reduxjs/toolkit.
    Create the Redux directory structure.
        src/redux/store.js
        src/redux/slices/potentialCountriesSlice.js
    Configure store.js with configureStore and set up an empty reducer object.
    Configure potentialCountriesSlice.js with createSlice.
        Define initial state, reducers (setPotentialCountries, deletePotentialCountries).
    Connect Redux to the React application in index.js.
    Use useSelector in App.js to verify state connection.

3. Display the List of Potential Countries

Goal: Update and display state with a list of potential countries based on user input.

Steps:

    In Header.js, use useDispatch to dispatch deletePotentialCountries and setPotentialCountries actions upon API call.
    In OptionDisplay.js, use useSelector to read from global state and display the list.

4. Set Up Redux for displayCountry State

Goal: Manage global state for the selected country.

Steps:

    Create src/redux/slices/displayCountrySlice.js.
    Configure the slice with initial state and reducers (setDisplayCountry, deleteDisplayCountry).
    Add the reducer to store.js.
    Use useDispatch in OptionDisplay.js to set displayCountry upon country selection.
    Display the selected country in Header.js and clear it when a new search is made.

5. Display Country Details in MainDisplay

Goal: Display selected country information based on state.

Steps:

    Create components: Overview.js, Symbols.js.
    In MainDisplay.js, import and conditionally render the child components.
    Populate Overview.js with relevant country details from state.
    Populate Symbols.js with relevant country symbols from state.

Custom Hooks

Goal: Create reusable custom hooks.

Steps:

    Identify reusable logic in your components.
    Abstract this logic into custom hooks.

Advanced Redux (Ducks)

Goal: Use advanced Redux patterns.

Steps:

    Connect components to the Redux store using connect.
    Split the state using combineReducers.
    Add and configure middleware for async actions.

Conclusion

By following these steps, you will implement a full-fledged "Country Explorer" application with Redux for state management. Remember to review each section and its objectives as you progress to ensure a thorough understanding and proper implementation. Happy coding!
