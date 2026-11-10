# Game Lobby

# Goal:

Create a game lobby where users can create accounts to join and create chat rooms. Users can change between rooms where they can message and upload files to the room for other users to view, users can also privately message other online users.

# MVP User Stories

As a player I want to be register an account with a unique username and password, accounts being registed should be required to have a unique username and shown an error in the case they don't.
As a player I can log back into my account with my username and password
As a player I want to create rooms for my friends and other users to join. Rooms can not have duplicate names and shouldn't be created if attempted.
As a player I want to be able to a view a list of users in the same room as me
As a player I want to be able to privately message online users in a room. 
As a player I can view a list of active rooms  
As a player I can l logout of my account to protect my account being used  
As a player I can message privately and in the chat room at the same time 
As a player I want to be able to send files in a room

# Later / Out of scope features

## Later

Private messaging online and offline, saved message history, user profiles (profile pictures, about page) Client customisation, create private rooms with password protection, friend system (shows online and offline players the user has added allowing for messaging outside rooms)

## Out of scope

Voice Chat, Mobile apps

# Non Functional Requirements

Chat message should appear for other players within a second  
Chat rooms should hold at least 20 users  
Files should max at 5 mb and only images and documents for now
Users in room should only be able to view said room messages and files

# Current Stack Overview

**Backend:** ASP.NET Core (.NET 10), controllers. Modern replacement for WCF; controllers are what most job codebases use.

**Real-time:** SignalR. 

**Frontend:** React \+ TypeScript (Vite). Replaces WPF; web skills employers ask for.

**Database:** PostgreSQL in Docker. Stores users only (username \+ password hash); runs locally, so nothing pauses.

**In-memory state:** Rooms, messages, files behind interfaces (IRoomStore, IFileStorage). Lost on restart (your choice); can swap to Redis or object storage later without rewriting.

**Auth:** Own register/login \+ PasswordHasher \+ JWT. You build the flow; the framework does the hashing.

**Scaling (later):** Redis backplane, object storage, load balancer. What you’d need to run more than one server.

**DevOps:** Docker Compose, GitHub Actions CI. Standard on job projects.

**Hosting (last):** Decide later (Azure for Students VM is the favourite). Avoids the free-tier pausing problem.

