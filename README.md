OVERVIEW:
* Similar app to twitter to work on creation of flask back end and rendering of homepages on the front end
* Back end: built in flask, routes managed on app.py file, models built on models.py, forms managed with WTForms
* Front end: templates rendered by flask in response to requests.

INSTALLING DEPENDENCIES:
* git pull
* initialize venv -- python -m venv venv, source venv/bin/activate
* pip install -r requirements.txt
* createdb warbler
* createdb warbler_test
* create .env file with SECRET_KEY=abc123 & DATABASE_URL=postgresql:///warbler

TEST NOTES:
* Tests exist for message & user views, user model. Please see test_message_model for reasoning on why tests are not included for those models.

RUNNING TESTS:
* for test_user_views.py file: enter this in command line FLASK_ENV=production python -m unittest test_message_views.py
* for test_message_views.py: FLASK_ENV=production python -m unittest test_message_views.py
* for test_user_model.py: python -m unittest test_user_model.py

TODO - What would I do here with more time?
* more tests: 
    * e.g. When logged in, can I only act on my own account to add / delete messages?
    * how do all views work together?
    * are there message model tests I am missing
* as of now, you only see warbles if you follow somebody. add something that gives "suggested" warbles if you have no more warbles
* Add AJAX with axios so we don't have to refresh the page when you like something
* Allow password changes
* Direct messaging between users
* DRY up templates, URL's, optimize queries
