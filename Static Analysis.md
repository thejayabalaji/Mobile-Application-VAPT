# Static Analysis

## 1. Objective

static analysis was to examine the AndroGoat APK without executing the application.The assessment focused on identifying insecure configurations, permissions, hard-coded strings.

## 2. Tool used
- Jadx

## 3. Execution
### AndroidManifest.xml Review

![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Static%20analysis%20Screenshots/STAndroid%20manifest.png?raw=true)

The application supports outdated Android versions that contain known security vulnerabilities on Android OS.

### Owasp Top 10 : M2: Inadequate Supply Chain Security


### Finding Hardcoded Strings






## 3. MobSF Analysis

MobSF was used to perform automated static analysis of the APK.

![MobSF Dashboard](../screenshots/mobsf-dashboard.png)

### Observations

- ...
- ...
- ...

## 4. AndroidManifest.xml Analysis

The application manifest was reviewed for exported components,
permissions, debuggable configuration, and other security-relevant settings.

![Manifest Analysis](../screenshots/manifest.png)

### Finding

**Exported Activity**

Description: ...

Impact: ...

## 5. Source/Code Analysis

...

## 6. Static Analysis Findings

| ID | Finding | Severity | Status |
|---|---|---|---|
| STA-01 | ... | High | Confirmed |
| STA-02 | ... | Medium | Confirmed |

## 7. Conclusion
