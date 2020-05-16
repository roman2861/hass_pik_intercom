Плагин для поддержки линейки домофонов Рубитек, установленных в некоторых ПИКовских домах.
---
Для авторизации используются логин (телефон) и пароль, используемые для управления домофоном в приложении Домофон. Идентификатор устройства _**dev_id**_ лучше поменять, но это не точно.

Для установки плагина поместите содержимое директорию **config/custom_components/pik_intercom**

И добавьте следующую конфигурацию в файл **config/configuration.yaml**

```yaml
pik_intercom:
  login: "+79991234567"
  password: "topsecret"
  dev_id: "00000000-0000-0000-0000-00000000000"

camera:
  - platform: pik_intercom

switch:
  - platform: pik_intercom

stream:
```
Поддерживаемый функционал:
-[x] трансляции с камер
-[x] открытие домофона
-[x] открытие двери без камеры (на лестницу)
-[ ] вызов на домофон (sip)
-[ ] события вызова с домофона


**Пример работы:** ![demo](https://github.com/l0k9j8/hass_pik_intercom/raw/master/demo.png)

