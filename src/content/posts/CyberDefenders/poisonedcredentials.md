---
title: PoisonedCredentials - CyberDefenders
published: 2025-02-17
description: 'En este laboratorio, se simuló un incidente de seguridad de red relacionado con credenciales envenenadas, donde los atacantes explotaron vulnerabilidades en los protocolos Link-Local Multicast Name Resolution (LLMNR) y NetBIOS Name Service (NBT-NS). El escenario comenzó con una actividad sospechosa detectada por el equipo de seguridad, lo que llevó a un análisis con Wireshark para identificar el ataque. A lo largo del laboratorio, se investigaron aspectos clave del ataque, como la identificación de consultas envenenadas, el seguimiento de la IP del atacante y el análisis de intentos de autenticación SMB.'
image: '../../../assets/CyberDefenders/PoisonedCredentials/poisonedcredentials-banner.webp'
tags: [CyberDefenders, BlueTeam, SOC]
category: 'WriteUp'
draft: false 
---

En este laboratorio de **[CyberDefenders](https://cyberdefenders.org/blueteam-ctf-challenges/poisonedcredentials/)**, se simuló un incidente de seguridad de red relacionado con credenciales envenenadas, donde los atacantes explotaron vulnerabilidades en los protocolos Link-Local Multicast Name Resolution (LLMNR) y NetBIOS Name Service (NBT-NS). Estos protocolos, diseñados para la resolución de nombres en redes locales, son vulnerables por su dependencia de consultas de difusión y la falta de autenticación robusta, lo que permite a los ciberdelincuentes realizar ataques man-in-the-middle, redirigir el tráfico y robar credenciales.

El escenario comenzó con una actividad sospechosa detectada por el equipo de seguridad, lo que llevó a un análisis con Wireshark para identificar el ataque. A lo largo del laboratorio, se investigaron aspectos clave del ataque, como la identificación de consultas envenenadas, el seguimiento de la IP del atacante y el análisis de intentos de autenticación SMB.

~~~
Platform: CyberDefenders
Level: Easy
Type: SOC, Network Forensics
~~~

### Lab Scenario

> El equipo de seguridad de su organización ha detectado un aumento en la actividad sospechosa de la red. Existen preocupaciones de que puedan estar ocurriendo ataques de envenenamiento LLMNR (Link-Local Multicast Name Resolution) y NBT-NS (NetBIOS Name Service) dentro de su red. Se sabe que estos ataques explotan dichos protocolos para interceptar el tráfico de la red y potencialmente comprometer las credenciales de usuario. Su tarea es investigar los registros de la red y examinar el tráfico capturado.

### Key Information

**`LLMNR (Link-Local Multicast Name Resolution)`** es un protocolo de resolución de nombres en redes locales que permite la resolución de nombres sin depender de un servidor DNS centralizado. Sin embargo, debido a su falta de mecanismos de autenticación robustos, **LLMNR** es susceptible a ataques de **envenenamiento de LLMNR**, donde un atacante puede interceptar las solicitudes de resolución de nombres y responder con información falsa. Este tipo de ataque suele realizarse utilizando herramientas como **Responder**, que engañan a los dispositivos de la red para que envíen credenciales (como hashes NTLMv2 o NTLMv1) al atacante en lugar de al servidor legítimo. Al robar estas credenciales, el atacante puede obtener acceso no autorizado a la red.

De manera similar, **`NBNS (NetBIOS Name Service)`** es un protocolo utilizado en redes locales para la resolución de nombres NetBIOS, permitiendo que los dispositivos se identifiquen y se comuniquen utilizando nombres legibles en lugar de direcciones IP. Al igual que **LLMNR**, **NBNS** carece de autenticación adecuada, lo que lo convierte en un objetivo fácil para ataques de **envenenamiento de NBNS**. En este tipo de ataque, el atacante responde a las solicitudes de resolución de nombres con información falsa, suplantando al servidor legítimo y redirigiendo el tráfico hacia su propio dispositivo. Esto permite que el atacante capture credenciales de usuario o realice ataques de **man-in-the-middle** para interceptar comunicaciones y robar datos sensibles.

Ambos protocolos, al no contar con mecanismos de autenticación robustos, son vulnerables a estos ataques de envenenamiento, en los que los atacantes pueden capturar o manipular credenciales y obtener acceso a recursos sensibles dentro de la red local.

![Yw4rf PoisonedCredentials](../../../assets/CyberDefenders/PoisonedCredentials/poisonedcredentials-cyberdefenders.png)

