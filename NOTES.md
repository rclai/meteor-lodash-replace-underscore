### Notes, observations, bugs

- Underscore's `_.extend` copies prototypes, Lodash doesn't (also, `_.extend` is an alias to `_.assign`). This breaks `iron:router` initially when trying to call `router.start()`. [Here's a fix](https://github.com/rclai/iron-router/commit/f48d0760120342a9c01c2f44b8b4589d8872f766).
