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


## SAMPLE

```sh:

heroku apps:destroy --app heroku-dusque
heroku-dusque

heroku create heroku-dusque -s cedar --buildpack https://github.com/dbym4820/heroku-buildpack-commonlisp.git

heroku config:add CL_IMPL=ccl --app heroku-dusque

heroku config:add CL_WEBSERVER=hunchentoot --app heroku-dusque

heroku config:add LANG=en_US.UTF-8 --app heroku-dusque

git push heroku master