# Lab 29 - Component Composition
Joy Hou, Feb 21, 2018

## Problem Domain
Building upon lab 28 for the notes to do application, we are refactoring and adding in a update form component that inherits a note through props and onSubmit is able to update the App's state with an updated note.

## Components
### Main
main.js renders the application to the DOM.

### App
The App Component manages routes to the landing (/) component and the dashboard (/) component.

### Landing
The Landing component displays a brief description of the app and links to the dashboard component.

### Dashboard
The Dashboard component manages the entire application state. It contains a notes array with all of our notes in it. There is the handleAddNote method, which allows the user to add a note and contains the note default propeties. There is also a handleRemoveNote method, which allows the user to delete a note. It calls on NoteCreateForm and NoteList components to render the notes form and notes.

### NoteCreateForm
The NoteCreateForm component handles the submission when adding a note. It takes in the user submitted data and adds the note to the application state.

### NoteList
The NoteList component displays an unordered list of NoteItem components.

### NoteItem
The NoteItem component displays each individual note title and content, and also a delete button which removes the note from the application state when clicked.

### NoteUpdate
The NoteUpdate component that inherits a note through props and onSubmit is able to update the App's state with an updated note.