### Notes, observations, bugs

- Underscore's `_.extend` copies prototypes, Lodash doesn't (also, `_.extend` is an alias to `_.assign`). This breaks `iron:router`.
