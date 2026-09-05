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

#### AndroGOAT presents a PIN entry screen. Normally, a user would have to enter the correct PIN to proceed to the protected content.
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/2nd%20point.png?raw=true)
#### Check the log. Get the activity
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/2nd%20point%201.png?raw=true)
#### Instead of entering a PIN, use ADB to invoke the protected activity directly from the host machine’s terminal:
#### -- adb shell
#### -- am start -n owasp.sat.agoat/.AccessControl1ViewActivity
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/2nd%20point%202.png?raw=true)
#### The protected activity launches directly on the emulator without requiring the PIN.
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/2nd%20point%203.png?raw=true)

### OWASP Top 10 : M1: Improper Platform Usage

## 3. Insecure Data Storage
#### - Part 1
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/3rd%20p1.png?raw=true)
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/3rd%20p2.png?raw=true)
#### - Part 2 (SQL Data storage)
#### Check source code to identify which type of DB is being used here.
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/3rd%20sql%20p1.png?raw=true)
#### It’s SQL DB. Navigate to the app’s database directory and open the SQLite database
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/3rd%20sql%20p2.png?raw=true)
#### - Part 3 (Temporary Data Storage)
#### Check the type of DB and some path information from source code Then Navigate to the application’s root data directory and list its contents
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/3rd%20temp.png?raw=true)

### OWASP Top 10 : M9: Insecure Data Storage

## 4. SQL Injection
#### Applying SQL payloads in search bar
#### ‘ or 1=1 --
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/4SQL%20Injection.png?raw=true)

### OWASP Top 10 : M4: Insufficient Input/Output Validation

## 5. XSS (Cross Site Scripting)
#### Applying XSS payloads in search bar
#### <script>alert(‘XSS’)</script>
![image alt](https://github.com/thejayabalaji/Mobile-Application-VAPT/blob/main/Dynamic%20analysis/4XSS.png?raw=true)

### OWASP Top 10 : M4: Insufficient Input/Output Validation
