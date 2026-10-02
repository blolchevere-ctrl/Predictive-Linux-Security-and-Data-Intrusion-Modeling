<!-- HEADER BANNER -->
<div align="center">
  <img src="./assets/banner-binario.jpg" width="100%" alt="Cybersecurity & Binary Code Banner" />
</div>

<br />

<!-- HEADER WITH UNALM SHIELD -->
<table border="0" width="100%">
  <tr>
    <td width="78%" valign="top">
      <h1>🐧 Predictive Linux Security & Automated Threat Mitigation System</h1>
      <h3>Statistical Analytics Pipeline & Active Firewall Defense Engine for Linux Infrastructure</h3>
      <p>
        👤 <b>Autor:</b> Brian Alva Aquino (<a href="https://github.com/blolchevere-ctrl">@blolchevere-ctrl</a>)<br />
        🎓 <b>Institución:</b> Universidad Nacional Agraria La Molina (UNALM)<br />
        📚 <b>Área:</b> Linux Systems, Predictive Analytics & Defensive Cyber-Engineering
      </p>
      <p>
        <img src="https://img.shields.io/badge/OS-Linux_Ubuntu-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" />
        <img src="https://img.shields.io/badge/Scripting-Bash_%7C_Python-4EAA25?style=flat-square&logo=gnubash" alt="Bash" />
        <img src="https://img.shields.io/badge/Analytics-Statistical_Modeling-blueviolet?style=flat-square" alt="Analytics" />
        <img src="https://img.shields.io/badge/Status-Production_Ready-brightgreen?style=flat-square" alt="Status" />
      </p>
    </td>
    <td width="22%" align="center" valign="middle">
      <img src="./assets/escudo-unalm.png" width="120" alt="Escudo UNALM" />
    </td>
  </tr>
</table>

---

## 📌 Arquitectura General del Sistema

Este repositorio contiene una **plataforma defensiva integral para servidores Linux** que combina telemetría a nivel de Kernel, modelado estadístico multivariado y mitigación automatizada en el cortafuegos.

A diferencia de las soluciones tradicionales basadas únicamente en reglas estáticas, este sistema evalúa estocásticamente la densidad de tráfico y los patrones de acceso no autorizados, prediciendo la probabilidad de compromiso antes de que ocurra una violación de datos.

---

## ⚙️ Componentes de la Solución

```text
  [ /var/log/auth.log & auditd ]
                │
                ▼
  ┌───────────────────────────┐
  │ 1. Telemetría y Parsing   │ ── (Estructuración Regex de eventos Syslog)
  └───────────────────────────┘
                │
                ▼
  ┌───────────────────────────┐
  │ 2. Modelado Estadístico   │ ── (Regresión Logística / Poisson / Binomial Negativa)
  └───────────────────────────┘
                │
                ▼
  ┌───────────────────────────┐
  │ 3. Agente de Mitigación   │ ── (Bloqueo dinámico mediante iptables / ufw)
  └───────────────────────────┘
```

### 1. Ingesta Estructurada de Telemetría Linux
* **Parsing en Tiempo Real:** Filtro optimizado sobre `/var/log/auth.log`, `syslog` y auditorías `auditd`.
* **Identificación de Eventos:** Detección de fallos de autenticación SSH, escalamiento indebido de privilegios (`sudo`), escaneo de puertos y mutaciones anómalas en el sistema de archivos.

### 2. Motor de Inferencia Estadística Predictiva
* **Modelado de Probabilidad de Compromiso:** Implementación de **Regresión Logística** para estimar la probabilidad condicional de intrusión dado un conjunto de métricas temporales.
* **Modelos de Frecuencia y Conteo:** Uso de **Regresión de Poisson** y **Binomial Negativa** para predecir ráfagas (*bursts*) de ataques de fuerza bruta por ventana temporal.

### 3. Agente de Respuesta Defensiva y Control de Cortafuegos
* **Respuesta Automatizada:** Scripting avanzado en Bash integrado con el motor de inferencia Python.
* **Hardening Dinámico:** Aplicación automática de reglas de bloqueo de direcciones IP en `iptables` y `ufw` al superar umbrales de probabilidad crítica.
* **Auditoría de Acciones Defensivas:** Generación de reportes de atenuación y rotación de logs de bloqueo.

---

## 📂 Estructura del Repositorio

```text
Predictive-Linux-Security-and-Data-Intrusion-Modeling/
├── assets/
│   ├── banner-binario.jpg
│   └── escudo-unalm.png
├── config/
│   ├── firewall_rules.conf
│   └── threshold_settings.json
├── src/
│   ├── __init__.py
│   ├── log_parser.py          # Extracción y parsing de eventos Syslog/auditd
│   ├── predictive_model.py    # Regresión Logística y Poisson
│   └── mitigation_agent.py    # Integración con el sistema operativo
├── scripts/
│   ├── deploy_agent.sh        # Script de despliegue en servidor Linux
│   └── apply_iptables.sh      # Ejecutor de reglas de firewall
├── notebooks/
│   └── intrusion_analysis.ipynb
├── tests/
│   └── test_parser.py
├── requirements.txt
└── README.md
```
