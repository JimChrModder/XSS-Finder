# F.A.Q

# ScreamingCobra
- Swiss knife for XSS on any URI
- XSS Fuzzer & Finder
- Any logic is valid logic in this software

# License
- EULA

# Running
- chmod u+x *
- ./interface.sh

# Screenshot
<div align="center">
    <img src="https://i.ibb.co/xgSzyKq/screamingcobra.png" width="600px"</img> 
</div>

# Screenshot
<div align="center">
    <img src="https://i.ibb.co/HFCnszs/Screenshot-from-2019-08-21-23-05-41.png" width="600px"</img> 
</div>

# DOM Based
<div align="center">
    <img src="https://i.ibb.co/SvSgHPQ/dombased.png" width="600px"</img> 
</div>

# Server Side URL hash (#) feature:
The hash (#) character in a URI denotes the beginning of a URI fragment. According to the RFC 3986, clients are not supposed to send URI fragments to the server, as the client should recognize that they reference a resource secondary to the current, or primary, resource. What does this mean for DOM based XSS! First, the fragment is stored in the DOM as a part of the document.location object, as well as in the document.location.href and document.URL attributes. If a developer parses either of these elements, the fragment will be included. Depending on how the developer parses the URL to extract parameter values, the use of a hash may have no effect on the parser, allowing an attacker to use a hash to inject the payload into the URL, but prevent the payload from being sent to the server where it may be scrutinized. Below is the same example as before, but the exploit is changed by introducing the hash character.

- Example: <script> var x = document.URL.substring(document.URL.indexOf("name=")+5);document.write(name + "!"); </script>
- Exploit: http://example.com?name=Tim#<script>alert(42)</script>
- Result: Hello Tim#<script>alert(42)</script>!

# Appeared
- https://blog.kelvinsecurity.com/2019/09/23/ultimate-swiss-knife-for-finding-xss-in-parameters-uri-url-urn-and-post-based-fuzzing/
- https://twitter.com/defsecnsattack/status/1189936304374591488

# Official Video and Tutorial
- https://www.youtube.com/watch?v=7zHmizAjQ4o

# Kali Installation
- chmod u+x Kali_Installer.sh
- ./Kali_Installer.sh
- ScreamingCobra
- ScreamingCobra is now system command, call anywhere in system

# Parrot_OS Installation
- chmod u+x Parrot_Os_Installer.sh
- ./Parrot_Os_Installer.sh
- ScreamingCobra
- ScreamingCobra is now system command, call anywhere in system


# Termux Installation
- chmod u+x Termux_Installer.sh
- ./interface.sh

# Compatible
- Android Led TV, Termux, Linux, Windows using cygwin

# Versions
- Version 1 is a normal version
- Version 2 is a Dom Experimental version


# URI, URL, Parameters Payloads
- Parameter :
- https://example.com.pk/pages.php?id=

- Fuzzing :
- https://example.com.pk/pages.php?id=id=id=id=

- Exclusives :
- https://example.com.pk/pages.php#
- https://example.com.pk/pages/
- https://example.com.pk/pages.php?id#


# XSS Payload Files
- payload
- dompayload

# Increasing XSS Payload Files
- copy paste your payload direct into payload file
- copy pastge your dom payload direct into dompayload file
