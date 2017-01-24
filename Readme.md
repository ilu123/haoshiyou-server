# Haoshiyou-Server, an API server for [haoshiyou.org](http://haoshiyou.org)

Powered by StrongLoop/ApiConnect

## Quick Start

1. Start the MySQL server on your MacBook

2. Start the Server

  - Though GUI, first run `apic edit` in `haoshiyou-server` folder, 
    then open a browser to go to `http://127.0.0.1:9000/`, 
    click the "<b>Run</b>" button on the bottom, and
    then query the server by

    ```bash
    curl --request GET \
      --url 'https://localhost:4002/api/HsyListings' \
      --header 'accept: application/json' \
      --header 'content-type: application/json' \
      --header 'x-ibm-client-id: default' \
      --header 'x-ibm-client-secret: SECRET' \
      --insecure
    ```

  - Through CLI, run `npm start`, and then query the server by

    ```bash
    curl --request GET \
      --url 'http://localhost:3000/api/HsyListings' \
      --header 'accept: application/json' \
      --header 'content-type: application/json' \
      --header 'x-ibm-client-id: default' \
      --header 'x-ibm-client-secret: SECRET' \
      --insecure
    ```


## Working with Ionic

 1. Generate Angular2 SDK

    ```bash
    ./node_modules/.bin/lb-sdk server/server \
    <client source code> \
    -d ng2web -i disabled -v enabled
    ```

 for example

    ```bash
    ./node_modules/.bin/lb-sdk server/server \
    ../haoshiyou-dev/haoshiyou/src/loopbacksdk \
    -d ng2web -i disabled -v enabled
    ```
