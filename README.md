# QiviconAPI

## API einbinden:

```
<?php
require_once 'lib/riwin/Autoloader_024fc5f605c9d329833c4de0633a3183.php';
$api = new \riwin\QiviconAPI\QiviconAPI("hostname-Homebase", "email@mein.qivicon", "Passwort");
if (isset($_GET['module']) && isset($_GET['cmd'])) {
    call_user_func('\\riwin\\QiviconAPI\\RPCModules\\' . $_GET['module'] . '::' . $_GET['cmd'])->getBody();
}
if (isset($_GET['logout'])) {
    session_destroy();
}
```



## ******************************************
## * Modul - AlarmSystem:
## ******************************************

### * Alarm scharf schalten:
```
    /index.php?module=AlarmSystem&cmd=activateAlarmSystem
```

### * Alarm unscharf schalten:
    /index.php?module=AlarmSystem&cmd=deactivateAlarmSystem

### * Ausgelösten Alarm beenden:
```
    /index.php?module=AlarmSystem&cmd=deactivateAlarm
```

### * Alarm System Eigenschaften anzeigen:
```
    /index.php?module=AlarmSystem&cmd=getAlarmSystemProperties
```


## ******************************************
## * Modul - Generic
## ******************************************

### * Dashboard-Info:
```
    /index.php?module=Generic&cmd=getDashboardInfo
```

### * Homebase Eigenschaften:
```
    /index.php?module=Generic&cmd=getHomeboxProperties
```

### * Räume mit Geräten/Kanälen:
```
    /index.php?module=Generic&cmd=listRooms
```


## ******************************************
## * Modul - Situation
## ******************************************

### * Haushüter an:
```
    /index.php?module=Situation&cmd=activateVirtualResident
```

### * Haushüter aus:
```
    /index.php?module=Situation&cmd=deactivateVirtualResident
```

### * Haushüter Ereignisse:
```
    /index.php?module=Situation&cmd=getVirtualResidentProperties
```

### * Situationen auflisten:
```
    /index.php?module=Situation&cmd=listSituations
```

### * Situation anzeigen:
```
    /index.php?module=Situation&cmd=getSituation&param_id={situationId}
```

### * Situation de- / aktivieren:
```
    /index.php?module=Situation&cmd=setSituationState&param_id={situationId}&param_active={true|false}
```


## ******************************************
## * Modul - Notification
## ******************************************

### * Benachrichtigungen auflisten:
```
    /index.php?module=Notification&cmd=listNotifications
```


## ******************************************
## * Modul - Device
## ******************************************

### * Anwesend einstellen:
```
    /index.php?module=Device&cmd=setHomeStatePresent
```

### * Abwesend einstellen:
```
    /index.php?module=Device&cmd=setHomeStateAway
```

### * Dimmer einstellen (0-100):
```
    /index.php?module=Device&cmd=setDimmerCommand&param_uids={uid}&param_level={0-100}
```

### * setHueCommand
```
    /index.php?module=Device&cmd=setHueCommand&param_uid={uid}&param_isCombinedBulb={true|false}&param_hue={0-360}&param_saturation={0-100}&param_brightness={0-100}
```

### * setJunkersHotWaterState
```
    /index.php?module=Device&cmd=setJunkersHotWaterState&param_uid={uid}&param_state={0-1}
```

### * setMieleState
```
    /index.php?module=Device&cmd=setMieleState&param_uid={uid}&param_active={true|false}
```

### * setPlugState
```
    /index.php?module=Device&cmd=setPlugState&param_uid={uid}&param_state={0-1}
```

### * setShutterCommand
```
    /index.php?module=Device&cmd=setShutterCommand&param_uid={uid}&param_level={0-100}
```

### * setSonosControlPlayer
```
    /index.php?module=Device&cmd=setSonosControlPlayer&param_uid={uid}&param_control={PLAY,PAUSE,PREVIOUS,NEXT}
```

### * setSonosVolume
```
    /index.php?module=Device&cmd=setSonosVolume&param_uid={uid}&param_volume={0-100}
```

### * setTunableWhiteValuesCommand
```
    /index.php?module=Device&cmd=setTunableWhiteValuesCommand&param_uid={uid}&param_brightness={0-100}&param_colorTemperature={0-100}
```





### * Sitzung beenden (logout):
```
    /index.php?logout
```

