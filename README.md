# ioBroker.marstek-venus

ioBroker adapter for Marstek Venus C/D/E energy storage devices. Uses official local UDP Open API.

## Features

✅ Full device auto-discovery on local network  
✅ Real time 1 second polling for all values  
✅ Complete state coverage:
  - Battery status (SOC, temperature, capacity, charge flags)
  - Power values (PV, grid, battery, load)
  - Lifetime energy counters
  - Network status (WiFi, signal strength, bluetooth)
  - Device information

✅ Full control support:
  - Switch operating modes: Auto / AI / Manual / Passive
  - Passive mode power and duration configuration
  - All modes supported exactly as per official API

✅ Supports all Venus models: Venus C, Venus D, Venus E

## Installation

1. Enable Open API in Marstek mobile app and note UDP port (default 30000)
2. Install this adapter via ioBroker admin interface
3. Configure instance:
   - Use Auto discovery (recommended) or enter device IP manually
   - Set UDP port as configured in app
   - Adjust poll interval (default 1000ms)
4. Save and start adapter

## API Reference

Adapter implements 100% of official Marstek Open API Revision 1.0 as documented.

All API methods are implemented:
- `Marstek.GetDevice`
- `Wifi.GetStatus`
- `BLE.GetStatus`
- `Bat.GetStatus`
- `PV.GetStatus`
- `ES.GetStatus`
- `ES.GetMode`
- `ES.SetMode`
- `EM.GetStatus`

## Changelog

### 0.1.0
- Initial release
- Full API implementation
- Auto discovery support
- All operating modes implemented
