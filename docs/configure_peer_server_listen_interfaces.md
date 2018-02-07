jind allows you to bind to specific interfaces which enables you to setup
configurations with varying levels of complexity.  The listen parameter can be
specified on the command line as shown below with the -- prefix or in the
configuration file without the -- prefix (as can all long command line options).
The configuration file takes one entry per line.

**NOTE:** The listen flag can be specified multiple times to listen on multiple
interfaces as a couple of the examples below illustrate.

Command Line Examples:

|Flags|Comment|
|----------|------------|
|--listen=|all interfaces on default port which is changed by `--testnet` and `--regtest` (**default**)|
|--listen=0.0.0.0|all IPv4 interfaces on default port which is changed by `--testnet` and `--regtest`|
|--listen=::|all IPv6 interfaces on default port which is changed by `--testnet` and `--regtest`|
|--listen=:23099|all interfaces on port 23099|
|--listen=0.0.0.0:23099|all IPv4 interfaces on port 23099|
|--listen=[::]:23099|all IPv6 interfaces on port 23099|
|--listen=127.0.0.1:23099|only IPv4 localhost on port 23099|
|--listen=[::1]:23099|only IPv6 localhost on port 23099|
|--listen=:23102|all interfaces on non-standard port 23102|
|--listen=0.0.0.0:23102|all IPv4 interfaces on non-standard port 23102|
|--listen=[::]:23102|all IPv6 interfaces on non-standard port 23102|
|--listen=127.0.0.1:23103 --listen=[::1]:23099|IPv4 localhost on port 23103 and IPv6 localhost on port 23099|
|--listen=:23099 --listen=:23103|all interfaces on ports 23099 and 23103|

The following config file would configure jind to only listen on localhost for both IPv4 and IPv6:

```text
[Application Options]

listen=127.0.0.1:23099
listen=[::1]:23099
```
