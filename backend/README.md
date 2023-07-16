# Django Backend
### Setting up virtual environment
1. Create a virtual environment and activate it:
```
/root/of/backend $ python3 -m venv .venv
/root/of/backend $ source .venv/bin/activate
```
2. Make sure the version of your pip is 23.0.1:
```
(.venv) $ pip --version
pip 23.0.1 from /root/of/backend/.venv/lib/python3.8/site-packages/pip (python 3.8)
```
3. Install all dependencies:
```
(.venv) $ pip install -r requirements.txt
```
Deactivate virtual environment if needed:
```
(.venv) $ deactivate
```
Tips:
1. Display dependencies as a tree: `(.venv) $ pipdeptree -fl`
2.

### Setting up PYTHONPATH
Add the path of `backend` to your `~/.bash_profile`
```
export PYTHONPATH=$PYTHONPATH:/root/of/backend
```
### Setting up MySQL database
1. Start the MySQL server:
```
$ brew services start mysql
```
2. Set the root password to be `pass1234`:
```
$ mysqladmin -u root password pass1234
```
3. Log in as the root user:
```
$ mysql -u root -p
```
4. Create database `shiba_nearby`:
```
mysql> CREATE DATABASE shiba_nearby;
```
5. Bring database up to date:
```
(.venv) $ /root/of/backend $ python manage.py migrate
```
### Running app locally
Run app in development mode:
```
/root/of/backend $
/root/of/backend $
```
