# Project Documentation

## 1. User Registration

We are now able to register users:

- `POST /register`: This endpoint calls the `registerUser(req, res)` function.
- The `registerUser` function checks if a user exists; if not, it calls `addUser()`.
- The `addUser` function generates the current time and creates a new user object. It also returns the new object, but we are not doing anything with it currently.

## 2. User Lookup

- `findUserByUsername` and `findUserById` are used to find users in the users array.

## 3. Initial Users Array

The initial user array is defined as follows:

```javascript
let users = [
    { 
        id: 1,
        username: 'SampleUser',
        password: 'sss',
        avatar_url: undefined,
        memberSince: '2024-01-01 08:00' 
    },
    { 
        id: 2,
        username: 'AnotherUser',
        password: 'sss',
        avatar_url: undefined,
        memberSince: '2024-01-02 09:00' 
    },
];
```
## 4. User Addition Example
When a user is added through registerUser, the array is updated as follows:

```javascript
[
  {
    id: 1,
    username: 'SampleUser',
    password: 'sss',
    avatar_url: undefined,
    memberSince: '2024-01-01 08:00'
  },
  {
    id: 2,
    username: 'AnotherUser',
    password: 'sss',
    avatar_url: undefined,
    memberSince: '2024-01-02 09:00'
  },
  {
    id: 3,
    username: 'Hassan',
    password: 'Ali1',
    avatar_url: undefined,
    memberSince: '2024-05-16 20:19'
  },
  {
    id: 4,
    username: 'Ali',
    password: 'Hassan',
    avatar_url: undefined,
    memberSince: '2024-05-16 20:19'
  }
]
```