# GameLobby

A real-time game lobby: players register, create or join rooms, chat, send private messages and share files.

A rebuild of a university distributed computing assignment (originally WCF + WPF on .NET Framework), ported to a modern stack:

- **Backend:** ASP.NET Core (.NET 10), controllers, SignalR
- **Frontend:** React + TypeScript (Vite)
- **Database:** PostgreSQL (Docker)
- **Later:** Redis backplane for scale-out, GitHub Actions CI

> Work in progress. See `docs/` for requirements and design decisions.
