cmake-debhelper
===============

CMake/CPack is great for quickly packaging for Debian.

However for instance, you may want to package a daemon and let the debhelpers
help you with update-rc.d-calls in your postinst/postrm-scripts or other stuff.
CPack doesn't let you do that out of the box.

**CMakeDebHelper** to the rescue!

The modules in cmake/ can be used for that exactly,
check out the whole repository to see a working example.

Please use out-of-source builds, in-source builds are a bad thing.

    mkdir build && cd build && cmake .. && make package

More information can be found on my blog-post: http://knzl.de/cmake-debhelper/

Debian Packaging reference: http://www.debian.org/doc/manuals/maint-guide/


License
-------

CMakeDebHelper: Copyright (C) 2013 Sebastian Kienzl;
Licensed under the GPL v2, see LICENSE
