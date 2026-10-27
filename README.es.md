# TDevTools

**Un conjunto gratuito de herramientas de escritorio para desarrolladores: 47 herramientas para JSON, XML, esquemas, API, codificación y certificados, disponible para macOS, Windows y Linux.**

Por [transposal.app](https://transposal.app)

**Leer en:** [English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Türkçe](README.tr.md) · [日本語](README.ja.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md)

> **🔒 Funciona localmente. Tus datos nunca salen de tu equipo.** TDevTools procesa todo en tu ordenador. Tus archivos JSON y XML, tokens, claves y certificados no se suben ni se envían a analíticas. No hay cuentas ni seguimiento. La aplicación solo se conecta a Internet cuando tú lo solicitas: al cargar una URL, enviar una petición de prueba a tu API o consultar el certificado de un servidor. El resto de herramientas funciona sin conexión.

## Capturas de pantalla

**JSON → JSON Schema:** genera un esquema a partir de datos de ejemplo.

![JSON a JSON Schema](screenshots/json-to-schema.png)

**Probador de API:** envía solicitudes y consulta respuestas como árbol, tabla o texto.

![Probador de API](screenshots/api-tester.png)

**Inspector de certificados:** consulta la cadena de certificados y verifica certificados y firmas.

![Inspector de certificados](screenshots/certificate-inspector.png)

## Descarga

Descarga la versión más reciente desde la página de [versiones](https://github.com/siddiquin/TDevTools-releases/releases/latest).

| Sistema | Archivo |
| --- | --- |
| macOS, Apple Silicon (M1–M4) | `TDevTools-<version>-arm64.dmg` |
| macOS, Intel | `TDevTools-<version>-x64.dmg` |
| Windows 10/11, 64 bits | `TDevTools-Setup-<version>-x64.exe` |
| Windows 10/11, ARM | `TDevTools-Setup-<version>-arm64.exe` |
| Windows, portable | `TDevTools-Portable-<version>.exe` |
| Linux, 64 bits (x86_64) | `TDevTools-<version>-x86_64.AppImage` |
| Linux, ARM64 | `TDevTools-<version>-arm64.AppImage` |

**Requisitos:** macOS 12 Monterey o posterior; Windows 10 u 11 (64 bits o ARM64); o una distribución Linux reciente de 64 bits (Ubuntu 20.04+, Debian 11+, Fedora 36+ o similar). Se necesitan unos 300 MB de espacio.

## Instalación

### macOS

1. Descarga el archivo `.dmg` adecuado, ábrelo y acepta el acuerdo de licencia.
2. Arrastra **TDevTools** a la carpeta **Aplicaciones** y expulsa la imagen de disco.
3. La primera vez, macOS puede avisar de que la aplicación no se puede verificar porque no tiene un certificado de desarrollador de pago. Es lo esperado; solo tienes que autorizarla una vez.
   - **macOS 14 o anterior:** en Finder, haz clic derecho en TDevTools y elige **Abrir**; confirma con **Abrir**.
   - **macOS 15 o posterior:** intenta abrirla y pulsa **Hecho** en el aviso. Ve a **Ajustes del Sistema → Privacidad y seguridad** y selecciona **Abrir igualmente** junto al aviso de TDevTools. Confirma la acción.
4. Si aparece «TDevTools está dañado y no se puede abrir», comprueba primero que lo descargaste de la página oficial de [versiones](https://github.com/siddiquin/TDevTools-releases/releases/latest). Después, en Terminal, ejecuta `xattr -dr com.apple.quarantine /Applications/TDevTools.app` para quitar la marca de descarga de esta aplicación.

### Windows

- **Instalador:** ejecuta `TDevTools-Setup-<version>-x64.exe` (o el archivo `arm64` para equipos ARM), acepta la licencia y pulsa **Instalar**. Si SmartScreen muestra «Windows protegió su PC», selecciona **Más información → Ejecutar de todas formas**. Se instala solo para tu cuenta, sin permisos de administrador.
- **Portable:** ejecuta `TDevTools-Portable-<version>.exe`. Si aparece SmartScreen, selecciona **Más información → Ejecutar de todas formas**.

### Linux (AppImage)

Descarga el archivo adecuado, dale permiso de ejecución desde **Propiedades → Permisos** o con `chmod +x TDevTools-*.AppImage`, y ábrelo o ejecútalo desde Terminal. Si no inicia, algunas distribuciones necesitan FUSE 2 (por ejemplo, Ubuntu/Debian: `sudo apt install libfuse2`; Ubuntu 24.04: `sudo apt install libfuse2t64`; Fedora: `sudo dnf install fuse-libs`). Para añadirlo al menú de aplicaciones, puedes usar Gear Lever o AppImageLauncher.

## Actualización y desinstalación

Para actualizar, descarga la nueva versión e instálala igual que la anterior; tus preferencias se conservan. En macOS, reemplaza la aplicación en Aplicaciones; en Windows, ejecuta el nuevo instalador; en Linux, sustituye el AppImage.

- **macOS:** mueve TDevTools a la Papelera. Para borrar también la configuración, elimina `~/Library/Application Support/TDevTools`.
- **Windows:** desinstala TDevTools en **Configuración → Aplicaciones → Aplicaciones instaladas**. Para borrar la configuración, elimina `%APPDATA%\TDevTools`. En la versión portable, elimina el `.exe`.
- **Linux:** elimina el AppImage. Para borrar la configuración, elimina `~/.config/TDevTools`.

La aplicación solo guarda preferencias, como el tema y el idioma; nunca conserva copias de tus datos, contraseñas o claves.

## Funciones

- **Formato y validación:** formateador, validador, reparación y editor visual de JSON; conversión entre JSON, XML, CSV, Excel, YAML, TOON y JSONL; Markdown y esquemas JSON/XML (XSD); generación de tipos TypeScript.
- **Seguridad:** decodificación, verificación y firma de JWT; codificación Base64/URL/SAML; hashes MD5, SHA-1 y SHA-256; certificados autofirmados y kits mTLS; inspector de certificados, claves públicas y almacenes JKS.
- **Visores y API:** vistas de JSON en árbol, tabla, cuadrícula, gráfico y texto; explorador OpenAPI/Swagger, cliente HTTP con OAuth2 y mTLS, visor SOAP/WSDL, visor de archivos y vista previa Markdown.
- **Consultas y transformación:** probador JSONPath, búsqueda y reemplazo con expresiones regulares, mapeo JSON exportable a JavaScript, TypeScript, Python o C#; Transposal Mapper opcional para transformaciones en la nube.
- **Comparación:** diferencias estructurales de JSON/XML y validación de esquemas JSON con errores por línea.
- **En toda la aplicación:** 8 idiomas, 6 temas, colores de acento, opciones de densidad y zoom, copia con un clic, menú contextual, arrastrar y soltar, y uso de CPU y memoria en la barra de estado.

## Privacidad y seguridad

- Todo el procesamiento se realiza en tu equipo: nada de lo que pegues o abras se sube.
- Sin cuentas, telemetría ni anuncios.
- Solo se conecta a la red cuando lo solicitas, por ejemplo, al cargar una URL, probar una API o consultar certificados.
- Las contraseñas, tokens y claves privadas solo permanecen en memoria mientras la aplicación está abierta; solo se guardan tus preferencias.
- Ventanas aisladas y política de seguridad de contenido estricta; las vistas previas HTML no ejecutan scripts; la aplicación pide permiso antes de abrir programas o scripts; los datos de inicio de sesión solo se envían al servidor que elegiste.
- Los ejemplos integrados usan servidores públicos de demostración y están limitados a una solicitud cada 2 minutos. Tus propias URL y archivos no tienen límite.

## Preguntas frecuentes

**¿TDevTools es gratis?** Sí, es gratis para desarrolladores. Consulta el [Acuerdo de licencia](LICENSE.md).

**¿Funciona sin conexión?** Sí, salvo las funciones que necesitan comunicarse con un servidor que elijas, como cargar una URL, probar API o SOAP y consultar una cadena de certificados.

**¿El código fuente está disponible?** TDevTools es de código cerrado. Puedes solicitarlo por correo a **<support@transposal.app>**, con el asunto «TDevTools».

**¿Por qué aparecen avisos de seguridad al instalar?** La aplicación no tiene un certificado de desarrollador de pago de Apple o Microsoft, por lo que Gatekeeper y SmartScreen muestran un aviso la primera vez. Sigue los pasos de instalación y descarga solo desde la página oficial de [versiones](https://github.com/siddiquin/TDevTools-releases/releases/latest).

## Licencia y soporte

- [Acuerdo de licencia de usuario final](LICENSE.md): uso gratuito, sin garantía. El acuerdo completo está disponible en 8 idiomas dentro de la aplicación, en **Ayuda → Acuerdo de licencia**.
- [Avisos de terceros](THIRD_PARTY_NOTICES.md)
- Soporte: **<support@transposal.app>**
- Sitio web: [transposal.app](https://transposal.app)

© 2026 Transposal. Todos los derechos reservados.