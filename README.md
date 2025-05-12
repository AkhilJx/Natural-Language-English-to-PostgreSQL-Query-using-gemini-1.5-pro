# Natural-Language-English-to-PostgreSQL-Query-using-gemini-1.5-pro
This tool allows users to ask questions about a database in plain English. The LLM (Gemini 1.5 Pro) interprets the user's query and converts it into the corresponding PostgreSQL query. This generated query is then executed on the provided database (Neon in this case), retrieving the relevant results, which are displayed to the user.

If the user asks a question unrelated to the PostgreSQL database, the system responds with an error message, prompting them to ask only database-related queries.

Neon is a serverless, open-source, cloud-native Postgres database. It separates storage and compute, which allows for scalability, autoscaling, branching, and lower costs, especially for modern applications and development workflows.

The Key Features of Neon:
Serverless: You don't manage servers — Neon automatically handles provisioning, scaling, and suspending compute resources when idle.

Separation of Storage and Compute: This allows compute resources to scale independently and helps reduce costs when no queries are being run.

Branching: Similar to Git, Neon lets you create branches of your database (e.g., for development, testing, or staging) without copying the full dataset.

Postgres Compatible: It's fully compatible with the PostgreSQL database engine, meaning you can use standard Postgres clients and tools.

Auto-suspend and Resume: Inactive compute instances are automatically suspended to save costs, and they resume when queries are made.

Built-in Storage Snapshots: Useful for creating backups and restoring to previous states.


In practical applications, we typically connect to a hosted database such as PostgreSQL, MySQL, or another SQL-based system. 

For this implementation, the Gemini 1.5 Pro LLM is utilized, which is available for free within usage limits on each Google account. Once these limits are exceeded, users can either upgrade to a paid plan or use a different Google account to continue. 

The psycopg2 library is used to establish the connection with a PostgreSQL database; however, the specific library required may vary depending on the database system in use.
