### Notes, observations, bugs

- Underscore's `_.extend` copies prototypes, Lodash doesn't (also, `_.extend` is an alias to `_.assign`). This breaks `iron:router` initially when trying to call `router.start()`. [Here's a fix](https://github.com/rclai/iron-router/commit/179e6492b74010dc97707ef6f3d5409e10580fad).
