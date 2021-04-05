Simple TLA+ 1 bit clock

TLA+ example:
```
VARIABLE clock
Init == clock \in {0, 1} //Clock can be any value in set 0,1
Tick == IF clock = 0 THEN `clock = 1 ELSE `clock = 0 //Transitions between states for clock
Spec == Init  /\ [][Tick]_<<clock>> // Spec to validate clock
```
PlusCalc example:
```
--fair alogirthm OneBitClock() {
variable clock \in {0, 1}; // Translates to the init step in our TLA+ example
{
	while (TRUE) {
		if (clock = 0) 
			clock := 1
		else
			clock := 0
		}
	}
}
```
---
https://sriramsami.com/tlaplus/