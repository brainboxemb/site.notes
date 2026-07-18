# USB Testing

This page contains tools and resources for controlling USB-connected devices during embedded testing.

## uhubctl

[`uhubctl`](https://github.com/mvp/uhubctl) is a command-line utility for controlling the power of individual ports on compatible USB hubs.

This can be useful for automated testing, for example:

- Power-cycling a device under test
- Recovering a device after a crash
- Testing startup and shutdown behaviour
- Automating tests that normally require unplugging a USB cable

Not every USB hub supports real per-port power switching. A compatible hub must support switching individual ports and must actually disconnect the USB power supply. :contentReference[oaicite:0]{index=0}

## SDWire

[SDWire](https://wiki.tizen.org/SDWire) is a USB-controlled SD card multiplexer.

It allows an SD card to be switched between:

- A host computer
- The device under test

This makes it possible to update an SD card image from a test computer and then reconnect the same card to the embedded device without manually moving it. This is particularly useful for automated testing of devices that boot from an SD card. :contentReference[oaicite:1]{index=1}

## Related Discussion

- [Latest embedded developer gadgets to make our lives easier](https://www.reddit.com/r/embedded/comments/15tesrs/latest_embedded_developer_gadgets_to_make_our/)  
  Reddit discussion containing suggestions for embedded development and testing tools, including switchable USB hubs, `uhubctl` and SDWire. :contentReference[oaicite:2]{index=2}

## Notes

-