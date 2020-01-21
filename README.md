# arquivo-patcher

Patching Arquivo.pt web archived pages using puppeteer to automate browser behavior

### Installing

```
npm install
```

### Patchinve Webpages
```
node app/app.js patch --help

Launch puppeteer to patch arquivo.pt webarchives.

Options:
  --version           Show version number                              [boolean]
  --help, -h          Show help                                        [boolean]
  --num_browsers, -b  The number of browsers instances to use.
                                                           [number] [default: 1]
  --num_pages, -p     The number of tabs pages for each browser instance top
                      use.                                 [number] [default: 1]
  --urls_list, -i     List of urls to patch.
                                          [string] [default: "./tests/urls.txt"]
  --timeout, -t       browsing page timeout            [number] [default: 90000]

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
