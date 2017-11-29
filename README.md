Heroku Buildpack for Common Lisp
================================

## How to use

```sh:
? heroku create application-name -s cedar --buildpack https://github.com/dbym4820/heroku-buildpack-commonlisp.git

# Choose implementation:
heroku config:add CL_IMPL=sbcl --app application-name
# or
heroku config:add CL_IMPL=ccl --app application-name

# Choose Web Server:
heroku config:add CL_WEBSERVER=hunchentoot --app application-name

# Avoid trouble with SBCL source encoding
heroku config:add LANG=en_US.UTF-8 --app application-name

# deploy 
git push heroku master
```