# Flask

## Hello World
```python
from flask import Flask

app = Flask(__name__)

@app.route('/hello')
def hello():
  return 'Hello, World!'

if __name__ == '__main__':
  app.run(debug=True)
```

## Routing
```python
@app.route('/hello/<string:name>') # example.com/hello/Tiago
def hello(name):
  return 'Hello ' + name + '!'
```

## Allowed Request Methods
```python
@app.route('/test') #default. only allows GET requests
@app.route('/test', methods=['GET', 'POST']) #allows only GET and POST.
@app.route('/test', methods=['PUT']) #allows only PUT
```

## Configuration
```python
#direct access to config 
app.config['CONFIG_NAME'] = 'config value' 

#import from an exported environment variable with a path to a config file
app.config.from_envvar('ENV_VAR_NAME')
```

## Templates
```python
from flask import render_template

@app.route('/')
def index():
  return render_template('template_file.html', var1=value1, ...)
```

## JSON Responses
```python
import jsonify

def returnstuff():
  num_list = [1,2,3,4,5]    
  num_dict = {'numbers' : num_list, 'name' : 'Numbers'}    
  
  #returns {'output' : {'numbers' : [1,2,3,4,5], 'name' : 'Numbers'}}    
  return jsonify({'output' : num_dict})
@app.route('/returnstuff')
```

## Access Request Data
```python
request.args['name'] #query string arguments
request.form['name'] #form data
request.method #request type
request.cookies.get('cookie_name') #cookies
request.files['name'] #files
```

## Redirect
```python
from flask import url_for, redirect

@app.route('/home')
def home():
  return render_template('home.html')

@app.route('/redirect')
def redirect_example():
  return redirect(url_for('index')) #sends user to /home
```

## Abort
```python
from flask import abort()

@app.route('/')
def index():
  abort(404) #returns 404 error
  render_template('index.html') #this never gets executed
```

## Cookies
```python
from flask import make_response

@app.route('/')
def index():
  resp = make_response(render_template('index.html'))
  resp.set_cookie('cookie_name', 'cookie_value')
  return resp
```

## Session Handling
```python
import session

app.config['SECRET_KEY'] = 'any random string' #must be set to use sessions

#set session
@app.route('/login_success')
def login_success():
  session['key_name'] = 'key_value' #stores a secure cookie in browser    
  return redirect(url_for('index'))
  
#read session
@app.route('/')
def index():
  if 'key_name' in session: #session exists and has key
    session_var = session['key_value']
  else: #session does not exist
```
