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


Deployment
On heroku: https://floating-wildwood-31941.herokuapp.com/

Database
Is written on SQLite3. 

Postman
Write message
POST https://floating-wildwood-31941.herokuapp.com/messages/


Get all messages
GET https://floating-wildwood-31941.herokuapp.com/message

Get unread messages
GET https://floating-wildwood-31941.herokuapp.com/message/unread


Get specific message
GET https://floating-wildwood-31941.herokuapp.com/message/<message_id>


Read message
PUT https://floating-wildwood-31941.herokuapp.com/message/<message_id>


Delete message
DELETE https://floating-wildwood-31941.herokuapp.com/message/<message_id>

