rest_api_demo
=============

Forked from https://github.com/postrational/rest_api_demo

> This repository contains boilerplate code for a RESTful API based on Flask and Flask-RESTPlus.
>
> The code of this demo app is described in an article on my blog:
> http://michal.karzynski.pl/blog/2016/06/19/building-beautiful-restful-apis-using-flask-swagger-ui-flask-restplus/

Running the repo code @2020/03/09 yielded
```
Traceback (most recent call last):
  File "rest_api_demo/app.py", line 6, in <module>
    from rest_api_demo.api.blog.endpoints.posts import ns as blog_posts_namespace
  File "/app/rest_api_demo/api/blog/endpoints/posts.py", line 4, in <module>
    from flask_restplus import Resource
  File "/usr/local/lib/python3.8/site-packages/flask_restplus/__init__.py", line 4, in <module>
    from . import fields, reqparse, apidoc, inputs, cors
  File "/usr/local/lib/python3.8/site-packages/flask_restplus/fields.py", line 12, in <module>
    from werkzeug import cached_property
ImportError: cannot import name 'cached_property' from 'werkzeug' (/usr/local/lib/python3.8/site-packages/werkzeug/__init__.py)
```

So I guess I should change the codez to force `Werkzeug` 0.16.1
... and have some fun
