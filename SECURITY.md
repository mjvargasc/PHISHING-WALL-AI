# Seguridad

PhishingWall AI es una herramienta educativa y preventiva. No garantiza la deteccion de todas las amenazas ni reemplaza soluciones profesionales de ciberseguridad.

## Reporte de vulnerabilidades

Reporta vulnerabilidades directamente a Mathias Javier Vargas Caicedo, titular de los componentes originales del proyecto. No publiques pruebas de explotación ni datos sensibles en issues públicos.

## Secretos y credenciales

- No commits de `.env`, tokens de Telegram, claves API, cookies, passwords, webhooks privados o credenciales de n8n.
- Usa `.env.example` como referencia publica.
- Si un secreto fue expuesto, revocalo o regeneralo antes de volver a usar la integracion.
- Revisa especialmente los JSON exportados desde n8n antes de publicarlos.

## Datos personales

- No agregues cedulas reales, conversaciones, historiales, bases de datos ni capturas con informacion personal.
- LANA solo valida estructura y digito verificador; no confirma identidad real.
- La aplicacion web actual no persiste datos ni envia entradas a servidores externos.

## Desarrollo seguro

- Evita `innerHTML` con contenido del usuario.
- Usa `textContent` y creacion segura de nodos.
- Normaliza y limita entradas del usuario.
- Mantén las integraciones externas desactivadas hasta configurar HTTPS, variables de entorno y permisos minimos.

## Limitaciones conocidas

- El analizador usa reglas heuristicas.
- No consulta inteligencia de amenazas en tiempo real.
- AURELIO no extrae metadatos, no hace OCR y no detecta manipulaciones visuales avanzadas.
- Las integraciones con Telegram/n8n dependen de configuracion externa segura.
