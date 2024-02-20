# Typescript Notes

### Model, class and interface:

**Definition:**

*   **Model** : It represents the data structure and business logic of an application.
                It encapsulates the properties and methods related to a specific entity or concept
                It used to organize and manage data, making it easier to manipulate and interact with in different parts of the application.

**Example:**
```html

<html>
    <body>
        <h1>Hello </h1>

    <body>
</html>

```

```js
// User Model
export class User {
  id: number;
  username: string;
  email: string;

  constructor(id: number, username: string, email: string) {
    this.id = id;
    this.username = username;
    this.email = email;
  }
}
```












