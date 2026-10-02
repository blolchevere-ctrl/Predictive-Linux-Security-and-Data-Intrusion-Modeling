<!-- HEADER BANNER -->
<div align="center">
  <img src="./assets/banner-binario.jpg" width="100%" alt="Cybersecurity & Binary Code Banner" />
</div>

<br />

<!-- HEADER WITH UNALM SHIELD -->
<table border="0" width="100%">
  <tr>
    <td width="78%" valign="top">
      <h1>🐧 Predictive Linux Security & Data Intrusion Modeling</h1>
      <h3>Statistical Regression & Automated Anomaly Prevention for Linux Systems</h3>
      <p>
        👤 <b>Autor:</b> Brian Alva Aquino (<a href="[https://github.com/blolchevere-ctrl](https://github.com/blolchevere-ctrl)">@blolchevere-ctrl</a>)<br />
        🎓 <b>Institución:</b> Universidad Nacional Agraria La Molina (UNALM)<br />
        📚 <b>Área:</b> Linux Hardening, Predictive Analytics & Systems Defense
      </p>
      <p>
        <img src="[https://img.shields.io/badge/OS-Linux_Ubuntu-FCC624?style=flat-square&logo=linux&logoColor=black](https://img.shields.io/badge/OS-Linux_Ubuntu-FCC624?style=flat-square&logo=linux&logoColor=black)" alt="Linux" />
        <img src="[https://img.shields.io/badge/Scripting-Bash_%7C_Python-4EAA25?style=flat-square&logo=gnubash](https://img.shields.io/badge/Scripting-Bash_%7C_Python-4EAA25?style=flat-square&logo=gnubash)" alt="Bash" />
        <img src="[https://img.shields.io/badge/Analytics-Regression_Modeling-blueviolet?style=flat-square](https://img.shields.io/badge/Analytics-Regression_Modeling-blueviolet?style=flat-square)" alt="Analytics" />
        <img src="[https://img.shields.io/badge/Status-Production_Ready-brightgreen?style=flat-square](https://img.shields.io/badge/Status-Production_Ready-brightgreen?style=flat-square)" alt="Status" />
      </p>
    </td>
    <td width="22%" align="center" valign="middle">
      <img src="./assets/escudo-unalm.png" width="120" alt="Escudo UNALM" />
    </td>
  </tr>
</table>

---

## 📌 Descripción General

Este repositorio está orientado a la analítica predictiva y endurecimiento de la seguridad (*hardening*) en infraestructura Linux. Analiza patrones de intrusión mediante modelado estadístico sobre logs del sistema operativo y automatiza respuestas defensivas en el cortafuegos.

---

## 🧩 Estructura por Mini-Proyectos

El proyecto está articulado en **3 miniproyectos modulares**:

### 📜 Mini-Proyecto 1: Parseo y Extracción de Syslogs Linux (`01-linux-log-parser`)
- **Objetivo:** Centralización y filtrado automático de registros del sistema para detectar actividad sospechosa.
- **Entregables:**
  - Extracción y normalización de logs `/var/log/auth.log`, `syslog` y auditorías de kernel (`auditd`).
  - Parsing de intentos fallidos de autenticación SSH, escalada de privilegios (`sudo`) y escaneo de puertos.
  - Exportación de métricas estructuradas en CSV y JSON.

### 📈 Mini-Proyecto 2: Modelado Predictivo de Intrusiones (`02-intrusion-probability-modeling`)
- **Objetivo:** Estimación de la probabilidad de compromiso del sistema mediante modelos estadísticos multivariados.
- **Entregables:**
  - Aplicación de **Regresión Logística** para predecir el éxito/fracaso de un ataque de fuerza bruta.
  - Modelos de conteo (**Regresión de Poisson / Binomial Negativa**) para cuantificar la frecuencia de ataques por intervalo de tiempo.
  - Validación de supuestos y bondad de ajuste del modelo predictivo.

### 🛡️ Mini-Proyecto 3: Automatización Defensiva y Reglas de Firewall (`03-automated-firewall-mitigation`)
- **Objetivo:** Scripting en Bash para el bloqueo predictivo y dinámico de amenazas detectadas.
- **Entregables:**
  - Scripts ejecutables en Bash que integran el modelo predictivo con el cortafuegos del sistema.
  - Bloqueo automático de IP maliciosas mediante actualización dinámica de reglas en `iptables` y `ufw`.
  - Sistema de registro auditable de acciones defensivas tomadas por el sistema.

---

## 📂 Estructura del Repositorio

```text
Predictive-Linux-Security-and-Data-Intrusion-Modeling/
├── assets/
│   ├── banner-binario.jpg
│   └── escudo-unalm.png
├── 01-linux-log-parser/
│   ├── scripts/
│   └── README.md
├── 02-intrusion-probability-modeling/
│   ├── notebooks/
│   └── README.md
├── 03-automated-firewall-mitigation/
│   ├── bash/
│   └── README.md
├── logs/
└── README.md
