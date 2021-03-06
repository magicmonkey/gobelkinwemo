_This is a fork of the version at `github.com/go-home-iot/belkin` and should be imported as `import belkin "github.com/magicmonkey/gobelkinwemo"`.  This fork adds a callback which gets called as soon as a device is discovered on the network, instead of waiting for the full timeout duration before returning any devices.  To use this, call `ScanWithCallback` instead of `Scan`_

# belkin
A golang library to scan and control Belkin devices, such as the WeMo Maker, WeMo Insight

##Documentation
See [godoc](https://godoc.org/github.com/go-home-iot/belkin)

##Support
This library has only been tested against:
  - WeMo Maker
  - WeMo Insight Switch
  
It may work for the other devices, but has not been tested against them.

##Installation
```bash
go get github.com/go-home-iot/belkin
```

##Package
```go
import "github.com/go-home-iot/belkin"
```

##Testing
Run the unit tests to talk to actual devices.  The tests assume that you have real devices connected to the local network that can be used during testing

```bash
go test
```

or for more detailed responses from the devices
```bash
go test -v
```

##Version History
###0.2.0
Added support for GetBinaryState and GetAttributes calls
###0.1.0
Initial release, support for scanning for belkin devices and TurnOn/TurnOff

