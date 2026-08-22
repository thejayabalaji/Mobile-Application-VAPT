# Static Analysis

## 1. Objective

static analysis was to examine the AndroGoat APK without executing the application.The assessment focused on identifying insecure configurations, permissions, hard-coded strings.

## 2. Tool used
- Jadx  (_To decompile the apk_)

## 3. Execution
### I. AndroidManifest.xml Review
The application supports outdated Android versions that contain known security vulnerabilities on Android OS.
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Static%20analysis%20Screenshots/STAndroid%20manifest.png?raw=true)

## Owasp Top 10 : M2: Inadequate Supply Chain Security


### II. Finding Hardcoded Strings
Locating embedded secrets, keys, and credentials in code.
- #### Promocode
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Static%20analysis%20Screenshots/STpromocode.png?raw=true)
- #### Open API Key
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Static%20analysis%20Screenshots/STopen%20api%20key.png?raw=true)
- #### AWS Credentials (ID & Password)
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Static%20analysis%20Screenshots/ST%20AWS%20ID.png?raw=true)

## Owasp Top 10 : M1: Improper Credential Usage
