# Dragit
Experimental application for intuitive file sharing between devices.

The network part is using `libp2p` and custom protocol for file transfer.
The frontend is ran on `gtk-rs`.

## How to build and run?
1) Start the application in two terminals (can be on separate machines in the same network)
```
$ cargo run
```
2) Wait for the two applications discover each other
3) Drag a file and drop it to the drop zone in one of the windows
4) File should be saved to your Downloads folder!

## Performance
Please build in the release mode to get the best performance (roughly 16-20x faster).

```
$ cargo build --release

$ ./target/release/dragit
```

## Bluetooth support
App can use Bluetooth OBEX protocol for file transfer throught the D-Bus BlueZ interface, which should work on most of the Linux devices. (currently disabled)

## TODOs:
- implement error events
- add logging
- add sender side progress bar
- show details about the host
- add confirmation message ("Do you want to accept this file?")
- add files queue
- inject_dial_upgrade_error - but why not inbound?

- adjust network timeouts
- re-enable the Bluetooth
