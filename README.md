# ser2net Container

Docker container to run ser2net.

## Usage

This container runs ser2net in the foreground and uses the config file located
at /etc/ser2net.conf.

Be sure to enable any ports or devices as necessary.

Example usage (docker-compose):

```yaml
    version: '3.4'
    services:
      ser2net:
        image: danrue/ser2net:3.5
        volumes:
          - ./ser2net/ser2net.conf:/etc/ser2net.conf
        devices:
          - /dev/serial/by-id/usb-Silicon_Labs_CP2102_USB_to_UART_Bridge_Controller_0001-if00-port0
```
