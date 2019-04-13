# modified ESPAsyncWebServer 

The only reason this fork exists is to have ESPAsyncWebServer with ESP8266WebServer.

Both won't compile together due to a naming conflict in 
```
typedef enum {
  aHTTP_GET     = 0b00000001,
  aHTTP_POST    = 0b00000010,
  aHTTP_DELETE  = 0b00000100,
  aHTTP_PUT     = 0b00001000,
  aHTTP_PATCH   = 0b00010000,
  aHTTP_HEAD    = 0b00100000,
  aHTTP_OPTIONS = 0b01000000,
  aHTTP_ANY     = 0b01111111,
} WebRequestMethod;
``` 

As shown above, it compile fine of the members are renamed. 

To allow coexistance of ESPAsyncWebServer with this modified ESPAsyncWebServer it is renamed to ESPAsyncWebServerA, too.


# Get the original

Go to [ESPAsyncWebServer](https://github.com/me-no-dev/ESPAsyncWebServer)
