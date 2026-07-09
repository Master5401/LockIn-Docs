# Privacy Policy for LockIn

**Last Updated:** July 9, 2026

## 1. Information We Collect
To operate our atomic locking engine and render interactive UI components, LockIn only stores the minimum required data in our secure PostgreSQL database:
* **Discord User IDs:** To track who created a poll and who holds an active claim on an option.
* **Discord Channel & Message IDs:** To edit and anchor live ledger updates to the correct Discord message.
* **User-Generated Content:** The text of the questions and options you submit via the `/poll` modal.

## 2. Information We Do NOT Collect
LockIn does **not** collect, read, or store:
* Direct messages (DMs) or message history in your channels.
* Personal identifiable information (PII) such as real names, email addresses, IP addresses, or financial data.
* Any messages outside of the explicit slash commands and button interactions directed at the Bot.

## 3. How We Use Data
Collected data is used strictly for the physical operation of the service:
* Enforcing first-come, first-served exclusivity rules.
* Restoring UI state after server restarts.
* Automatic RAM eviction of mutex locks once a poll's physical duration expires.

## 4. Data Retention and Deletion
* Poll data and associated user IDs are retained in the database to maintain ledger history for server administrators.
* Server administrators may request the complete deletion of their server's historical poll data by opening an issue on our GitHub repository.
* When the Bot is kicked or removed from a server, active UI patches and memory locks are dropped from runtime memory.
