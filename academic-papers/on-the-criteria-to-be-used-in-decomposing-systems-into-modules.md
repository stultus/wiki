---
description: >-
  By David Parnas, Department of Computer Science, Carnegie Mellon  University, 
  Pittsburgh, Pennsylvania
---

# On the criteria to be used in decomposing systems into modules

#### The actual paper

{% file src="../.gitbook/assets/criteria\_for\_modularization.pdf" caption="On the criteria to be used in decomposing systems into modules" %}

I collected the above paper from [here](https://www.win.tue.nl/~wstomv/edu/2ip30/references/criteria_for_modularization.pdf) 

#### What is in it?

This paper discusses modularization as a mechanism for improving the flexibility and comprehensibility of a system while allowing the shortening of its development time. The effectiveness of a "modularization" is dependent upon the criteria used in dividing the system into modules. A system design problem is presented and both a conventional and unconventional decomposition are described. It is shown that the unconventional decompositions have distinct advantages for the goals outlined. The criteria used in arriving at the decompositions are discussed. The unconventional decomposition, if implemented with the conventional assumption that a module consists of one or more subroutines, will be less efficient in most cases. An alternative approach to implementation which does not have this effect is sketched.

Quoting  [Michael Feathers](https://michaelfeathers.silvrback.com/bio),

> This is a very old paper, but it is more than a classic. In in it, Parnas introduces a forerunner to the Single Responsibility Principle. He introduces the idea that we should use modularity to hide design decisions – things which could change. People still don’t consider this as often as they should.
>
> Another thing I really like in the paper is his comment on the KWIC system which he used as an example. He mentioned that it would take a good programmer a week or two to code. Today, it would take practically no time at all. Thumbs up for improved skills and better tools. We have made progress.







