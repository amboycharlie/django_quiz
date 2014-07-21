Django quiz app
===============

This is a configurable quiz app for Django.

I use it to run a few medical revision websites. Here is an [example website](http://www.revisemrcp.com/)

My websites have used twitter bootstrap for the front end and I have tried to strip out anything from
the template files that are dependant on bootstrap.

![Questions](http://i.imgur.com/VRYx3OV.png "Question picture hosted by Imgur")


Current features
----------------
Features of each quiz:
* Question order randomisation
* Storing of quiz results under each user
* Previous quiz scores can be viewed on category page
* Correct answers can be shown after each question or all at once at the end
* Logged in users can return to an incomplete quiz to finish it and non-logged in users can complete a quiz if their session persists
* The quiz can be limited to one attempt per user
* Questions can be given a category
* Success rate for each category can be monitored on a progress page
* Explanation for each question result can be given
* Pass marks can be set
* Multiple choice question type
* True/False question type
* Custom message displayed for those that pass or fail a quiz



![Result page](http://i.imgur.com/UJtRZxo.png "Result picture hosted by Imgur")

Requirements
------------
django-model-utils 2.0.3

It was developed using Django 1.6.5

Installation
------------
Clone the repo with `git clone https://github.com/tomwalker/django_quiz.git`.

Run `pip install -r requirements.txt`.

Add `'quiz', 'multichoice', 'true_false',` to your `INSTALLED_APPS` setting.

    INSTALLED_APPS = (
        ...
        'quiz',
        'multichoice',
        'true_false',
        ...
    )

Add the following to your projects `urls.py` file, substituting `q` for whatever you want the quiz base url to be.

    urlpatterns = patterns('',
        ...
        url(r'^q/', include('quiz.urls')),
    	...
    )



This is my first open source project so please forgive any problems and/or dreadful code!

MIT License (MIT)
Copyright (c) 2012 - 2014 Dr Tom Walker

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
