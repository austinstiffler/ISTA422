#### T-SQL Chapter 10 Homework
#### Austin Stiffler
#### 30 March, 2021
---

1. A *transaction* is a unit of work that might include multiple activities that query and modify data and that can also change the data definition.

1. 
  * **Atomicity** - Either all changes in the transaction take place or none do.
  * **Consistency** - The database must adhere to all integrity rules that have been defined within it by constraints.
  * **Isolation** - Ensures that transactions access only consistent data.
  * **Durability** - After the commit instruction is recorded in the transaction log on disk, the transaction is considered durable even if the change hasn’t yet made it to the data portion on disk.

3. For example, to get an exclusive lock on a row, your transaction must first acquire intent exclusive locks on the table and the page where the row resides.

1. Different types of locks that are used when a transaction is processing. These locks prevent other transactions from querying the table, until the transaction is complete.

1. A transaction request on an incompatible lock on the same resource is blocked if another transaction holds a lock on it, and the requester enters a wait state. The blocked request keeps waiting until the blocker releases the interfering lock. My words: If someone is using a bathroom and another person tries to open the door, the door won't open because the door is locked. The person then has to wait until the bathroom door is unlocked and the person inside finishes.

1. session id, resource type, database id, dbname, res description, resource associated entity id, request mode, request status

1. sessionid, connect_time, last_read, last_write, most_Recent_sql_handle

1. session_id, login_time, host_name, program_name, login_name, nt_user_name, last_request_start_time, last_Request_end_time

1. Isolation levels determine the level of consistency you get when you interact with data.

1. Ann object converts its state to a byte stream, so the byte stream can be reverted back into a copy of the object.

1. When two or more sessions block each other.