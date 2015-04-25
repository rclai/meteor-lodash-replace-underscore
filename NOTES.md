### Notes, observations, bugs

- Underscore's `_.extend` copies prototypes, Lodash doesn't (also, `_.extend` is an alias to `_.assign`). This breaks `iron:router` initially when trying to call `router.start()`. [Here's a fix](https://github.com/rclai/iron-router/commit/1b3ad3e6339f69a7df4da75942e66de28736974c).
