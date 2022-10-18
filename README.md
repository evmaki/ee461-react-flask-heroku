# React/Flask Starter App on Heroku
This is a barebones repo used to demonstrate the setup and deployment of a React/Flask app hosted on Heroku for EE461L, Software Engineering & Design.

## app.py
This contains the Flask backend. The ``/`` route serves up the built React app that is placed in ``/ui/build/`` each time you build the React frontend. You can run the backend by running the following on your command line in the top-level directory:

``flask run``

## /ui
This contains the React frontend. Run ``npm install`` after cloning this repo to install the ``node_modules``. 

Each time you make changes to it, **you need to _manually build it_** by running the following on the command line in the ``/ui`` directory:

``npm run build``

## Suggested Workflow
Follow this suggested workflow as you make changes to increase your chances of success:

1. **Fork this repo**, then clone it using ``git clone https://github.com/yourgithubusername/ee461-react-flask-heroku.git``
2. Open two terminals: one for working on React and another for Flask. We'll call these "React terminal" and "Flask terminal".
3. Install React dependencies. In your React terminal, ``cd ui`` then ``npm install``.
4. Build the React app. Run ``npm run build`` in your React terminal, in the ``ui`` directory.
5. Start the Flask app. Run ``flask run`` in your Flask terminal, in the same directory as ``app.py``.
6. Go to ``localhost:5000`` in your browser. The starter React app page should show up.
7. When you make changes to your React app, **repeat step 4**.
8. When you make changes to your Flask app, **repeat step 5**.
9. When you are ready to deploy:
    - Create a new app on Heroku
    - Connect Heroku to your GitHub account (if you haven't already)
    - Search for this repository under your new Heroku app > Deploy > Connect to GitHub (bottom of the page) and connect to it
    - At the bottom of the Deploy page under Manual deploy, select the main branch and click Deploy Branch
    - If/when deployment fails, view the build log to learn why