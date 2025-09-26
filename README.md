# `ethOS` #####################################################################
<div style="margin-left=4em; font-style=italic">
&mdash; the one true nanokernel &mdash;
</div>

## About ##

`ethOS` is an ultra-light OS made from scratch to handle millions of concurrent
processes without latency using two-level scheduling (RR and aging MLFQ, to be exact).

It is hevily inspired by NetBSD, seL4 and Plan 9 from Bell Labs.

The kernel itself is _incredibly small_ (nanokernel) and handles little more than context switching,
IPC (which, for performance, is never used), drivers, `syscall`s, and scheduler all run on userspace,
and userspace is also relatively _light_ (still somewhat bigger that getting Linux and removing all
utils for your own).

`ethOS` is also formally proven, and safe. Kernel cannot corrupt user memory and vice-versa.

## Why? ##

> How do you even reach a point this is neccessary?

**TL;DR: Mission critical systems.**

If you worked with embedded systems, you know these often have little power, and sometimes (more _rare_
nowadays), **mission-critical software** is built with these, and there you need to both (1) ensure safety
and (2) squeeze every single cycle, and usefully use it.

## Licensing ##

`ethOS` was made by Mario Rosell <mar1lusk1@proton.me> is under the public domain
([The Unlicense](https://unlicense.org/)), do whatever you want.

## Also read ##

+ `README-ES.md` &mdash; Spanish translation of this readme.
+ `CODE_OF_CONDUCT.md` &mdash; A (_global_) code of conduct you should follow.
+ `HACKING.md` &mdash; Learn to contribute to `ethOS`.
+`LICENSE` &mdash; As aforementioned, public domain.

