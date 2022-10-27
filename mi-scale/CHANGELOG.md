## [0.3.6] - 2022-10-10
### Added
- Added apparmor Security to support Supervised Installation. (Fixes [67](https://github.com/lolouk44/hassio-addons/issues/67) - Thanks @MariusHerget)

## [0.3.5] - 2022-10-10
### Added
- Added extra logging. Logging Level can be set from config file.
- Deprecated options MISCALE_VERSION, TIME_INTERVAL.
### Changed
- Restored HCI settings handling

## [0.3.4] - 2022-10-05
### Changed
- Restored MQTT Discovery. ([fixes #65](https://github.com/lolouk44/hassio-addons/issues/65))
- Removed no longer needed MISCALE_VERSION

## [0.3.3] - 2022-10-03
### Changed
- Restoring handling of V1 scales. ([fixes #64](https://github.com/lolouk44/hassio-addons/issues/64))

## [0.3.2] - 2022-10-03
### Changed
- Fixed missing dbus option. ([fixes #63](https://github.com/lolouk44/hassio-addons/issues/63))

## [0.3.1] - 2022-10-02
### Changed
- Fixed MQTT Config. ([fixes #55](https://github.com/lolouk44/xiaomi_mi_scale/issues/55))

## [0.3.0] - 2022-10-02
### Changed
- Stopped using deprecated/no longer supported bluepy library and replaced with bleak, requiring major code overhaul. ([fixes #59](https://github.com/lolouk44/hassio-addons/issues/59))
- Updated documentation to reflect MQTT integration (moved out of sensor config)
### Breaking Changes
- If using a MiScale V1, make sure you add the MISCALE_VERSION to your options.json file (see doc)

## [0.2.8] - 2022-02-03
### Changed
- Changed time format for datestamp to contain timezone ([fixes #59](https://github.com/lolouk44/hassio-addons/issues/59))

## [0.2.7] - 2022-01-13
### Added
- Added support for Long Term Statistics (HA 2021.9 minimum required)
- Impedance posted to MQTT ([fixes #56](https://github.com/lolouk44/hassio-addons/issues/56))

## [0.2.6] - 2021-06-28
### Changed
- Fixed handling of MQTT_PORT and TIME_INTERVAL

## [0.2.4] - 2021-05-10
### Fixed
- Fixed user lookup by non kg weight (https://github.com/lolouk44/hassio-addons/issues/36)
- Added pre-relase workflow

## [0.2.1] - 2021-05-10
### Changed
- Split README.md into README.md and DOCS.md, revisit and improve content ([PR-37](https://github.com/lolouk44/hassio-addons/pull/37))

## [0.2.0] - 2021-02-11
### Breaking Changes
- Allow any amount of users to be configured (removes limit of three) (based on [PR-18](https://github.com/lolouk44/hassio-addons/pull/18))
- Users need to be added as a list (see config example)
- All users must now provide a GT and LT value
- Try not to overlap ranges - if you do it will ony pick the first one that matches

## [0.1.18] - 2021-02-11
### Changed
- Restored correct code after accepting a PR based on older code in 0.1.17

## [0.1.17] - 2021-02-10
### Changed
- Reduced docker image size
- Added BLUEPY_PASSIVE_SCAN Option to help with some Raspberry Pi devices getting errors like `Bluetooth connection error: Failed to execute management command ‘le on’`
- Fixed config.json startup deprecated option (fixes https://github.com/lolouk44/hassio-addons/issues/32)

## [0.1.16] - 2020-11-26
### Changed
- Fixed MQTT Discovery Message

## [0.1.15] - 2020-11-26
### Changed
- Fixed MQTT Discovery Message

## [0.1.14] - 2020-11-24
### Changed
- 2nd attempt to fix executable files (fixes https://github.com/lolouk44/hassio-addons/issues/23)
- Fixed image links in README file

## [0.1.13] - 2020-11-24
### Changed
- Fixed executable files ~~(fixes https://github.com/lolouk44/hassio-addons/issues/23)~~

## [0.1.12] - 2020-11-23
### Changed
- Fixed workflow for automatic docker images building

## [0.1.11] - 2020-11-23
### Changed
- Remove additional logging for Scale V1 that was used for testing
- Changed timestamp to default python format (fixes https://github.com/lolouk44/xiaomi_mi_scale/issues/29)
- Removed hard-coded 'unit_f_measurement' in the MQTT Discovery (fixes https://github.com/lolouk44/hassio-addons/issues/22)
- Fixed hard coded MQTT Discovery Prefix (fixes https://github.com/lolouk44/xiaomi_mi_scale/issues/35)
- Change measures format to be numbers instead of string where applicable (https://github.com/lolouk44/xiaomi_mi_scale/pull/36)
### Added
- Created workflow to automatically build docker images on new releases (Thanks @AiiR42 for your help)


## [0.1.10] - 2020-09-09
### Changed
- Fixed issue with detection of boolean in MQTT_DISCOVERY (https://github.com/lolouk44/hassio-addons/issues/16 and https://github.com/lolouk44/xiaomi_mi_scale/issues/31)

## [0.1.9] - 2020-09-08
### Changed
- Fixed typo in MQTT message following the **breaking change** to snake_case attributes in 0.1.8

## [0.1.8] - 2020-09-08
### Breaking Changes
- Attributes are now snake_case (fixes https://github.com/lolouk44/xiaomi_mi_scale/issues/24)
### Changed
- Fixed default MQTT Prefix in config.json typo (fixes https://github.com/lolouk44/hassio-addons/issues/6)
- Fixed MQTT Discovery value check to discover
- Changed timestamp to default python format
- Changes the bluetooth reset from reset to down-wait-up (fixes https://github.com/lolouk44/hassio-addons/issues/13)
- Fixed hard coded hci0 to provided hci interface when performing a reset
- Fixed weight in Lbs not detected on Scale V1 (XMTZCO1HM) (fixes https://github.com/lolouk44/xiaomi_mi_scale/issues/28)
- Fixed body calculations for non kg weights
- Updated README
### Added
- Added unit to attributes

## [0.1.7] - 2020-07-06
### Added
- repository.json to make it a real add-on repo (fixes https://github.com/lolouk44/hassio-addons/issues/4)
## Changed
- Now truly handles optional config entries(fixes https://github.com/lolouk44/hassio-addons/issues/3)
- MQTT Discovery set wtih retain flag (fixes https://github.com/lolouk44/hassio-addons/issues/2)
- README updated to use Xiaomi Mi Fit App to retrieve the MAC Address (fixes https://github.com/lolouk44/xiaomi_mi_scale/pull/25)

## [0.1.6] - 2020-07-01
### Added
- Docker Image so install is quicker (no local build required).

## [0.1.5] - 2020-07-01
### Added
- MQTT Discovery Support.

## [0.1.4] - 2020-06-29
### Added
- First release (version in line with non Add-On script for ease of maintenance).
