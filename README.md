# The Pragmatic ToDo

A ToDo list for pragmatic people.

## Local development

This project requires `NodeJS v20 LTS` or later versions.

Clone the repository to your local machine and open the downloaded project directory. Then, type the following commands:

```bash
cd pragmatic-todo
npm i
npm run dev
```

---

## Features

The Pragmatic To-do list is a single-page application (SPA) made with React/Typescript.
It is based in a context-switching behavior, where each context provides a given set of features:

> * Task Management;
> * Calendar Agenda Management;
> * A sticky notes desk;
> * Theme Switching;
> * Activity Dashboards/Statistics;
> * Local data persistence (via the IndexedDB browser API);
> * Back-end synchronization (optional);
> * A lateral menu for navigating between contexts:
   >  * Home Page;
   >  * Tasks;
   >  * Events;
   >  * Notes;
   >  * Settings;

---

## Context

The following section describes which features and behavior is set to a given application context. Each context is meant
to be a separate, independent, section of the application, which might share data or behavior between them.

If behavior is meant to be shared between different application contexts, they might have customizations for enabling a
specific application flow, assuring the user can distinguish which context they are navigating into.

---

### Home Page

The Home Page context provides the following functionalities:

#### A "Recent Activity" dashboard:

* Shows a set of simple graphics for the user's activity in the past 30 days;

#### A "Recent Tasks" section:

* Initially shows the 5 most recent created tasks which are not marked as complete;
* Has a filter for switching between assigned categories between tasks, showing the most recent tasks per category;
* Each task can be marked as completed;
    * An option for checking all user-created tasks;
    * An option for creating a new task;

#### An "Upcoming Events" section:

* Shows the upcoming events of the current month, grouped by period (e.g. "12/07 - 18/07");
* An option for checking all events;
* An option for creating a new event in the Agenda;

#### A "Sticky Notes" Dropdown:

* Shows the 5 latest user-created notes;
* An option for checking all user-created notes;
* An option for creating a new sticky note;

---

### Tasks Page

The Tasks Page context provides the following functionalities:

#### A section with all user's created tasks:

Each task can be edited, marked as complete or deleted.

#### An option for creating a new task:

A form collects all the task data and perform basic validations.

#### An option for editing an existing selected task:

A form renders with the selected task data, enabling the user to update any given field.

#### An option for deleting a selected task

A confirmation dropdown is shown for warning the user about the action.

#### A filter for showing tasks based on user preferences:

> - Show/Hide tasks of a specific category;
> - Show/Hide tasks marked as `complete`;
> - Sort tasks by a given criteria;
> - Search tasks by title or description;

By default, completed tasks are moved to the `Complete` category.

---

### Events Page

The "Events" page context provides the following functionalities:

#### A section listing all upcoming events 

 Upcoming events are grouped by period. By default, all events that may have a date time gap under one week between each other are grouped and labeled within a "period" label, starting from the earliest to the latest. E.g.: `17/07 - 23/07`

#### A filter for searching for specific events

> * A set of user controls lets the user search for a created event with a given set of criteria. Its exhibition is also adjustable upon the user preferences.
> * Events can be directly edited or deleted through the search results

#### An option for adding a new event to the agenda

 A form renders with the required data for creating a new event.

#### A section listing all the previous events

 All events registered in past dates are displayed here. It works just as the "Upcoming Events" section was previously described.

---

### Notes Page

The "Notes" page context provides the following functionalities:

#### A notes section display all user's created notes

A list displaying all notes created by the user. The notes are sorted by their creation dates by default. User interaction might change this behavior. 

> Notes also have an option to be "fixed" in the user's screen. They will stay visible to the user even if the application window is minimized.

Notes can also be edited or deleted upon user interaction. These actions have no confirmation warning.

#### An option for creating a new note

A form is rendered upon user interaction with all required fields for creating a new note. Basic validations are applied to given form fields.

---

### Settings Page

The "Settings" page provides the following functionalities:

#### A "UI Settings" section

This section lets the user customize some UI-related behavior such as:
* Themes;
* Displayed sections in the "Home" page;
* Item count to be rendered for each section of the "Home" page;

#### A "User Settings" section

This section lets the user customize general application behavior such as:
* Application language;
* Username;