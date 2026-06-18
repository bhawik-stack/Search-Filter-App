# React Interview Assignment - Todo Search & Filter App

## Objective

Build a React application that fetches and displays a list of Todos from a public API. Implement real-time search and filtering functionality.

Estimated Time: **30 Minutes**

---

## Requirements

### 1. Fetch Todo Data

Fetch todos from the following API:

```javascript
https://jsonplaceholder.typicode.com/todos
```

Display the first 20 todos in a list.

Each todo should display:

* Todo ID
* Todo Title
* Completion Status

Example:

```text
1. delectus aut autem
Status: Pending

2. quis ut nam facilis et officia qui
Status: Completed
```

---

## 2. Search Functionality

Add a search input above the todo list.

Requirements:

* Search should work in real-time while typing.
* Search should filter todos based on the title.
* Search should be case-insensitive.

Example:

Search Input:

```text
delectus
```

Expected Result:

```text
delectus aut autem
```

---

## 3. Status Filter

Add a dropdown filter with the following options:

```text
All
Completed
Pending
```

Behavior:

### All

Display all fetched todos.

### Completed

Display only todos where:

```javascript
completed === true
```

### Pending

Display only todos where:

```javascript
completed === false
```

---

## 4. Combined Filtering

Search and Status Filter should work together.

Example:

Search:

```text
qui
```

Filter:

```text
Completed
```

Result:

Only completed todos containing "qui" in the title should be displayed.

---

## 5. Loading State

While data is being fetched:

```text
Loading todos...
```

should be displayed.

---

## 6. Error Handling

If API fails:

```text
Failed to fetch todos.
```

should be displayed.

---

## Expected UI

```text
---------------------------------------------------
| Search Todos...                                |
---------------------------------------------------

Status:
[ All ▼ ]

---------------------------------------------------
| Todo Title                     | Status         |
---------------------------------------------------
| delectus aut autem             | Pending        |
| quis ut nam facilis...         | Completed      |
| fugiat veniam minus            | Pending        |
---------------------------------------------------
```

---

## Technical Requirements

Must use:

* React Functional Components
* useState
* useEffect
* Array map()
* Array filter()
* Fetch API

Do NOT use:

* Redux
* External State Management Libraries
* UI Libraries (Material UI, Ant Design, etc.)

---

## Evaluation Criteria

| Criteria             | Points |
| -------------------- | ------ |
| API Integration      | 20     |
| Search Functionality | 20     |
| Filter Functionality | 20     |
| Code Quality         | 15     |
| State Management     | 15     |
| Error Handling       | 5      |
| UI Structure         | 5      |

Total: 100 Points

---

## Bonus Tasks (Optional)

### Bonus 1

Display counts:

```text
Total: 20
Completed: 8
Pending: 12
```

### Bonus 2

Add debounce (300ms) to search.

### Bonus 3

Add a "Clear Filters" button.

---

