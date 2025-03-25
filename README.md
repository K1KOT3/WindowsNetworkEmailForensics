# PR2 - Análisis Forense Avanzado

🕵️ **Investigación forense en entornos Windows y análisis de tráfico de red**  

Este repositorio contiene el informe de la **Práctica 2 de Análisis Forense Avanzado**, en el que se han llevado a cabo procedimientos detallados para la adquisición y análisis de evidencias digitales en **Windows y correos electrónicos**.

## 🔍 Descripción

Este análisis forense incluye:
- **Investigación en sistemas Windows**: Registro de conexiones activas, caché DNS y ARP, análisis de tráfico de red, y correlación de eventos sospechosos.
- **Forense en correos electrónicos**: Extracción de información de cabeceras SMTP, análisis de IPs, identificación de servidores de correo y trazabilidad de comunicaciones.
- **Uso de Wireshark** para el análisis de capturas de red, incluyendo tráfico HTTP, SMTP y TLS.
- **Identificación de amenazas** a través de herramientas y técnicas de ciberseguridad.

## 📁 Contenido del Repositorio

- `PR2.pdf` → Informe completo con el análisis forense y hallazgos clave.

## 🛠 Herramientas Utilizadas

### 🔹 **Forense en Windows**
- `netstat -an` → Listado de conexiones activas.
- `netstat -bano` → Relación de procesos y puertos abiertos.
- `ipconfig /displaydns` → Caché DNS del sistema.
- `arp -a` → Análisis de direcciones IP y MAC en la red.
- `tasklist /v` → Identificación de procesos en ejecución.
- `netstat -e` → Estadísticas de conexiones actuales.

### 🔹 **Forense en Email y Red**
- **Wireshark** → Análisis de tráfico SMTP, HTTP y TLS.
- Filtros aplicados en Wireshark:
  - `smtp.req.command`
  - `http.cookie`
  - `frame.number == X` (para análisis de tramas específicas).

## 🚀 Hallazgos Destacados

- **Detección de conexiones sospechosas** con servidores externos.
- **Análisis de ARP Spoofing** para identificar ataques MITM (Man-in-the-Middle).
- **Identificación de tráfico de malware** en conexiones TCP establecidas con direcciones de comando y control (C2).
- **Extracción de credenciales y metadatos de correos electrónicos** mediante análisis de cabeceras SMTP.

## 📜 Licencia

Este proyecto se distribuye bajo la licencia **MIT**. Consulta el archivo `LICENSE` para más detalles.
