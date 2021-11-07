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
pipenv install -r requirements.txt
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
will be available on http://localhost:8000

Superuser django:
username: benha
paasword: benha

Deployment
On heroku: https://floating-wildwood-31941.herokuapp.com/

Database
Is written on SQLite3. 

Postman

Create user:
POST   /users/

Write message:
POST /messages/

Get all messages for a specific user:
GET  /all-messages/user-id/

Get unread messages for a specific user :
GET   /unread-messages/user-id/

Read message ( mark read in the database)
GET  /read-messages/message_id/

Delete message
DELETE  /messages/message_id/
