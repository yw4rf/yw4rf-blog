---
title: What is OWASP? Owasp Top 10?
published: 2024-11-18
description: 'OWASP (Open Web Application Security Project) es una organización sin fines de lucro dedicada a mejorar la seguridad del software. Su misión es proporcionar recursos gratuitos y accesibles que ayuden a las organizaciones a desarrollar y mantener aplicaciones web seguras. OWASP se enfoca en la educación, investigación y colaboración en torno a las mejores prácticas de seguridad en el desarrollo de aplicaciones.'
image: '../../../assets/Ethical-Hacking/OWASPtop10/tryhackme-owasptop10.png'
tags: [Pentesting, EthicalHacking]
category: 'Cybersecurity'
draft: false 
---

## What is OWASP? 

**[OWASP (Open Web Application Security Project)](https://owasp.org/)** es una organización sin fines de lucro dedicada a mejorar la seguridad del software. Su misión es proporcionar recursos gratuitos y accesibles que ayuden a las organizaciones a desarrollar y mantener aplicaciones web seguras. OWASP se enfoca en la educación, investigación y colaboración en torno a las mejores prácticas de seguridad en el desarrollo de aplicaciones.

### OWASP Objectives:

- **Educación y concienciación sobre seguridad**: OWASP promueve el entendimiento de los riesgos de seguridad a lo largo del ciclo de vida del desarrollo de software.

- **Mejores prácticas de seguridad**: Proporciona directrices, herramientas y proyectos que ayudan a los desarrolladores a seguir prácticas de seguridad durante el proceso de desarrollo.

- **Comunidad abierta**: OWASP fomenta la colaboración entre expertos de seguridad, desarrolladores y organizaciones para mejorar las prácticas de seguridad en el software.

## What is OWASP Top 10?

Una de las publicaciones más conocidas de OWASP es su lista de las **Top 10** vulnerabilidades de seguridad en aplicaciones web. Cada cierto tiempo, OWASP revisa y actualiza esta lista con las amenazas más críticas, con el objetivo de concienciar sobre los riesgos comunes y ayudar a las organizaciones a proteger sus sistemas.

## OWASP Top 10 (2021):

1. **[A01:2021 - Broken Access Control](https://yw4rf.vercel.app/posts/ethical-hacking/bac/)**  
    Errores en el control de acceso pueden permitir a los usuarios no autorizados acceder a funciones o datos sensibles. Esto incluye la evasión de permisos, eludir controles de acceso y modificar la información de otros usuarios.
    
2. **A02:2021 - Cryptographic Failures**  
    Falta de encriptación o el uso de algoritmos débiles o mal implementados puede comprometer la confidencialidad y la integridad de los datos.
    
3. **A03:2021 - Injection**  
    Ataques como SQL injection, NoSQL injection, y LDAP injection ocurren cuando los datos proporcionados por un usuario son insertados en una consulta sin validación adecuada, lo que puede permitir a los atacantes ejecutar comandos maliciosos.
    
4. **A04:2021 - Insecure Design**  
    La falta de una arquitectura y diseño seguros desde el inicio puede llevar a vulnerabilidades. Esto incluye la falta de protección ante amenazas conocidas o malas prácticas en la construcción de la aplicación.
    
5. **A05:2021 - Security Misconfiguration**  
    Configuraciones inseguras en el servidor, la base de datos, o el software pueden permitir a los atacantes acceder a datos o recursos sensibles.
    
6. **A06:2021 - Vulnerable and Outdated Components**  
    El uso de componentes de software desactualizados o con vulnerabilidades conocidas puede ser explotado por atacantes para comprometer la seguridad de la aplicación.
    
7. **A07:2021 - Identification and Authentication Failures**  
    Problemas con la autenticación y gestión de sesiones, como el uso de contraseñas débiles, la falta de autenticación multifactor, o la gestión incorrecta de sesiones.
    
8. **A08:2021 - Software and Data Integrity Failures**  
    Las fallas de integridad en el software o los datos pueden permitir a los atacantes modificar el comportamiento de la aplicación o introducir datos maliciosos.
    
9. **A09:2021 - Security Logging and Monitoring Failures**  
    La falta de registros adecuados y monitoreo de seguridad puede dificultar la detección de incidentes de seguridad y la respuesta ante ataques.
    
10. **A10:2021 - Server-Side Request Forgery (SSRF)**  
    Un ataque SSRF ocurre cuando un atacante puede hacer que el servidor de la aplicación realice solicitudes a otros recursos internos o externos, lo que puede llevar a la filtración de información o comprometer otros sistemas.


> **References:**
> - [Owasp site](https://owasp.org/)
> - [Owasp Top 10](https://owasp.org/www-project-top-ten/)