---
title: "Technical Debt"
header:
  overlay_image: /assets/images/technical-debt.jpg
tags:
---
Regular debt is about owing money. What is owed in technical debt? Engineering effort.

And just like with regular debt, what is owed has to be paid back with interest.

So taking on technical debt immediately relieves us from a certain amount of engineering effort. But eventually we will have to pay it all back. And then some more. 

How does technical debt generate the additional effort?
 - You made a little hack. Someone else used it in their code. Now you refactored your code and want to remove the hack. Nuh, uh, uh! You can't, because there is more code depending on it that needs refactoring.
 - You made a clever workaround and forgot about it. Some time later, you come back to this code with a need to fix a bug or implement a new feature. The workaround was so smart that you don't remember how it worked and now have to figure it out again.
 - And many more similar and familiar situations...

Ok. 

So why would anyone take on technical debt?

❌ Bad reasons to take on technical debt:
 - "We need to meet the deadline"
 - "Work hours end in 10 minutes and I want to finish this PR"
 - "We didn't think of it right away"
 - "It already works"
 - "Feeling lazy"

✅ Good reasons to take on technical debt:
 - You are building a throw-away prototype
 - The software is *very* simple and serves as a small and/or temporary utility
 - You can leverage the loaned time/effort in a way that it brings more value than the technical debt's compounded interest

Ok, so is this a definitive list of when to take on and when not to take on technical debt? Of course no.

Reality is complicated. As always, **it depends**.

There is one hard truth, though, **do not** take on technical debt impulsively.

And if you do take on technical debt:
 - Have a good reason for it
 - Plan when and how to pay it back

