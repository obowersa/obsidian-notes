c-sharp supports both structs and classes

Structs:
- Value types, allocated on the stack or inline in containing types
- Allocations and deallocations are cheaper
- In structs, each variable contains it's own copy of the data

Classes:
- Reference types allocated on the heap
- Assigningment of large reference types is cheaper
- static/etc can persist across classes


structs are useful for small, short lived or embeded objects

---
#dotnet 