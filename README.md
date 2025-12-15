# µnit

µnit is a small but full-featured unit testing framework for C, by [Evan Nemerson](https://github.com/nemequ).  It has
no dependencies (beyond libc), is permissively licensed (MIT), and is
easy to include into any project.

For more information, see
[the µnit web site](https://nemequ.github.io/munit).

[![Build status](https://travis-ci.org/nemequ/munit.svg?branch=master)](https://travis-ci.org/nemequ/munit)
[![Windows build status](https://ci.appveyor.com/api/projects/status/db515g5ifcwjohq7/branch/master?svg=true)](https://ci.appveyor.com/project/quixdb/munit/branch/master)

## Installation

Run:
```bash
$ npm i munit.c
```

And then include `munit.h` as follows:
```c
#include "node_modules/munit.c/munit.h"
```

You may also want to include `munit.c` as follows:
```c
#ifndef __MUNIT_C__
#define __MUNIT_C__
#include "node_modules/munit.c/munit.c"
#endif
```

This will include both the function declaration and their definitions into a single file.

## Features

Features µnit currently includes include:

 * Handy assertion macros which make for nice error messages.
 * Reproducible cross-platform random number generation, including
   support for supplying a seed via CLI.
 * Timing of both wall-clock and CPU time.
 * Parameterized tests.
 * Nested test suites.
 * Flexible CLI.
 * Forking
   ([except on Windows](https://github.com/nemequ/munit/issues/2)).
 * Hiding output of successful tests.

Features µnit does not currently include, but some day may include
(a.k.a., if you file a PR…), include:

 * [TAP](http://testanything.org/) support; feel free to discuss in
   [issue #1](https://github.com/nemequ/munit/issues/1)

### Include into your project with meson

In your `subprojects` folder put a `munit.wrap` file containing:

```
[wrap-git]
directory=munit
url=https://github.com/nemequ/munit/
revision=head
```

Then you can use a subproject fallback when you include munit as a
dependency to your project: `dependency('munit', fallback: ['munit', 'munit_dep'])`

## Documentation

See [the µnit web site](https://nemequ.github.io/munit).

Additionally, there is a heavily-commented
[example.c](https://github.com/nemequ/munit/blob/master/example.c) in
the repository.

<br>
<br>


[![ORG](https://img.shields.io/badge/org-nodef-green?logo=Org)](https://nodef.github.io)
![](https://ga-beacon.deno.dev/G-RC63DPBH3P:SH3Eq-NoQ9mwgYeHWxu7cw/github.com/nodef/munit.c)
[![SRC](https://img.shields.io/badge/src-repo-green?logo=Org)](https://github.com/nemequ/munit)
