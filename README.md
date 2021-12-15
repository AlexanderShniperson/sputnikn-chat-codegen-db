# SputnikN chat codegen DB
A database generator for chat server

### The idea
Generating code from a database schema is used to avoid writing unnecessary code by a programmer to access database objects, speed up project work and focus on business logic.

### What to do
Restore database:
- schema from `src/schema/database.sql` into database named `sputniknchat`;<br>
- data from `src/schema/data.sql` into database named `sputniknchat`;

To generate database layer objects just do below<br>
Run in project directory: `gradle -Pgendb build -x test` or `./gradlew -Pgendb build -x test`<br>
After generation the target classes will be copied to destination project.