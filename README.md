# Test-DB-backup
A fragment of the database that can be restored on your local development environment for EGTA developers. This part should be executed once you have set up the local dev copy up to restoring the db schema.

Here is a little bit of data to work with. Unzip the folder, and then run: `pg_restore -Fd -d egtaonline3_development db.dump3`

If you get errors, you can try 
`pg_restore -Fd -c -d egtaonline3_development db.dump31` but this might delete your user.

If it does, pull up the rails console and do

`User.create!(email: "put your email in here", password: "put your password in here", password_confirmation: "put the same password in here", admin: true, approved: true)`
