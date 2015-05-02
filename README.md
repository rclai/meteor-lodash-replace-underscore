## Replace Meteor Underscore with Lodash!

This is a drop-in replacement of underscore to lodash, in a non-official way (obviously).

## Installation

Because this is more of a hack than an actual official package, to install it, you just have to:

```
# make sure you have a "packages" folder in your app's root folder
$ cd /your/meteor/app/packages
$ git clone https://github.com/rclai/meteor-lodash-replace-underscore.git
```

That's it.

### How is this different from installing a community package for Lodash?

By including this package as a local package, you essentially make Meteor compile your app with Lodash instead of Underscore. 

When you install a Lodash package, all you've done is install an additional package that doesn't actually replace Underscore, even though you're using Lodash in your app.

### How does this work?

Local packages take presendence over packages (even core packages). 

So by creating a local underscore package you are replacing the underlying underscore.js files with lodash and now your Meteor will use only Lodash files to run your app.

### Why?

- Because [this issue](https://github.com/meteor/meteor/issues/1009) is not going anywhere but simply growing in +1's.
- MDG does not have the resources to take on such a task as it will involve an arduous QA process.
- It is doable with help (PLEASE HELP).

### What now?

I will try to spot and document any quirks I encounter as to how doing this will break Meteor due to they way Underscore and Lodash differ. For example, Underscore's `_.extend` will copy over prototypes where as Lodash's `_.extend` doesn't and therefore `iron:router` won't work properly.

Also, I'll try to see if I can run the Meteor test suite.

### Contributing

It would be awesome if you guys would post issues or pull-requests to the [`NOTES.md`](https://github.com/rclai/meteor-lodash-replace-underscore/blob/master/NOTES.md) file regarding certain issues or errors you've encountered with either Meteor or packages that break as a result of this. Just simply give me the name of the package and the error and I'll document it if you can't look into it.

My hope is that Meteor will get a head start by using this information to (hopefully) transition to Lodash.

### Credit

This code is implemented by using the code from [here](https://github.com/stevezhu/meteor-lodash).
