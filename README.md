# arquivo-patcher

Node.JS App that patches Arquivo.pt Web Archives

### Installing

```
npm install
```

### Patchinve Webpages
```
node app/app.js patch --help
```


### Launching with Docker

```
docker build . -t arquivo/patcher --force-rm
docker run -d arquivo/patcher
```
 
### Patching Webpages

```
docker run -it -v "/home/dbicho/Documents/arquivo-patcher/tests/urls.txt:/patcher/urls.txt" arquivo/patcher node app/app.js patch -b 2 -p 2 -i urls.txt
```
