# ptchemy

## A Simple framework for project

Requirement

* [Python3]()
* [Tornado](http://www.tornadoweb.org)
* [Mako](http://docs.makotemplates.org/en/latest/usage.html)
* [SQLAlchemy](http://www.sqlalchemy.org)
* [FormEncode](http://www.formencode.org/en/latest/Validator.html)

Structure

    you_project/         项目
        __init__.py
        app.py
        settings.py
        libs/
        models/
        handlers/
        templates/
        locale/

## How can I start the application?

At first you should run application server in a terminal:

    cd billfow
    cp settings._py settings.py # setting your config with @YOU
    python3 app.py

If you add template languages, what you should run as below:

    xgettext --from-code=utf-8 -L Python -k_ -j -o ./locale/en_US/LC_MESSAGES/lang.po templaes/*.html

-j will join messages with existing file. So you juest translat the added message in .po, remember generate .mo file:

    msgfmt -o ./locale/en_US/LC_MESSAGES/lang.po ./locale/en_US/LC_MESSAGES/lang.po

Same to `zh_CN` language.

This application server has been running at the port 8080 and you can view the application in your web browser with URL [http://127.0.0.1:8080](http://127.0.0.1:8080).

## License

Copyright (c) 2013 tonsh
