# Samsung FRP Bypass

- grab python from <a href="https://www.python.org/downloads/">here</a><br>
- Make sure you have all the dependencies listed in `requirements.txt` installed
- Install them using `pip install -r requirements.txt`
- You can simply plug the samsung over USB and run `python main.py`

## frp.bin
### runs the following commands in adb

settings put global setup_wizard_has_run 1<br>
settings put secure user_setup_complete 1<br>
content insert --uri content://settings/secure --bind name:s:DEVICE_PROVISIONED --bind value:i:1<br>
content insert --uri content://settings/secure --bind name:s:user_setup_complete --bind value:i:1<br>
content insert --uri content://settings/secure --bind name:s:INSTALL_NON_MARKET_APPS --bind value:i:1<br>
am start -c android.intent.category.HOME -a android.intent.action.MAIN<br>
Wait 5 sec<br>
am start -n com.android.settings/com.android.settings.Settings<br>
Wait 5 sec<br>
reboot

## main.py
<img width="511" alt="Screenshot 2023-11-26 at 1 46 06 AM" src="https://github.com/sudo-self/samsung-frp/assets/119916323/001dfba7-4941-4d61-828c-da7c0d010f08">
<img width="680" alt="Screenshot 2023-11-26 at 4 20 27 AM" src="https://github.com/sudo-self/samsung-frp/assets/119916323/bd0c81ea-1416-4c21-bbea-c8c382589115">
<table style="height: 336px; width: 100%; border-collapse: collapse; background-color: #fcfcfc;"><tbody><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">Access Device Settings</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="intent://com.android.settings/#Intent;scheme=android-app;end">OPEN</a></span></span></td></tr><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">Access SAMSUNG Galaxy Apps</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="intent://com.sec.android.app.samsungapps/#Intent;scheme=android-app;end">OPEN</a></span></span></td></tr><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">Access SAMSUNG Galaxy Store</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="https://www.samsung.com/uk/apps/galaxy-store/" target="_blank" rel="noreferrer noopener">OPEN</a></span></span></td></tr><tr style="height: 24px;"><td style="width: 76.5326%; height: 24px;"><span style="font-family: arial, helvetica, sans-serif;">Set Pattern Lock</span></td><td style="width: 23.4674%; height: 24px;"><span style="color: #ff0000;"><a style="color: #ff0000;" href="intent://com.google.android.gms/#Intent;scheme=promote_smartlock_scheme;end"><span style="font-family: arial, helvetica, sans-serif;">OPEN</span></a></span></td></tr><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">Access Google Search BOX</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="intent://com.google.android.googlequicksearchbox/#Intent;scheme=android-app;end">OPEN</a></span></span></td></tr><tr style="height: 24px;"><td style="width: 76.5326%; height: 24px;"><span style="font-family: arial, helvetica, sans-serif;">Alliance Shield X</span></td><td style="width: 23.4674%; height: 24px;"><span style="color: #ff0000;"><a style="color: #ff0000;" href="intent://com.rrivenllc.shieldx/#Intent;scheme=android-app;end"><span style="font-family: arial, helvetica, sans-serif;">OPEN</span></a></span></td></tr><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">GMAIL APP</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="intent://com.google.android.gm/#Intent;scheme=android-app;end">OPEN</a></span></span></td></tr><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">Chrome APP</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="intent://com.android.chrome/#Intent;scheme=android-app;end">OPEN</a></span></span></td></tr><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">Youtube APP</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="intent://com.google.android.youtube/#Intent;scheme=android-app;end">OPEN</a></span></span></td></tr><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">Samsung My Files</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="intent://com.sec.android.app.myfiles/#Intent;scheme=android-app;end">OPEN</a></span></span></td></tr><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">Android Google Maps</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="intent://com.google.android.apps.maps/#Intent;scheme=android-app;end">OPEN</a></span></span></td></tr><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">Touch ID</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="intent://com.android.settings/com.samsung.android.settings.biometrics.fingerprint.FingerprintEntry/#Intent;scheme=android-app;end">OPEN</a></span></span></td></tr><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">Remote Call Dialer</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="tel:112" target="_blank" rel="noreferrer noopener">OPEN</a></span></span></td></tr><tr style="height: 22px;"><td style="width: 76.5326%; height: 22px;"><span style="font-family: arial, helvetica, sans-serif;">GS Hidden Settings</span></td><td style="width: 23.4674%; height: 22px;"><span style="color: #ff0000;"><span style="font-family: arial, helvetica, sans-serif;"><a style="color: #ff0000;" href="https://apps.samsung.com/appquery/appDetail.as?appld=com.jami.tool.play.services.hidden.settings">OPEN</a></span></span></td></tr></tbody></table><p>&nbsp;</p><h2><span style="color: #000000;"><strong><span style="font-size: 18pt;"><a id="PCAPP"></a>
