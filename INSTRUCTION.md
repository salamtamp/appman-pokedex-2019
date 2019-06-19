# INSTRUCTION

## Business Requirements

- Create both `frontend` and `backend` for `Pokedex` application with Node.js
- `Pokedex` applications contains 5 pages which are `Pokedex Login`, `Pokedex Registration`, `Pokedex List`, `Pokedex Information` and `Add Pokemon to Pokedex`
- Called page that required authentication a `Private` page, otherwiser called it `Public` page

### Registration

- `Public` page
- Normal registration form contains 2 fields which are `username` and `password` and a submit button
- `password` field must be masked
- After submit registration form redirect to `Login` page
- After registration success user will receive an empty `Pokedex`

`SCREENSHOT: REGISTRATION PAGE`

### Login

- `Public` page
- Normal login form contains 2 fields which are `username` and `password` and a submit button
- `password` field must be masked
- After submit login form redirect to `List` page.
- Fallback page when authentication failed

`SCREENSHOT: LOGIN PAGE`

### List

- `Private` page
- Contains all `Pokedex` cards of all users.
- Each card contains `username` of it's owner
- Each card links to it's own `Information` page
- Fallback page when authenticated

`SCREENSHOT: LIST PAGE`

### Information

- `Private` page
- Contains `username` and all `Pokemon` in  `Pokedex`
- Contains link to navigate to `Add Pokemon` and `List` pages
- Each `Pokemon` in `Pokedex` is displayed in a card that contains it's `name`, `image`, `HP`, `attack`, `resistance` and `type`
- Link to `Add Pokemon` is present only when authenticated user is it's `Pokedex` owner

`SCREENSHOT: INFORMATION PAGE`

### Add Pokemon

- `Private` page
- Contains `search` field which receive text and filter `Pokemon` by `name` and `type` (`name` has higher `priority`)
- Contains link to navigate to it's `Information` page
- Each `Pokemon` in search result is displayed in the same card with card in `Information` page but contains `Add` button to add `Pokemon` to `Pokedex`

`SCREENSHOT: ADD POKEMON PAGE`

## Technical Requirements

- The application must separate `frontend` and `backend` into a different application

### `frontend`

- `frontend` application must be built by modern frontend JavaScript library / framework such as `React.js`, `Vue.js`, `Angular.js`, etc with concept of `SPA`
- `frontend` application must compatible with only `1024px` screen size (No responsive needed)

### `backend`

- `backend` application must be build by modern Node.js library such as `Express`, `Koa`, `Hapi`, `Loopback`, etc with concept of `RESTful API`
- `backend` application must connect with database
- Database can be SQL, NOSQL, etc
- All request must be log to `stdout` in `development` environment and to `production.log` file in `production` environment (All sensitive data must be masked)

## Hint

- `Pokemon` data can be found in [pokemon.json](./seeds/pokemon.json)
