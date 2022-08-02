Dotnet has a few different ways of deploying
-Framework-dependant deployment (FDD)
-Framework-dependant executables(FDE)
-Self contained

FDD: A dll which relies on the dotnet CLR being installed, running the dll directly
FDE: An executable which relies on .NET being installed on the system
Self Contained: A bundled executable which contains the runtime as well

To publish a self contained app, you can specify a rid using the -r switch on dotnet publish
---
Dotnet uses RID's (run time identifiers) to mark where something can run

---
from dotnet 5.x onwards, you can use trimming to rduce the side This can be done either with a PublishTrimed setting in the project file, or, -p:PublishTrimmed=True on the CLI

From dotnet 6, you also have link trim mode

---

[[C Sharp 10 and .NET 6 – Modern Cross-Platform Development - Sixth Edition]]

---
#dotnet #apple-arm #dotnet-5 #dotnet-6