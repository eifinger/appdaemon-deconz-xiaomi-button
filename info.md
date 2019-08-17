{% if prerelease %}
# This is a Beta version!
---
{% endif %}

{% if version_installed != selected_tag %}
# Changes as compared to your installed version:

## Breaking Changes

## Changes

## Features

## Bugfixes

---
{% endif %}

# appdaemon-deconz-xiaomi-button

[![GitHub Release][releases-shield]][releases]
[![GitHub Activity][commits-shield]][commits]
[![License][license-shield]](LICENSE.md)

[![hacs][hacsbadge]](hacs)
![Project Maintenance][maintenance-shield]
[![BuyMeCoffee][buymecoffeebadge]][buymecoffee]

_App which toggles entities for single/double/hold presses of Xiaomi buttons connected via deconz_

## App configuration

```yaml
DeconzXiaomiButton Lobby:
  module: deconz_xiaomi_button
  class: DeconzXiaomiButton
  id: lobby_switch
  actor_single: light.lobby
```

key | optional | type | default | description
-- | -- | -- | -- | --
`module` | False | string | `deconz_xiaomi_button` | The module name of the app. There shouldn't be any reason to change this.
`class` | False | string | `DeconzXiaomiButton` | The name of the Class. There shouldn't be any reason to change this.
`id` | True | string | | The id of the xiaomi button.
`actor_single` | True | string | | The entity_id to toggle on a single button press.
`actor_double` | True | string | | The entity_id to toggle on a double button press.
`actor_hold` | True | string | | The entity_id of the light to dim up when holding the button.

---

<a href="https://www.buymeacoffee.com/eifinger" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/black_img.png" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;" ></a><br>

***

[buymecoffee]: https://www.buymeacoffee.com/eifinger
[buymecoffeebadge]: https://img.shields.io/badge/buy%20me%20a%20coffee-donate-yellow.svg?style=for-the-badge
[commits-shield]: https://img.shields.io/github/commit-activity/y/eifinger/appdaemon-deconz-xiaomi-button?style=for-the-badge
[commits]: https://github.com/eifinger/appdaemon-deconz-xiaomi-button/commits/master
[hacs]: https://github.com/custom-components/hacs
[hacsbadge]: https://img.shields.io/badge/HACS-Default-orange.svg?style=for-the-badge
[license-shield]: https://img.shields.io/github/license/eifinger/appdaemon-deconz-xiaomi-button?style=for-the-badge
[maintenance-shield]: https://img.shields.io/badge/maintainer-Kevin%20Eifinger%20%40eifinger-blue.svg?style=for-the-badge
[releases-shield]: https://img.shields.io/github/release/eifinger/appdaemon-deconz-xiaomi-button.svg?style=for-the-badge
[releases]: https://github.com/eifinger/appdaemon-deconz-xiaomi-button/releases
