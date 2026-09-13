## Uso

Esta herramienta está diseñada para ejecutarse en entornos locales o servidores de retransmisión intermedia. Sigue estos pasos para inicializar el optimizador de stream de manera automatizada.

### Requisitos Previos

Asegúrate de contar con Python 3.8+ instalado en tu sistema. No requiere dependencias externas complejas de red al basarse en peticiones nativas de optimización de sockets y empaquetamiento de parámetros URL para VDO.ninja.

### Ejecución Básica

Para generar los enlaces optimizados forzando el perfil de ultra-bajo consumo y empaquetado automático de tokens, ejecuta el script principal en tu terminal:

```bash
python generador_112p.py
```

### Parámetros de Optimización Aplicados

El script inyectará de forma automática las siguientes directivas de rendimiento en los tokens de sesión de VDO.ninja:

* **Restricción de Bitrate:** Fuerza el límite de transferencia a `~62 kbps` para priorizar la estabilidad del audio y la continuidad sobre la resolución de video pesada.
* **Control de Latencia Activo:** Ajusta dinámicamente los buffers de retransmisión para evitar la acumulación de retraso bajo redes móviles o inestables.
* **Persistencia de Sesión:** Monitorea y reencampa automáticamente los tokens expirados o caídos para evitar desconexiones del flujo de trabajo de producción.

