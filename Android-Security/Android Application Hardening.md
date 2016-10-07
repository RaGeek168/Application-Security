# Android Application Hardening Controls
Description: This checklist will help android developers to harden their application during the development phase.

##### Encrypt shared preferences
  - Reference: https://github.com/scottyab/secure-preferences
##### Avoid storing sensitive information withing shared preferences even if you are using encrypted shared preferences
##### Encrpyt SQLite database.
  - Reference: https://github.com/sqlcipher/sqlcipher
##### Application must not store any sensitive information in system logs.
##### Application must not store any sensitive information in SQLitedb for any kind of analystic purpose.
##### No extra permission should be taken from user than the intended one.
##### Implement hmacSHA256 encryption within request and response in order to avoid tampering.
  - http://infosecninja.blogspot.in/2016/09/android-application-security-tamper.html
##### Use proguard/dexguard for source code ofuscation.
  - https://www.guardsquare.com
  - http://proguard.sourceforge.net/
##### Disallow user to run application on rooted devices and old Android versions 4.1 >=
##### Implement best available solution for SSL pinning
  - 1. Using a simple HttpsURLConnection with a PinningTrustManager
  - 2. Using a simple HttpClient with a PinningTrustManager
  - 3. Work with PinningTrustManager and PinningSSLSocketFactory more directly
  - https://github.com/moxie0/AndroidPinning
#### Do not export more than required activities of post login which can be directly triggered via adb by attackers.
  - If require, there must be a valid intent filter
#### Do not share sensitive information on SD card which is publicly available even non-rooted devices.
#### If there is file upload mechanism then follow best practices for file upload on server side.
  - Upload feature testcases - http://apps.testinsane.com/mindmaps/Uploads/Upload.png
#### Implement 2/3 minutes of throttling between two consecutive requests made to the server. It helps to avoid all security scanners that can be executed on your api server, backend web application.
