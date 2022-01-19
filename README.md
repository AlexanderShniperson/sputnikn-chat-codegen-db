# SputnikN chat codegen DB
A database generator for chat server

### Repositories overview
The chat ecosystem consists of several dependent repositories:<br>
- [Database code gen](https://github.com/AlexanderShniperson/sputnikn-chat-codegen-db) - Class generator according to the DB schema, the DB schema is attached;<br>
- [Transport code gen](https://github.com/AlexanderShniperson/sputnikn-chat-codegen-proto) - Transport message generator between Client and Server;<br>
- [Chat server](https://github.com/AlexanderShniperson/sputnikn-chat-server) - High loaded and scalable chat server written with Akka/Ktor/Rest/WebSocket/Protobuf/Jooq;<br>
- [Client chat SDK](https://github.com/AlexanderShniperson/sputnikn-chat-client) - SDK client chat library for embedding in third-party applications written in Flutter;<br>
- [Sample application](https://github.com/AlexanderShniperson/sputnikn-chat-sample) - An example of a chat application using the SDK client library written with Flutter;<br>

### The idea
Generating code from a database schema is used to avoid writing unnecessary code by a programmer to access database objects, speed up project work and focus on business logic.

### What to do
Restore database:
- schema from `src/schema/database.sql` into database named `sputniknchat`;<br>
- data from `src/schema/data.sql` into database named `sputniknchat`;

To generate database layer objects just do below<br>
Run in project directory: `gradle -Pgendb build -x test` or `./gradlew -Pgendb build -x test`<br>
After generation the target classes will be copied to destination project.