node-nconf-config
=================

A configured nconf instance for great application configuration.

Supported Files
===============
### defaults.json
Default JSON File. The base configuration, overridden by all of the below.

### environment.json
Environment Specific JSON file. Will override anything set in defaults.json

### vpn.json
VPN Specific JSON file. Will override anything set in environment.json. Only
activated if the special environment variable `VPN` is set to `true`

### Process Variables
Any process variable set will override anything in the specified JSON files. Process variables have a special format so given the following JSON configuration:

```json
{
  "CONFIG": {
    "TEST": {
      "OVERRIDE": "Value"
    }
  }
}
```
The process variable to override the `Value` would be `CONFIG__TEST__OVERRIDE`
