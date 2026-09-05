# Dynamic Analysis

# Objective

The objective of dynamic analysis was to assess the AndroGoat APK while the application was running in a controlled Android environment.
The testing focused on application behavior, runtime interactions, network communication and authentication.
The identified issues were validated and documented based on the OWASP Mobile Top 10.

# Tool used
- Objection
- Frida
- Brup Suite

# Execution
## 1. SSL Pinning
- Installed Frida Server on the Android emulator and used Objection to bypass SSL pinning.
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/SSL%20pinning.png?raw=true)
- Type [android sslpinning disable] to disable the SSL Pinning.
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/final%20andro.png?raw=true)
- The requested protocol is appear in Burp suite  

### Owasp Top 10 : M5: Insecure Communication

## 2. Unprotected android components
