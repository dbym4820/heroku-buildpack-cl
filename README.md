Heroku Buildpack for Common Lisp
================================

## How to use

```sh:
? heroku create -s cedar --buildpack https://github.com/dbym4820/heroku-buildpack-commonlisp.git

# Choose implementation:
heroku config:add CL_IMPL=sbcl
# or
heroku config:add CL_IMPL=ccl

# Choose Web Server:
heroku config:add CL_WEBSERVER=hunchentoot
# or 
heroku config:add CL_WEBSERVER=aserve

# Avoid trouble with SBCL source encoding
heroku config:add LANG=en_US.UTF-8

# deploy 
git push heroku master
```