# Managing Process Overload

> **Company:** Booking.com | **Difficulty:** Medium

---

#### Scenario:
The process count on a production server keeps increasing even though no new workloads were deployed. Zombie processes are accumulating in the system.

#### Task:
Find all zombie processes, kill their parent processes to remove the zombies, and confirm they are gone from the system.

####  Expected Output:

No leftover or defunct processes should be left after the fix.
