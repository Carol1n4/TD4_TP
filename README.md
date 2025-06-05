# Trabajo Práctico: Protocolo ICMP - Ping con Scapy

**Primer semestre 2025**

## 🧠 Introducción

En este trabajo práctico se explorará el protocolo ICMP, su funcionamiento y cómo se puede utilizar para implementar herramientas como Ping. El objetivo es implementar la herramienta Ping en Python usando la librería Scapy, experimentar con ella y compararla con implementaciones existentes.

## 🌐 Contexto

Ping permite verificar si un host es accesible mediante una red IP y medir la latencia entre dos nodos. Funciona enviando paquetes ICMP *echo request* y esperando respuestas *echo reply*. Mide RTT (round-trip time), pérdida de paquetes y genera estadísticas como:

- RTT mínimo, máximo, promedio
- Porcentaje de pérdida
- Desvío estándar

Para implementarlo, basta con enviar paquetes ICMP, registrar respuestas y procesar los resultados.

## 🧩 Ejercicios

### 1. Investigación sobre ICMP
Responder:
- a. ¿Cuál es la función del protocolo ICMP?
- b. ¿Qué tipos de mensaje ICMP existen y cuáles se usan en `ping`?
- c. ¿Qué es `Traceroute` y cómo se implementa con mensajes ICMP (Time Exceeded)?

### 2. Implementación de Ping en Python 3 con Scapy
- a. Mostrar para cada respuesta:
  - Longitud del paquete
  - RTT
  - TTL
- b. Al finalizar múltiples envíos, mostrar:
  - i. Paquetes enviados
  - ii. Paquetes recibidos
  - iii. Paquetes perdidos
  - iv. Porcentaje de pérdida
  - v. RTT promedio
  - vi. RTT máximo
  - vii. RTT mínimo
  - viii. Desvío estándar del RTT (usar `statistics.stdev()`)
- c. Recomendación: crear una función para enviar un solo paquete ICMP y reutilizarla.

### 3. Manejo de errores ICMP tipo 3 (Destination Unreachable)
Interpretar códigos como:
- 0: Destination Network Unreachable
- 1: Destination Host Unreachable

Mostrar el error correspondiente en la terminal.

## 📊 Experimentación e Informe

### 4. Ping a 5 universidades de distintos continentes
- a. Analizar diferencia de RTT entre universidades. ¿A qué se puede deber?
- b. Comparar herramienta propia con el `ping` nativo del sistema.
- c. Incluir al menos 2 gráficos con los resultados.

### 5. Medición diaria por una semana
- Realizar pings a una misma universidad en distintos momentos del día (mañana, tarde, noche).
- Analizar diferencias y posibles causas.

## 📦 Entrega

- Trabajo en grupos de **3 estudiantes**.
- Entregar un `.zip` con:
  - Informe en formato PDF
  - Código Python / Jupyter Notebook

**Fecha límite de entrega: 22/06 a las 23:59 hs**

> ⚠️ No se aceptarán entregas fuera de término.
