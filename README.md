# nova-search-engine-ui

UI for the simple web search engine https://github.com/bh4sith/nova-search-engine

## INSTALL AND RUN

### REQUIREMENTS
This tool requires *Python3+* and the web search engine API (see link above).

### WITH PIP
```
git clone https://github.com/bh4sith/nova-search-engine-ui.git
cd nova-search-engine-ui
pip install -r requirements.txt
```

Then, run the tool :
```
FLASK_APP=index.py HOST=<ip> PORT=<port> flask run --port 80
```
Where :
* `ip` + `port` : route to web search engine API

To run in debug mode, prepend `FLASK_DEBUG=1` to the command :
```
FLASK_DEBUG=1 ... flask run --port 80
```

### WITH DOCKER
build yourself a Docker image :
```
git clone https://github.com/bh4sith/nova-search-engine-ui.git
cd nova-search-engine-ui
docker build -t nova-search-engine-ui .
```
```
docker run -p 80:5000 \
-e "HOST=<ip>" \
-e "PORT=<port>" \
bh4sith/nova-search-engine-ui
```
Where :
* `ip` + `port` : route to web search engine API


## USAGE AND EXAMPLES
To use the search engine, just type this endpoint in your web browser : http://localhost/


## LICENCE
MIT
