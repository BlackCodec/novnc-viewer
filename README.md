# novnc-viewer
NoVNC Viewer is a simple bash script for starting novnc server and open browser to server url.

**Latest release:** 20240625.1130

## Requirements

 - NoVnc server (get it [here](https://novnc.com/))
 - A browser
 
## Usage

You need to invoke novnc-viewer specifying target server and target port like any vncviewer.

The difference is that novnc-viewer accept only the followind optional parameters:

 - -d or --debug: enable debug messages

All novnc logs are written on /tmp/vnc-<novnc_server_port>.log

## Installation

Copy novnc-viewer in any folder you prefer and make it executable (```chmod +x ./novnc-viewer```).

## Configuration

Edit the novnc-viewer file with your preferred editor, you can change the following variables:

 - first_port: is the first port that the novnc-viewer check if it is free and start novnc on this port. If the port is in use, increment by one and recheck. (Default: 6001)
 - close_timeout: if no connection is received after timeout the server will be stopped. Units is seconds, default 5 minutes. (Default: 300)
 - browser\_cmd: the browser command to invoke. (Default: firefox)
 - novnc\_cmd: the novnc command to invoke. (Default: novnc_proxy)
 
## Release: 
 - 20240625.1130:
   - First release

