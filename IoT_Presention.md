---
marp: true
backgroundColor: #1e1e2e
color: #cdd6f4

style: |
  
  @import url('https://cdn.jsdelivr.net/npm/@fontsource/iosevka/index.css');

  section 
  {
    font-family: 'Iosevka', monospace;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    padding: 60px 70px 50px;
  }

  section h1 
  {
    font-size: 48px;
    color: #cdd6f4;
    border: none;
    margin: 0 0 32px;
  }

  section h1::before 
  {
    content: "$ ";
    color: #ff0000;
  }

  section ul 
  {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
    gap: 18px;
    counter-reset: line;
  }

  section li 
  {
    font-size: 28px;
    margin: 0;
    counter-increment: line;
  }

  section li::before 
  {
    content: counter(line, decimal-leading-zero) "  ";
    color: #6c7086;
  }

  section li strong 
  {
    color: #cdd6f4;
  }

  section li em 
  {
    font-style: normal;
    color: #6c7086;
    margin-left: 12px;
  }

  section.one 
  {
    justify-content: center;
    text-align: center;
  }

  section.one h1 
  {
    font-size: 64px;
  }

  section.one p 
  {
    color: #6c7086;
    font-size: 28px;
  }

  section.sources ul 
  {
    gap: 6px;
  }

  section.sources li 
  {
    font-size: 25px;
  }

  section.sources a 
  {
    color: #89b4fa;
    text-decoration: none;
  }
  
  
---

<!-- _class: one -->

# IoT Security

 Jacob Zepeda
 
---

# What is IoT?

- **Small devices** *(microcontroller, firmware, internet)*
- **Commonly found** *(sensors, fridges, lightbulbs, cars, cameras)*

![w:](IoT.svg)

---

# Breaking News
![bg right:40% width:800 ](fridge.svg)

### French Refrigerator Hack
- **Open to the internet** 
  &nbsp; *(using default admin credentials)*
- **Temperatures overridden** 
  &nbsp; *(up to 176F, causing fires)*
- **700 supermarkets affected** 
  &nbsp; *($10m in lost goods)*
---

# Risks
- **Weak/Default Credentials** *(root:root, hardcoded in firmware)*
- **Misconfigurations** *(exposed endpoints)*
- **Unpatched Software** *(known CVEs and flaws)*
- **Legacy Encryption** *(RC4, DES)*
- **Firmware Vulnerabilities** *(buffer overflows, RCEs)*
- **Lack of Isolation** *lateral movement, pivoting*
- **Side Channels, Malware, Botnets, Financial loss** 


---

# Prevention

- **Change default passwords**
- **Update or remove old software**
- **Isolate devices from your network**
- **Buy from trusted vendors**
- **Analyze devices and network traffic**

---

<!-- _class: sources -->

- [cybersecuritynews.com](https://cybersecuritynews.com/)
- [spamhaus.com/threat-map](https://www.spamhaus.com/threat-map/)
- [ibm.com/think/topics/internet-of-things](https://www.ibm.com/think/topics/internet-of-things)
- [ibm.com/think/topics/encryption](https://www.ibm.com/think/topics/encryption)
- [shodan.io](https://www.shodan.io/)
- [safeguard.sh](https://safeguard.sh/resources/blog/hardcoded-credentials-in-firmware-cwe-798)
- [paulkocher.com: DPA ](https://www.paulkocher.com/doc/DifferentialPowerAnalysis.pdf)
- [chs.us](https://chs.us/2026/06/owasp-a04-cryptographic-failures-prevention/)
- [pentestpartners.com](https://www.pentestpartners.com/security-blog/how-to-do-firmware-analysis-tools-tips-and-tricks/)
- [book.rada.re](https://book.rada.re/analysis/code_analysis.html)
- [nvd.nist.gov](https://nvd.nist.gov/)
- [ipinfo.io](https://ipinfo.io/blog/france-fridges-hack)
- [code.nsa.gov](https://code.nsa.gov/)
