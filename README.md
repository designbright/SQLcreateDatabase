Use a PostgreSQL database
Create and use a PostgreSQL database for storing todo items.

Create a PostgreSQL database called todolist with a table called todos to be used for storing todo items.

Each item should have the following fields:

id -- a serial primary key
title -- not optional, string up to 255 characters
details -- optional, holds a large amount of text
priority -- not optional, an integer. Default is 1.
created_at -- not optional. A date and time.
completed_at -- optional. A date a time.

In a file called todo.sql:

Write the CREATE TABLE statement to make this table.
  CREATE TABLE todo (
    id SERIAL PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    details VARCHAR(9000) NULL,
    priority INTEGER DEFAULT 1 NOT NULL,
    created_at TIMESTAMP NOT NULL,
    completed_at TIMESTAMP NULL
  );

Write INSERT statements to insert five todos into this table, with one of them completed.
  INSERT INTO todo (
  title,
  details,
  priority,
  created_at,
  completed_at
  ) VALUES (
  'Clean Bathroom',
  'bathroom is super dirty, it needs cleaning',
  2,
  TO_TIMESTAMP('2017-08-07 07:03:56', 'YYYY-MM-DD HH24:MI:SS'),
  NULL
  );

  INSERT INTO todo (
  title,
  details,
  priority,
  created_at,
  completed_at
  ) VALUES (
  'Complete TIY Projects',
  'robots and sqldatabases',
  2,
  TO_TIMESTAMP('2017-08-07 11:59:09', 'YYYY-MM-DD HH24:MI:SS'),
  NULL
  );

  INSERT INTO todo (
  title,
  details,
  priority,
  created_at,
  completed_at
  ) VALUES (
  'walk dog',
  'big loop',
  1,
  TO_TIMESTAMP('2017-08-07 02:32:07', 'YYYY-MM-DD HH24:MI:SS'),
  NULL
  );

  INSERT INTO todo (
  title,
  details,
  priority,
  created_at,
  completed_at
  ) VALUES (
  'be nice to people',
  'karma',
  3,
  TO_TIMESTAMP('2017-08-07 03:45:43', 'YYYY-MM-DD HH24:MI:SS'),
  NULL
  );

  INSERT INTO todo (
  title,
  details,
  priority,
  created_at,
  completed_at
  ) VALUES (
  'apply for jobs',
  'but not at thoughtbot or pendo',
  1,
  TO_TIMESTAMP('2017-08-07 01:24:40', 'YYYY-MM-DD HH24:MI:SS'),
  TO_TIMESTAMP('2017-08-07 12:05:29', 'YYYY-MM-DD HH24:MI:SS')
  );

  INSERT INTO todo (
  title,
  details,
  priority,
  created_at,
  completed_at
  ) VALUES (
  'finish homework',
  'data is kewl',
  2,
  TO_TIMESTAMP('2017-08-10 08:45:40', 'YYYY-MM-DD HH24:MI:SS'),
  NULL
  );

  INSERT INTO todo (
  title,
  details,
  priority,
  created_at,
  completed_at
  ) VALUES (
  'finish branding icons',
  'upload new font to computer',
  2,
  TO_TIMESTAMP('2017-08-10 08:45:40', 'YYYY-MM-DD HH24:MI:SS'),
  NULL
  );

Write a SELECT statement to find all incomplete todos.
  SELECT FROM todo WHERE completed_at IS NULL;

Write a SELECT statement to find all todos with a priority above 1.
  SELECT * FROM todo WHERE priority > 1;

Write an UPDATE statement to complete one todo by its id. Your ids may differ, so you will choose the id to up.
  UPDATE todo SET completed_at = TO_TIMESTAMP('2017-08-09 03:35:27', 'YYYY-MM-DD HH24:MI:SS') WHERE id = 5;

Write a DELETE statement to delete all completed todos.
  DELETE FROM todo WHERE title = 'Clean Bathroom';
# SQLcreateDatabase
