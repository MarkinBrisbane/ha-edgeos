# Changelog

## 2020-05-08 #2

**Fixed bugs:**

- Fix redundant calculation of bits to bytes as data is already bytes    

## 2020-05-08 #1

**Implemented enhancements:**

- Consider away interval can be modified in integration's options, interval is in seconds, default=180

**Fixed bugs:**

- Fix default value of unit in integration's options 

## 2020-05-06

**Fixed bugs:**

- Fix WebSocket disconnections [\#26](https://github.com/elad-bar/ha-edgeos/issues/26)

## 2020-05-02

**Implemented enhancements:**

- Improved device tracker is home logic to consider traffic instead of just DPI report
- Version validation upon adding new integration (Required at least v1.10)

## 2020-05-01

**Fixed bugs:**

- Fix device_tracker didn't work correctly. It is always displayed not home

**Implemented enhancements:**

- More enhancements to options, ability to change setup details
- Support new translation format of HA 0.109.0
- Added __main__.py to root directory for debugging 

## 2020-04-28 #3

**Fixed bugs:**

- Invalid credentials to EdgeOS Router when using IP [\#25](https://github.com/elad-bar/ha-edgeos/issues/25)

## 2020-04-28 #2

**Fixed bugs:**

- Async login without sleep 1 second

## 2020-04-28 #1

**Fixed bugs:**

- Fix disabled entity check throws an exception in logs

## 2020-04-27

**Fixed bugs:**

- Fix disabled entities still being triggered for updates

## 2020-04-26

**Fixed bugs:**

- Fix disabled entities are getting enabled after periodic update (update interval)

## 2020-04-25

**Implemented enhancements:**

- Simplified the way calculating whether device is connected or not, based on report of traffic analysis instead of calculating amount of traffic (bps) over the last 3 minutes [\#24](https://github.com/elad-bar/ha-edgeos/issues/24) 
- Moved service `edgeos.save_debug_data` to Integration -> Options as configuration (that being reset after doing the action once)
- Moved service `edgeos.log_events` to Integration -> Options as configuration to toggle upon need
- Added ability to configure the log level of the component from Integration - Options, more details in README

## 2020-04-20 #2

**Fixed bugs:**

- Fix connection maximum attempts and added keep-alive WS message every 30 seconds [\#21](https://github.com/elad-bar/ha-edgeos/issues/21)

## 2020-04-20 #1

**Fixed bugs:**

- Missing resource for update interval field [\#19](https://github.com/elad-bar/ha-edgeos/issues/19)

## 2020-04-18

**Implemented enhancements:**

- Added changelog
- Added ability to configure update entities interval in seconds (Integrations -> Integration Name -> Options)  [\#19](https://github.com/elad-bar/ha-edgeos/issues/19) [\#15](https://github.com/elad-bar/ha-edgeos/issues)
- Added instructions how to install in HACS [\#16](https://github.com/elad-bar/ha-edgeos/issues/16)
- Added password encryption upon saving the integration settings
- Improved drop-down logic to choose device trackers, monitored devices and interfaces [\#9](https://github.com/elad-bar/ha-edgeos/issues/9)
- Moved code to new file structure
- More logs added for easier debugging

**Fixed bugs:**

- Login failure initiated reconnect mechanism instead of die gracefully 
