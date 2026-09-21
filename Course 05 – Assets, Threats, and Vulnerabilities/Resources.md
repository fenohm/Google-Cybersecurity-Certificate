# Resources – Course 05

Recursos externos utilizados o relacionados con los principales conceptos estudiados en **Course 05 – Assets, Threats, and Vulnerabilities**.

---

## OWASP

### OWASP Top 10

El **OWASP Top 10** es un documento de referencia sobre los principales riesgos de seguridad en aplicaciones web.

**Utilidad:** Ayuda a comprender vulnerabilidades como Broken Access Control, Injection, Cryptographic Failures y Security Misconfiguration.

* [OWASP Top 10](https://owasp.org/www-project-top-ten/)

### OWASP Web Security Testing Guide

La **OWASP Web Security Testing Guide (WSTG)** contiene metodologías y técnicas para evaluar la seguridad de aplicaciones web.

**Utilidad:** Recurso útil para estudiar pruebas de seguridad y vulnerabilidades como **SQL Injection**.

* [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)

---

## NIST

### National Vulnerability Database (NVD)

La **National Vulnerability Database (NVD)** es una base de datos mantenida por NIST que contiene información sobre vulnerabilidades de seguridad identificadas mediante **CVE**.

**Utilidad:** Permite investigar vulnerabilidades específicas, su severidad y productos afectados.

* [NIST National Vulnerability Database](https://nvd.nist.gov/)

### NIST Cybersecurity Framework

El **NIST Cybersecurity Framework (CSF)** proporciona un marco para gestionar y reducir riesgos de ciberseguridad.

**Utilidad:** Ayuda a relacionar conceptos como Identify, Protect, Detect, Respond y Recover con la gestión de riesgos.

* [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)

---

## MITRE

### MITRE ATT&CK

**MITRE ATT&CK** es una base de conocimiento que documenta tácticas, técnicas y procedimientos utilizados por atacantes.

**Utilidad:** Permite estudiar el comportamiento de los **Threat Actors** y relacionarlo con diferentes técnicas de ataque.

* [MITRE ATT&CK](https://attack.mitre.org/)

---

## OSINT

### OSINT Framework

**OSINT Framework** reúne diferentes herramientas y fuentes utilizadas para realizar investigaciones mediante **Open Source Intelligence (OSINT)**.

**Utilidad:** Puede utilizarse para investigar información pública relacionada con dominios, personas, organizaciones, IPs y otros indicadores.

* [OSINT Framework](https://osintframework.com/)

### VirusTotal

**VirusTotal** permite analizar archivos, URLs, dominios e indicadores utilizando información proveniente de múltiples motores de seguridad.

**Utilidad:** Es útil para realizar análisis iniciales de posibles archivos o indicadores maliciosos.

* [VirusTotal](https://www.virustotal.com/)

### Have I Been Pwned

**Have I Been Pwned** permite comprobar si una dirección de correo electrónico aparece en filtraciones de datos conocidas.

**Utilidad:** Ayuda a comprender los riesgos asociados con credenciales expuestas y ataques como **Credential Stuffing**.

* [Have I Been Pwned](https://haveibeenpwned.com/)

---

## Threat Modeling

### STRIDE

**STRIDE** es un framework de Microsoft para identificar diferentes categorías de amenazas durante el desarrollo de aplicaciones.

Las categorías son:

* **Spoofing**
* **Tampering**
* **Repudiation**
* **Information Disclosure**
* **Denial of Service**
* **Elevation of Privilege**

**Utilidad:** Permite analizar amenazas de manera estructurada durante el desarrollo de aplicaciones.

* [Microsoft Threat Modeling Tool](https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool)

---

## Vulnerability Management

### CVE

**Common Vulnerabilities and Exposures (CVE)** es un sistema utilizado para identificar públicamente vulnerabilidades conocidas.

**Utilidad:** Permite referenciar vulnerabilidades específicas mediante identificadores como `CVE-2021-44228`.

* [CVE Program](https://www.cve.org/)

### Log4Shell

**Log4Shell (CVE-2021-44228)** fue una vulnerabilidad crítica en la biblioteca Apache Log4j que permitió ataques de **Remote Code Execution (RCE)** en sistemas afectados.

**Utilidad:** Es un ejemplo importante para comprender el impacto que puede tener una vulnerabilidad crítica ampliamente utilizada.

* [NVD – CVE-2021-44228](https://nvd.nist.gov/vuln/detail/CVE-2021-44228)

---

## Security Tools

### Hashcat

**Hashcat** es una herramienta utilizada para evaluar la seguridad de contraseñas mediante el análisis de hashes.

**Utilidad:** Permite estudiar conceptos como password security, hashing y ataques de fuerza bruta en entornos autorizados.

* [Hashcat](https://hashcat.net/hashcat/)

### John the Ripper

**John the Ripper** es una herramienta utilizada para evaluar la seguridad de contraseñas.

**Utilidad:** Puede utilizarse en laboratorios y sistemas autorizados para estudiar ataques contra hashes de contraseñas.

* [John the Ripper](https://www.openwall.com/john/)

### Aircrack-ng

**Aircrack-ng** es un conjunto de herramientas orientadas al análisis y evaluación de la seguridad de redes Wi-Fi.

**Utilidad:** Permite estudiar conceptos relacionados con seguridad inalámbrica y autenticación.

* [Aircrack-ng](https://www.aircrack-ng.org/)

### THC Hydra

**THC Hydra** es una herramienta utilizada para realizar pruebas automatizadas de autenticación contra diferentes servicios.

**Utilidad:** Puede utilizarse en laboratorios autorizados para comprender ataques de fuerza bruta y evaluar controles de autenticación.

* [THC Hydra](https://github.com/vanhauser-thc/thc-hydra)

---

## Security Standards and Documentation

### CWE

**Common Weakness Enumeration (CWE)** es una clasificación de debilidades comunes de software y hardware.

**Utilidad:** Ayuda a comprender las causas y categorías de diferentes vulnerabilidades.

* [CWE – MITRE](https://cwe.mitre.org/)

### CVSS

**Common Vulnerability Scoring System (CVSS)** proporciona una metodología para expresar la severidad de una vulnerabilidad.

**Utilidad:** Permite comprender cómo se evalúa el impacto y la gravedad de diferentes vulnerabilidades.

* [FIRST CVSS](https://www.first.org/cvss/)

---

## Conceptos para seguir estudiando

Los siguientes temas fueron especialmente relevantes durante el curso y pueden servir como base para continuar estudiando:

* **Risk Management**
* **Threat Modeling**
* **Threat Actors**
* **Attack Vectors**
* **Vulnerability Management**
* **SQL Injection**
* **OWASP Top 10**
* **Penetration Testing**
* **Social Engineering**
* **Phishing**
* **Malware**
* **Brute Force Attacks**
* **Identity and Access Management (IAM)**
* **Principle of Least Privilege**
* **Encryption**
* **Hashing**
* **Security Awareness**
* **DevSecOps**
* **OSINT**

---

## Nota

Los recursos y herramientas mencionados deben utilizarse de manera responsable y únicamente sobre sistemas propios, laboratorios o entornos donde exista autorización para realizar pruebas de seguridad.

