# Architecture Decision Log

**Written by the learner**, reviewed by the mentor. These entries are your interview talking points:
"Why did you do X?" Answer here first.

Template:
```
## NNN — <decision title> (YYYY-MM-DD)
Context: what problem or choice came up?
Options considered: at least two
Decision:
Why: trade-offs, what you gave up
Would revisit if:
```

---

Decision 1: Changing from WCF/WPF to ASP.NET Core and React
Changed to core and react as they are current and common frameworks and libraries and allow for cross platform use rather than just windows

Decision 2: SingalR only, no polling client
Polling client was built originally for the purpose of the course to contrast to event-driven architecture which is more efficent and responsive

Decision 3: Postgres for users only: rooms, messages and files in memory behind interfaces
This is chosen to reach a MVP with the matching characteristics to the original assignment, allowing for users to live through restarts but rooms, messages and files to only remain while the server does this is to be done behind interfaces to allow quick changeover without extensive rewriting for later plans when the projects progresses past the inital base and when new features and functionality are to be added like persistent chats etc.