# Dynamic Analysis

## 1. Objective

The objective of dynamic analysis was to assess the AndroGoat APK while the application was running in a controlled Android environment.
The testing focused on application behavior, runtime interactions, network communication and authentication.
The identified issues were validated and documented based on the OWASP Mobile Top 10.

## 2. Tool used
- Objection
- Frida
- Brup Suite

## 3. Execution
### SSL Pinning
- Installed Frida Server on the Android emulator and used Objection to bypass SSL pinning.
