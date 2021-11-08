Rest API backend system that is responsible for handling messages between users.

A message contains :
1. sender (owner)
2. Receiver
3. Message
4. Subject
5. creation date 


The rest API contains 
- Write message 
- Get all messages for a specific user
- Get all unread messages for a specific user
- Read message (return one message)
- Delete message (as owner or as receiver


Installation locally:
git clone https://github.com/Adassa86/messages-main.git

pip install -r requirements.txt

python manage.py makemigrations

python manage.py migrate

python manage.py createsuperuser

python manage.py runserver

and will be available on http://localhost:8000


Superuser django:
http://localhost:8000/admin
username: benha
paasword: benha


Deployment
On heroku: floating-wildwood-31941


Database
Is written on SQLite3. 


Postman

Create user:
POST   /users/
https://floating-wildwood-31941.herokuapp.com/users/

Write message:
POST /messages/
https://floating-wildwood-31941.herokuapp.com/messages/

Get all messages for a specific user:
GET /all-messages/user-id/
https://floating-wildwood-31941.herokuapp.com/all-messages/1/

Get unread messages for a specific user :
GET   /unread-messages/user-id/
https://floating-wildwood-31941.herokuapp.com/unread-messages/1/

Read message ( mark read in the database)
GET  /read-messages/message_id/
https://floating-wildwood-31941.herokuapp.com/read-messages/1/

Delete message
DELETE  /messages/message_id/
https://floating-wildwood-31941.herokuapp.com/messages/1/
