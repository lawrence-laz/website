---
title: "Misapplied design principles: DRY"
header:
  overlay_image: /assets/images/technical-debt.jpg
tags:
---

DRY is an acronym for don't repeat yourself. What it means and promises.
It's not a bad principle. When done right it can do X and Y.

However, it can oftentimes be misapplied. We humans are very good at looking for patterns. Sometimes so much as to find patterns where there are none.
What happens is you see a few pieces of blocks that look alike and start looking for a ways to deduplicate it.
On a good day you might end up with a small function that now is being called from those few places.
On a bad day you might end up with an abstract base class that has multiple implementations, each for the part that was just so very slightly "different".
(don't go with negative opinion so early)

what I mean by a pattern that is not really there is: the two pieces of code have simillar requirements but coming from different sources, and the requirements are subject to change at which point the deduplicated code no longer fits both cases.

At this point if you're lucky, some voice inside you will admit that this was a mistake and you will remove the extracted code and just get back to each place having its own implementation.
If you are not prone to these "inside voices" you might just end up commiting to the extracted abstraction and just put in some more effort to get it to work. If it doesn't fit you just need to push it a little harder, right?

now let's take a step back and try to dig up the reason why we made the change to begin with.
Was it because there were two places where code looked alike? That's not a real problem. As long as your code reads well and
you are not having problems maintaining it, that is.

the principle is good when: two places are unlikely to go out of sync, you should use it to solve a problem in code when things become difficult to maintain or understand.

The principle is not good when applied for it's own reasons.

Do not deduplicate code with a reason "Make code more DRY";


Extract a function, slap a message "Make code more DRY", and push. Hope noone chokes on the dryness.


