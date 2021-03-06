miitus
=========
A platform for massive group discussion(targeting more than **1000+** people at the same time).
- effectively exchange of opinions.
- next generation voting-like opinion gathering mechanism.
 
##Contents
- [Development](https://github.com/AntXlab/piicebee/edit/master/README.md#Development)

---------

###Development
prepare for web development
```bash
cd client/web/
npm install
bower install
```

prepare for server development
```bash
pip install -r requirement-dev.txt
```

Other dependencies
- npm
- rabbitmq
- cassandra

Start Rest Server
```bash
python run.py
```

Start worker
```bash
celery -A miitus.srv.tasks worker --app=miitus.srv.core:__celery_app --loglevel=info --autoreload
```

Server side testing
```bash
py.test -s -v --cov=miitus --cov-report=html miitus/tests
```

Client side code build
```bash
grunt build
```
You will find a dist folder under client/web/

