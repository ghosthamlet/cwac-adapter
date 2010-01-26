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

Usage
-----
Full instructions for using this module are forthcoming. Stay
tuned!

Dependencies
------------
None at present.

Version
-------
This is version 0.1 of this module, meaning it is pretty darn
new.

Demo
----
There is no demo project, other than a stub activity that does
not use the referenced module. Please refer to
[`EndlessAdapter`][endless] and [`ThumbnailAdapter`][thumbnail]
for examples of using this class.

License
-------
The code in this project is licensed under the Apache
Software License 2.0, per the terms of the included LICENSE
file.

Questions
---------
If you have questions regarding the use of this code, please
join and ask them on the [cw-android Google Group][gg]. Be sure to
indicate which CWAC module you have questions about.

[gg]: http://groups.google.com/group/cw-android
[endless]: http://github.com/commonsguy/cwac-endless/tree/master
[thumbnail]: http://github.com/commonsguy/cwac-thumbnail/tree/master