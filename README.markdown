CWAC AdapterWrapper: Adding Bits o' Functionality
=================================================

Android comes with a few "wrapper" classes, like `CursorWrapper`,
that make it relatively easy for you to add just a bit of
functionality to an existing object. The wrapper delegates
all behaviors to the wrapped object; you just override the
specific behaviors you need. This works well in cases where
there are many possible underlying implementations, so you
could not robustly accomplish these ends by subclassing.

Android lacks such a wrapper for `ListAdapter`, though. There
is a `WrappedListAdapter` entry in the SDK, but it is an interface,
not an implementation.

So, CWAC offers an `AdapterWrapper` to fill this void.

By itself, it is not terribly interesting. However, other CWAC
projects, like [`EndlessAdapter`][endless] and
[`ThumbnailAdapter`][thumbnail], take advantage of it.

This is packaged as an Android library project, though a simple
JAR is also available from the Downloads section of this
GitHub repository.

Usage
-----
Just extend AdapterWrapper and override whatever adapter-related
methods you wish. By default, all adapter methods delegate to the
wrapped adapter. Your code can get at the wrapped adapter by
calling `getWrappedAdapter()`.

Dependencies
------------
None at present.

Version
-------
This is version v0.4.0 of this module, meaning it is slowly climbing
towards respectability.

Demo
----
There is no demo project. Please refer to
[`EndlessAdapter`][endless] and [`ThumbnailAdapter`][thumbnail]
for examples of using this class.

License
-------
The code in this project is licensed under the Apache
Software License 2.0, per the terms of the included LICENSE
file.

Questions
---------
If you have questions regarding the use of this code, please post a question
on [StackOverflow](http://stackoverflow.com/questions/ask) tagged with `commonsware` and `android`. Be sure to indicate
what CWAC module you are having issues with, and be sure to include source code 
and stack traces if you are encountering crashes.

If you have encountered what is clearly a bug, please post an [issue](https://github.com/commonsguy/cwac-adapter/issues). Be certain to include complete steps
for reproducing the issue.

Do not ask for help via Twitter.

Release Notes
-------------
v0.4.0: converted to Android library project

Who Made This?
--------------
<a href="http://commonsware.com">![CommonsWare](http://commonsware.com/images/logo.png)</a>

[gg]: http://groups.google.com/group/cw-android
[endless]: http://github.com/commonsguy/cwac-endless/tree/master
[thumbnail]: http://github.com/commonsguy/cwac-thumbnail/tree/master
