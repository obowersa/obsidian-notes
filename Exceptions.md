Dotnet supports try/catch exceptions ( which is different from golangs approach).

Some useful notes on it:

Can catch a generic exception with catch (Exception ex). This can then be used in a string.

You can use filtering on exceptions with when. for example:

catch (FormatException) when (amount.containers($)).

This is useful for narrowing down exceptions and handling specific cases

throw ex -> throws with the current stack and loses info
throw -> throws the original stack

---

[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet