# PhishingWall AI

<img width="1024" height="1024" alt="image" src="https://github.com/user-attachments/assets/81a39141-160d-49c9-bdfc-e4c639125421" />


PhishingWall AI es una plataforma educativa y preventiva enfocada en detectar senales comunes de phishing en mensajes, enlaces, cedulas ecuatorianas e imagenes sospechosas. Esta version funciona como aplicacion web estatica y no envia los datos del usuario a servicios externos.

Mathias Javier Vargas Caicedo — Creador, autor, desarrollador principal y titular de PhishingWall AI.

Copyright © 2026 Mathias Javier Vargas Caicedo. Todos los derechos reservados.

PhishingWall AI fue desarrollado como un proyecto tecnologico, educativo y preventivo. No garantiza la deteccion de todas las amenazas ni sustituye herramientas profesionales de ciberseguridad.

## Problema

Los intentos de phishing suelen usar urgencia, enlaces acortados, dominios dudosos, solicitudes de credenciales y mensajes que imitan instituciones reales. PhishingWall AI ayuda a reconocer esas senales antes de abrir enlaces, responder mensajes o compartir datos.

## Caracteristicas

- Analizador de mensajes, enlaces y textos sospechosos.
- Deteccion de palabras de riesgo, enlaces acortados, HTTP sin cifrado, dominios raros y exceso de urgencia.
- Seccion visible "Prueba PhishingWall AI" con ejemplos rapidos ficticios y educativos.
- Modo demostracion local deterministico cuando no hay APIs externas configuradas.
- Boton para limpiar entradas y resultados.
- LANA: validacion local de cedula ecuatoriana con dato protegido, desenfoque visual y boton mostrar/ocultar.
- Demostracion de privacidad con codigo local `DEMO2026` y datos ficticios no oficiales.
- AURELIO: revision local de imagenes por nombre, formato y tamano del archivo.
- Imagen local ficticia para probar AURELIO.
- Plantilla sanitizada para documentar integracion con Telegram mediante n8n.
- Documentacion de seguridad, privacidad, instalacion y arquitectura.

## Capturas

<img width="1605" height="595" alt="image" src="https://github.com/user-attachments/assets/4842daa9-b1e8-41fa-ac16-7b4651adb5d3" />


Las capturas fueron generadas durante la verificacion local del proyecto.

## Tecnologias

- HTML5
- CSS3
- JavaScript moderno con ES modules
- Node.js solo para servidor local y pruebas
- n8n y Telegram como integraciones externas documentadas

## Estructura

```text
phishingwall-ai/
├── index.html
├── src/
│   ├── css/
│   ├── js/
│   ├── services/
│   └── utils/
├── assets/
│   ├── logos/
│   └── screenshots/
├── automation/
│   ├── n8n/
│   └── telegram/
├── docs/
│   └── legacy/
├── examples/
├── scripts/
└── tests/
```

No se crearon carpetas vacias para imagenes o capturas porque no habia recursos disponibles durante la inspeccion.

## Instalacion

Requisitos:

- Node.js 18 o superior para usar los scripts de desarrollo y pruebas.
- Un navegador moderno.

```bash
npm install
```

El proyecto no declara dependencias de produccion. `npm install` solo prepara el lockfile si se decide crearlo en el futuro.

## Ejecucion local

```bash
npm start
```

Luego abre `http://127.0.0.1:4173`.

Tambien puedes abrir `index.html` directamente, aunque el boton de ejemplos funciona mejor servido por HTTP porque carga `examples/safe-samples.json`.

## Pruebas

```bash
npm run check
```

Este comando ejecuta:

- Revision estatica contra `innerHTML`, `eval()` y patrones comunes de secretos.
- Pruebas de humo del analizador, LANA y AURELIO.

## Variables de entorno

Copia `.env.example` a `.env` solo en entornos locales o privados. No publiques `.env`.

```env
TELEGRAM_BOT_TOKEN=
N8N_WEBHOOK_URL=
API_BASE_URL=
ECUADOR_API_KEY=
```

La aplicacion estatica actual no lee `.env` directamente. Si se agrega backend o build tool, esas variables deben inyectarse sin exponer secretos en el cliente.

## n8n y Telegram

Los flujos externos no estaban disponibles en la carpeta inspeccionada. Se incluye una plantilla sanitizada en `automation/n8n/phishingwall-telegram-flow.example.json` y una guia en `docs/N8N_SETUP.md`.

No simules integraciones externas en produccion. Configura tokens, webhooks y credenciales dentro de n8n o variables de entorno privadas.

## Ejemplos seguros

Los ejemplos publicos estan en `examples/safe-samples.json` y tambien se muestran en la seccion visible "Prueba PhishingWall AI". No contienen cedulas reales, nombres de personas, cuentas bancarias, claves ni webhooks privados.

Cuando no hay servicio externo configurado, la interfaz muestra:

```text
Servicio externo no configurado. Se utilizó el análisis local de demostración.
```

La cedula `0000000000` aparece solo como `DEMOSTRACION - DATOS NO REALES`.

## Limitaciones conocidas

- El analisis es heuristico y educativo.
- No consulta listas negras en tiempo real.
- No confirma si una cedula pertenece a una persona real.
- AURELIO no realiza analisis forense ni OCR.
- La integracion con Telegram/n8n requiere configuracion externa.
- El modo demo no simula respuestas oficiales ni consultas externas.

## Privacidad y seguridad

La aplicacion no guarda historial, no envia datos a servidores y no incluye rastreadores. Evita ingresar datos reales si el repositorio se usa en demostraciones publicas. Consulta `docs/PRIVACY.md` y `SECURITY.md`.

## Estado actual

Version inicial organizada para GitHub: `1.0.0`.

## Autoría y créditos

### Creador y titular del proyecto

**Mathias Javier Vargas Caicedo**

Creador, autor, desarrollador principal y titular de PhishingWall AI.

La titularidad comprende los elementos originales del proyecto desarrollados por el autor. Las marcas, librerías, imágenes, tipografías y demás recursos pertenecientes a terceros conservan sus respectivos derechos y licencias.

### Representante

- **Karina Guadalupe Caicedo Ayala**

Representante de Mathias Javier Vargas Caicedo para efectos de acompañamiento y gestión relacionados con el proyecto.

### Colaboradores en la exposición académica

- **Delgado Chacón Samuel José**
- **Vélez Muñoz Ronald Steven**
- **Lenin Jacob Lucas Hoppe**

Los colaboradores mencionados participaron en la preparación, presentación y defensa académica de PhishingWall AI, pero no intervinieron directamente en el diseño, programación, fabricación o documentación técnica del producto.

La aparición de sus nombres reconoce su participación en la exposición y no los identifica como desarrolladores, programadores, autores, propietarios o titulares del software.

Para consultar la información completa sobre la autoría y participación, revisa [AUTHORS.md](AUTHORS.md).

Copyright © 2026 Mathias Javier Vargas Caicedo. Todos los derechos reservados.

## Licencia

Licencia propietaria. Todos los derechos reservados. Consulta `LICENSE` y `NOTICE.md`.
