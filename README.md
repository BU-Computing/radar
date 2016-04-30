# RADAR
### Room Availability Detection (and Reconnaissance).  
A room availability display for BU Computing.

###### Intro
A simple web app which shows room availability for Poole house 2nd floor labs. Hopefully this will be implemented on a screen in the elevator lobby.

###### How It Works
The application works by drawing an SVG of Poole house 2nd floor and applying HTML tags to each individual room. When the page is requested, the Flask backend injects json containing room availability into the page before it is rendered, and javascript uses this to color the rooms using their HTML tags. The system also has a small RESTful API so the data can be exposed.

###### Basic Usage
A python script 'manage.py' in the root of the repo is used to control the application.
It can be used to start/stop the web server, create the database, populate data, etc.

To get started, start a terminal and 'cd' into the correct directory, then run:
```
python ./manage.py
```

The app may prompt to install dependencies, which can be done with the following
command:
```
sudo app/deploy/install.sh
```

Executing manage.py will show a list of options. To start the web server type:
```
python ./manage.py runserver
```
...and it will start on 127.0.0.1:5000.

###### Requirements
The app should run on any machine with python. The dependency install script (app/deploy/install.sh) should handle everything.

###### Limitations
Currently, timetable data has been input manually which works but isn't ideal (it only takes a few minutes to do and only changes every once a term, but it's a bit of a pain). There are currently talks with IT Services to provide this data programatically.

###### Contributors
Contributers are welcome. Feel free to make a pull request, although ensure any
changes are sustainable for future use of the application without major support.

###### Future Ideas
* Programatic data access
* Integrate an open source SVG editor to customise drawings
* Consider implementing database editing functionality

###### Authors
Frontend Dev: David Bain [web][web_bain]  
Backend Dev:  Jimmy [web][web_jimmy]

[web_bain]: https://davidba.in
[web_jimmy]: https://jamesbaldwin.co.uk
