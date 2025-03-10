<img src="https://img.shields.io/badge/dynamic/json?color=41BDF5&logo=home-assistant&label=integration%20usage&suffix=%20installs&cacheSeconds=15600&url=https://analytics.home-assistant.io/custom_integrations.json&query=$.yoto.total">

# yoto_ha

Home Assistant Integration for Yoto.

PRs are appreciated to add more.

![image](https://github.com/cdnninja/yoto_ha/assets/6373468/a02dac1e-609c-4536-9588-9bf5c7bba013)

# Supported Device Features

Not all devices expose all sensors/entities. Only sensors/entities supported by your device will be available in the integration.

|                      | v1  | v2  | v3  | v3e  | mini |
| -------------------- | --- | --- | --- | ---  | ---- |
| Temperature Sensor   | ?   | no  | no  | yes  | no   |
| Night Light          | ?   | yes | yes | yes  | no   |
| Ambient Light Sensor | ?   | yes | yes | yes  | no   |

# Installing

The easiest way to install this integration is via HACS. https://hacs.xyz/

1. Once HACS is installed you add this as a custom repository:

![image](https://github.com/cdnninja/yoto_ha/assets/6373468/7aab0d92-f899-4c21-b51a-d6a5804d04fc)

2. After that you can adjust your HACS filter to not show all integrations and click install.
3. Next you must go to the integration page and "add" the integration to set it up.

# Services Working

- Play/Pause
- Play Media/Card via service call (format of media id is cardid-chapterid-trackid-seconds, if you leave off chapterid/trackid/seconds will start at chapter and track 1.)
- Stop Media via service call
- Set Time for Day/Night Modes
- Set display brightness Day/Night including auto
- Set Day/Night light color, this can be any color not just in app!
- Set Day/Night max volume

# Troubleshooting

You can enable logging for this integration specifically and share your logs, so I can have a deep dive investigation. To enable logging, enable via the gui or update your configuration.yaml like this, we can get more information in Configuration -> Logs page

```yaml config
logger:
  default: warning
  logs:
    custom_components.yoto: debug
    yoto_api: debug
```
