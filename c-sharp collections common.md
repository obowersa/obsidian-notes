Some common dotnet collections:

- System.Collections
	- IEnumerable, IEnumerable\<T>
	- Interrfaces and base classes used by collections

- System.Collections.Generic
	- List\<T>, Dictionary\<T>, Queue\<T>, Stack\<T>
	- Introduced with c-sharp 2.0 and dotnet fm 2.0. Generic type collections

- System.Collections.Concurrent
	- BlockingCollection, ConcurrentDictionary, ConcurrentQueue
	- Collections which are safe to use in multithreaded scenarios

- System.Collections.Immutable
	- ImmutableArray, ImmutableDictionary, ImmutableList, ImmutableQueue
	- Situations where the original collection will never change


All collections implement the ICollection interface, which means they must have a count property

All Collections implement the IEnumerable interface which means they can be iterated using the foreach statement. They must have a GetEnumerator method that returns an object that imeplements IEnumerator

---
Various types support the EnsureCapacity method to optimise performance

---
[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

[[dotnet-collections]]

---

#dotnet #dotnet-2 #dotnet-6