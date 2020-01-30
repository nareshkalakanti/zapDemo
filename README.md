zap-webdriver
=============
Example security tests using JUnit, Selenium WebDriver and OWASP ZAP to test the Bodgeit store (https://code.google.com/p/bodgeit/)
The tests use selenium to navigate and login to the app, then spider the content with ZAP and perform a security scan using ZAP's scanner.  Tests pass or fail based on vulnerabilities found.

Getting started
===============
1. Download and start the [bodgeit store](https://code.google.com/p/bodgeit/) on port 8080
2. Download and start [OWASP ZAP](https://code.google.com/p/zaproxy/wiki/Downloads?tm=2) at least version 2.4 
3. In the ZAP Options change the local proxy port to 8888
4. Download this repository
5. Look through the src/test/java/net/continuumsecurity/ZapScanTest class and check that the static fields match your setup.  In particular, change the CHROME_DRIVER_PATH to point to the chrome driver instance appropriate for your platform, the driver/ directory contains versions for Linux, Mac and Windows.
5. Run: mvn test

Run it using docker
=======
docker run --rm -p 8081:8080 -i -t -d psiinon/bodgeit# zapDemo
