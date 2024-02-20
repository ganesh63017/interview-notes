# Typescript Notes

### Model, class and interface:

<!-- **Definition:** -->

*   **Model** : It represents the data structure and business logic of an application.
                It encapsulates the properties and methods related to a specific entity or concept
                It used to organize and manage data, making it easier to manipulate and interact with in different parts of the application.

**Example:**

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

In this example, the User model defines the structure of a user, including properties like id, username, and email. It also has a constructor to initialize these properties when creating a new user instance.
---

*   **Class** : In object-oriented programming, a class is a blueprint for creating objects. It defines the properties and methods that objects of the class will have. In Angular, classes are commonly used to represent models, services, components, and other building blocks of the application.

**Example:**

```js
// User Class
export class User {
  id: number;
  username: string;
  email: string;

  constructor(id: number, username: string, email: string) {
    this.id = id;
    this.username = username;
    this.email = email;
  }

  getFullName(): string {
    return `${this.username} (${this.email})`;
  }
}
```

Now, the User class not only includes properties but also a method (getFullName()) to retrieve the full name of the user. This demonstrates how a class can encapsulate both data and behavior.

---










