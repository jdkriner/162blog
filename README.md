1 - We are now able to register users:
- app.post('/register', (req, res)) will call registerUser(req, res) function.
- registerUser checks if user exists, if not, it calls addUser()
- add user generates time and creates a new user object. it also returns the new object but we are not doing anything with it.

2 - findUserByUsername and findUserById are used to find users in the users array.

3 - the initial user array looks like this:

let users = [
    { 
        id: 1,
        username: 'SampleUser',
        password: 'sss',
        avatar_url: undefined,
        memberSince: '2024-01-01 08:00' },
    { 
        id: 2,
        username: 'AnotherUser',
        password: 'sss',
        avatar_url: undefined,
        memberSince: '2024-01-02 09:00' },
];

4 - when a user is added through registerUser, it will look like this:

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
    username: 'ali',
    password: 'Hassan',
    avatar_url: undefined,
    memberSince: '2024-05-16 20:19'
  }
]

notice how date was generated in real time and trying to register users that already exist do not add them to this array nor increment the id incorrectly.