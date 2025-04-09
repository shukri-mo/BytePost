# 📝 Byte Post

This project demonstrates how to use **React Context** and **custom hooks** to manage a list of posts. It includes functionality for searching, adding, and clearing posts. The posts are generated using the [`@faker-js/faker`](https://github.com/faker-js/faker) library to simulate realistic-looking content.

## ⚙️ Features

- 🔄 Automatically generates 30 random posts on load
- 🔍 Search functionality that filters posts by title and body
- ➕ Add new posts manually
- 🧹 Clear all posts
- 📦 Clean and scalable architecture using the Context API and the custom hook `usePosts`

---

## 🧠 How It Works

### `PostContext.js`

- **`PostProvider`**: A context provider component that wraps your application and holds the core post logic. It manages the state of posts, the search query, and provides functions to add, clear, and filter posts.

- **`usePosts()`**: A custom hook that allows components to access the context values. It simplifies consuming the context’s state and actions within functional components.

### Context Values Provided

| Key              | Description                                        |
|------------------|----------------------------------------------------|
| `posts`          | The list of posts filtered based on the `searchQuery`. |
| `onAddPost()`    | Adds a new post to the list.                       |
| `onClearPosts()` | Clears all posts from the list.                    |
| `searchQuery`    | The current search query, used for filtering posts. |
| `setSearchQuery` | A function to update the `searchQuery`.            |

### Derived State

The `searchedPosts` value is derived from the `searchQuery`. If the search query is not empty, it filters the posts based on the title and body. If the query is empty, all posts are shown.

---

## 📚 What I Learned

- **React Context API**: I gained a deeper understanding of the Context API and how to use it for state management across the app. I learned how to create a global context, manage shared state, and provide functionality (like adding and clearing posts) throughout the component tree.
  
- **Custom Hooks**: I learned how to build custom hooks like `usePosts()` to encapsulate logic and manage context state more efficiently in functional components.

- **Derived State**: I understood the importance of derived state and how to use computed values (like `searchedPosts`) to filter or transform data before rendering, which helps in keeping the state more organized and optimized.

- **Cleaner Architecture**: This project helped me appreciate the importance of clean and scalable architecture when building React applications. Using Context for global state management and custom hooks for logic encapsulation made the codebase more modular and maintainable.

- **Searching and Filtering**: I learned how to implement search functionality that dynamically filters data (in this case, posts) based on user input, enhancing the user experience.

---
