---
title: "Black Box Testing"
header:
  # image: /assets/images/technical-bet.jpeg
published: false
tags:
  # - software design
---

- Tests are for testing behavior, not implementation.
    As long as the software behaves as we need it, the tests shouldn't care how it's implemented.
    This is black box testing. We test using the the outer layer that is exposed to us.
    This enabled refactorings, where changing a class, be it a merge or a split, doesn't break the tests, as long as the
    code after refactoring provides same functionality.
    > If something breaks, I want to be told and if nothing breaks I don't want to be interrupted -Kent Beck, https://twitter.com/KentBeck/status/1182776914001268738
- The enablement of refactorings is crucial to having good design and architecture for an evolving software project.
    Note that for single-off projects and prototypes this is not important, if you code a thing and never touch it
    good design doesn't matter, as computer will be the only one reading it.


