---
description: 'By Jim Waldo, Geoff Wyant, Ann Wollrath and Sam Kendall'
---

# A Note On Distributed Computing

#### The actual paper

{% file src="../.gitbook/assets/waldo-94.pdf" caption="A Note On Distributed Computing" %}

I collected the above paper from [here](https://scholar.harvard.edu/files/waldo/files/waldo-94.pdf)

####  What is in it?

Much of the current work in distributed, object-oriented systems is based on the assumption that objects form a single ontological class. This class consists of all entities that can be fully described by the specification of the set of interfaces supported by the object and the semantics of the operations in those interfaces. The class includes objects that share a single address space, objects that are in separate address spaces on the same machine, and objects that are in separate address spaces on different machines \(with, perhaps, different architectures\). On the view that all objects are essentially the same kind of entity, these differ- ences in relative location are merely an aspect of the implementation of the object. Indeed, the location of an object may change over time, as an object migrates from one machine to another or the implementation of the object changes. 

It is the thesis of this note that this unified view of objects is mistaken. There are fundamental differences between the interactions of distributed objects and the interactions of non-distributed objects. Further, work in distributed object-oriented systems that is based on a model that ignores or denies these differences is doomed to failure, and could easily lead to an industry-wide rejection of the notion of distributed object-based systems.

Quoting  [Michael Feathers](https://michaelfeathers.silvrback.com/bio),

> Abstraction is great but it can only go so far. In this paper, the authors lay to rest what was once a pervasive myth – that we could design a distributed system and make distribution transparent. Ever wonder why you had to implement specific interfaces to do remoting in Java? This is why.
>
> In the aftermath it might seem hard to believe that people thought this was possible. I think we can we partially thank this paper for that.

