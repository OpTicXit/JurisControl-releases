<p align="center"><img src="assets/icon.png" width="96" alt="JurisControl"></p>

# JurisControl

Aplicación de escritorio para **Windows** dirigida a abogados colombianos. Con ella puede llevar el control de sus expedientes, las etapas de cada proceso con su fecha de inicio y su fecha final, los documentos anexos y los **vencimientos de términos**. Le avisa con **notificaciones de Windows** antes de que un término venza.

Funciona **sin internet** y guarda la información solo en su computador. Solo necesita conexión para buscar actualizaciones.

---

## Contenido
1. [Descargar e instalar](#1-descargar-e-instalar)
2. [Actualizaciones](#2-actualizaciones)
3. [Funciones](#3-funciones)
4. [Guía rápida de uso](#4-guía-rápida-de-uso)
5. [Cómo se cuentan los términos](#5-cómo-se-cuentan-los-términos)
6. [Sus datos y respaldos](#6-sus-datos-y-respaldos)
7. [Preguntas frecuentes](#7-preguntas-frecuentes)
8. [Para desarrolladores](#8-para-desarrolladores)

---

## 1. Descargar e instalar

**Requisitos:** Windows 10 u 11 de 64 bits. No requiere permisos de administrador.

1. Entre a la página de descargas: **https://github.com/OpTicXit/JurisControl-releases/releases/latest**
2. En la sección **Assets**, descargue el archivo `JurisControl-Instalador-X.Y.Z.exe` (X.Y.Z es el número de versión).
3. Abra el archivo descargado y siga los pasos del instalador. Puede elegir la carpeta de instalación.
4. Si Windows SmartScreen muestra el aviso *"Windows protegió su PC"*, haga clic en **Más información → Ejecutar de todas formas**. El aviso aparece porque el instalador no tiene una firma digital comercial; no indica un problema con el programa.
5. Al terminar se crean accesos directos en el **Escritorio** y en el **menú Inicio**.

> No descargue los archivos `latest.yml` ni `.blockmap` de la página de descargas. El programa los usa internamente para actualizarse.

## 2. Actualizaciones

JurisControl se mantiene al día solo:

- **Al iniciar** y luego **cada 6 horas**, busca si hay una versión nueva.
- Si la encuentra, la **descarga en segundo plano** y comprueba que el archivo esté completo y sin alteraciones.
- Cuando la descarga termina, aparece una notificación de Windows y el botón de la barra lateral cambia a **"Instalar versión X.Y.Z"**.
- Al pulsarlo, el programa se cierra, instala la nueva versión y vuelve a abrirse. Si prefiere no reiniciar en ese momento, la actualización se instala la próxima vez que cierre JurisControl por completo.

**Buscar una actualización a mano:**
- Botón **Buscar actualizaciones**, en la parte inferior de la barra lateral.
- **Configuración → Actualizaciones → Buscar actualizaciones**, donde también se ve el estado (buscando, descargando, al día).
- Clic derecho en el ícono de JurisControl junto al reloj → **Buscar actualizaciones**.

**Sus expedientes, documentos y configuración no se tocan al actualizar.** Se guardan aparte, en `%APPDATA%\JurisControl`. Al pasar de la versión 1.0 a una versión con cuentas, el programa le pide crear su cuenta y sus expedientes pasan a ella.

## 3. Funciones

**Cuentas por abogado**
- Cada abogado entra con su **usuario y contraseña** y solo ve sus propios clientes, expedientes y documentos. En un mismo computador puede haber varias cuentas.
- Los datos de cada cuenta se guardan **cifrados** con su contraseña.
- Al crear la cuenta se entrega un **código de recuperación**. Si olvida la contraseña, ese código permite crear una nueva sin perder nada.
- **Recordar sesión en este equipo:** el programa entra solo y las alertas funcionan desde que Windows arranca.

**Expedientes**
- Datos del cliente: nombre, tipo y número de documento, teléfono, correo, dirección y ciudad.
- Datos del proceso: radicado, tipo de caso, entidad, juzgado, fecha de apertura, honorarios, estado (Activo, En espera, Cerrado, Archivado) y prioridad.
- Información adicional de texto libre, que se guarda mientras escribe.
- Bitácora de actuaciones: el programa registra algunos hechos solo (por ejemplo, cuando se finaliza una etapa) y usted puede agregar notas propias.

**Etapas del proceso**, cada una con fecha de inicio, fecha final, estado (Pendiente, En curso, Finalizada, Suspendida), observaciones y campos propios:

| Etapa | Término sugerido | Norma de referencia |
|---|---|---|
| Derecho de petición | 15 días hábiles | Ley 1755 de 2015, art. 14 |
| Acción de tutela | 10 días hábiles | Decreto 2591 de 1991, art. 29 |
| Impugnación de tutela | 20 días hábiles | Decreto 2591 de 1991, arts. 31 y 32 |
| Incidente de desacato | 10 días hábiles | Decreto 2591 de 1991, arts. 27 y 52 |
| Proceso de calificación PCL | Lo define usted | Decreto 019 de 2012, art. 142 |
| Junta Regional de Invalidez | Lo define usted | Decreto 1072 de 2015 |
| Junta Nacional de Invalidez | Lo define usted | — |
| Proceso de pago | Lo define usted | — |
| Otra actuación | Lo define usted | Recurso, audiencia, demanda, conciliación, etc. |

**Documentos y anexos**
- Adjunte PDF, Word, Excel, imágenes, correos y otros archivos a cada expediente y, si quiere, a una etapa.
- Categorías: poder, documento de identidad, historia clínica, dictamen, fallo o auto, recurso, comprobante de pago, contrato de honorarios, entre otras.
- El programa guarda **una copia** del archivo, así que puede mover o borrar el original sin perder el anexo.
- **Buscador** (menú **Buscar** o **Ctrl + F**): encuentra clientes, expedientes y documentos escribiendo cualquier dato (nombre, cédula, radicado, entidad, nombre del archivo, descripción…), con o sin tildes. Puede filtrar solo documentos o una categoría para verlos todos organizados, del más reciente al más antiguo.

**Papelera y protección contra borrados**
- Los expedientes y documentos que elimine van a la **Papelera**, donde puede **restaurarlos durante 30 días**. Después se borran solos.
- **Copia automática diaria** (opcional) a la carpeta que elija: una USB, OneDrive o Google Drive. Los documentos que borre siguen guardados en esa copia.

**Alertas y notificaciones**
- Avisos de Windows para términos **vencidos**, que **vencen hoy** o que están **próximos a vencer** (por defecto, con 3 días de anticipación; usted puede cambiarlo).
- **Sonidos propios** de JurisControl: uno insistente para términos vencidos o que vencen hoy, uno suave para avisos de próximos vencimientos y recordatorios, y uno alegre cuando hay una actualización lista. Puede escucharlos o desactivarlos en **Configuración**.
- Centro de notificaciones dentro de la app, con contador de alertas sin leer.
- Recordatorios personales con fecha y hora.
- Sigue funcionando desde la **bandeja del sistema** (junto al reloj) aunque cierre la ventana, y puede **iniciar con Windows**.

**Herramientas**
- Panel con próximos vencimientos y recordatorios del día.
- Calendario mensual de vencimientos.
- Calculadora de términos en días hábiles o calendario.
- Reportes por estado y exportación a Excel (CSV) de expedientes y términos.
- Tema claro y oscuro.
- Atajos: **Ctrl + N** crea un expediente y **Ctrl + F** abre el buscador.

## 4. Guía rápida de uso

1. **Cree su cuenta** la primera vez que abra el programa. **Guarde el código de recuperación** (en un archivo fuera del computador o impreso): es la única forma de entrar si olvida la contraseña. Si ya usaba JurisControl 1.0 en ese equipo, sus expedientes pasan a esta primera cuenta.
2. **Configure sus datos:** en **Configuración** escriba su nombre y tarjeta profesional, y elija con cuántos días de anticipación quiere los avisos. Pulse **Probar notificación** para confirmar que Windows muestra los avisos.
3. **Active la copia automática diaria:** **Configuración → Respaldo → Elegir carpeta** (por ejemplo, su carpeta de OneDrive).
4. **Cree un expediente:** **Expedientes → Nuevo expediente**. Solo el nombre del cliente es obligatorio.
5. **Agregue una etapa:** dentro del expediente, en la pestaña **Etapas**, elija el tipo. El programa propone el término legal y calcula la fecha final; usted puede cambiar ambos.
6. **Adjunte documentos:** en la pestaña **Documentos**, elija los archivos y su categoría. La categoría le ayuda a encontrarlos después en **Buscar**.
7. **Cierre la etapa** cuando termine, con **Finalizar**. Las etapas finalizadas y los expedientes cerrados o archivados dejan de generar alertas.
8. **Revise el Panel** cada día, o deje que las notificaciones le avisen.

## 5. Cómo se cuentan los términos

- El conteo empieza **el día siguiente** a la fecha de inicio.
- Los **días hábiles** excluyen sábados, domingos y **festivos de Colombia**: los fijos, los que se trasladan al lunes por la Ley Emiliani (Ley 51 de 1983) y los que dependen de la Pascua.
- Si activa **Descontar vacancia judicial** en Configuración, también se descuentan del 20 de diciembre al 10 de enero y de lunes a miércoles de Semana Santa.

> **Importante:** los términos sugeridos son **orientativos**. Verifique siempre la norma aplicable y lo que disponga el despacho. JurisControl no reemplaza el criterio del abogado.

## 6. Sus datos y respaldos

- Cada cuenta guarda su información en `%APPDATA%\JurisControl\cuentas\<cuenta>` (puede abrir esa carpeta desde **Configuración → Abrir carpeta de datos**):
  - `datos.json`: expedientes, etapas, recordatorios y configuración, **cifrados** con su contraseña.
  - `anexos\`: copia de los documentos de cada expediente. Los documentos **no** van cifrados, para que Word, Excel o el lector de PDF puedan abrirlos.
  - `papelera\`: documentos eliminados de los últimos 30 días.
  - `respaldos\`: copia automática diaria de los datos; se conservan los últimos 15 días.
- **Copia automática diaria a una carpeta** (Configuración → Respaldo): cada día copia datos y documentos a la carpeta que elija. Esta copia y la de **Exportar respaldo** van **sin cifrar**, para poder restaurarlas en otro equipo: guárdelas en una carpeta privada.
- **Exportar respaldo** (Configuración) copia datos y anexos a la carpeta que elija, en el momento.
- **Restaurar respaldo** recupera una copia exportada. Antes de reemplazar, el programa guarda una copia de seguridad de los datos actuales.
- **Al desinstalar no se borran sus datos.** Si reinstala, todo vuelve a aparecer.
- **Cambiar de computador:** exporte el respaldo en el equipo viejo, instale JurisControl en el nuevo y use **Restaurar respaldo**.

## 7. Preguntas frecuentes

**Olvidé mi contraseña.**
En la pantalla de inicio pulse **Olvidé mi contraseña**, escriba su usuario y el código de recuperación, y elija una contraseña nueva. Sus datos se conservan y el programa le entrega un código nuevo (el anterior deja de servir). **Sin la contraseña ni el código no es posible recuperar los datos**, porque van cifrados; en ese caso solo queda restaurar una copia exportada o la copia automática.

**Borré un documento o un expediente por error.**
Abra **Papelera** y pulse **Restaurar**. Si pasaron más de 30 días, búsquelo en la carpeta de la copia automática diaria.

**Varios abogados usamos el mismo computador.**
Cada uno crea su cuenta (en la pantalla de inicio: **Crear otra cuenta**) y desactiva **Recordar sesión en este equipo**. Al terminar, pulse **Cerrar sesión**. Las alertas suenan solo para la cuenta que tenga la sesión abierta.

**No me llegan las notificaciones.**
Revise que estén activas en **Configuración → Notificaciones de escritorio**. Revise también la configuración de Windows (**Inicio → Configuración → Sistema → Notificaciones**): JurisControl debe estar permitido y el modo **No molestar** debe estar desactivado.

**Cerré la ventana, ¿sigue avisando?**
Sí, si está activa la opción **Seguir activo en la bandeja al cerrar**. Para salir del todo, haga clic derecho en el ícono junto al reloj → **Salir**.

**El botón de actualizar dice que no se pudo buscar.**
Revise su conexión a internet e intente de nuevo. El resto del programa funciona igual sin conexión.

**¿Mis datos se envían a algún servidor?**
No. JurisControl no envía expedientes ni documentos a ningún lado. Solo consulta GitHub para saber si hay una versión nueva.

---

## 8. Para desarrolladores

### Requisitos
- Windows 10 u 11
- [Node.js](https://nodejs.org) 18 o superior (incluye npm)
- [Git](https://git-scm.com), con acceso al repositorio privado `OpTicXit/JurisControl`

### Tecnología
Electron 33 y electron-builder 25, con **JavaScript sin frameworks** y sin bundler. No usa módulos nativos: los datos se guardan en JSON. Las actualizaciones usan [electron-updater](https://www.electron.build/auto-update) con GitHub Releases.

### Primeros pasos
```powershell
git clone https://github.com/OpTicXit/JurisControl.git
cd JurisControl
npm install
npm start
```
Con npm 11 o superior, si Electron no arranca después de `npm install`, ejecute `npm rebuild electron`. El permiso para su script de instalación ya está en `package.json` (`allowScripts`).

### Comandos
| Comando | Qué hace |
|---|---|
| `npm start` | Ejecuta la app en modo desarrollo. El botón de actualizar solo funciona en la versión instalada. |
| `npm run dist` | Genera el instalador en `dist\` sin publicarlo. |
| `npm run dist:dir` | Genera la carpeta `dist\win-unpacked` sin instalador, para pruebas rápidas. |
| `npm run publicar` | Genera el instalador y lo **publica como actualización** en GitHub Releases. |

### Estructura
```
main.js              Proceso principal: datos, IPC, alertas, bandeja, notificaciones, respaldos y actualizaciones
preload.js           Puente seguro window.api entre la interfaz y el proceso principal
renderer/index.html  Esqueleto de la ventana y barra lateral
renderer/styles.css  Estilos (tema claro y oscuro)
renderer/calendario.js  Festivos de Colombia, días hábiles y vacancia judicial
renderer/app.js      Interfaz: catálogos, vistas, modales y acciones
publicar.mjs         Compila y publica una nueva versión en GitHub Releases
assets/              Ícono de la aplicación y sonidos (assets/sonidos)
installer.nsi, build-seticon.mjs  Solo para compilar desde Linux
```
Las reglas de trabajo del proyecto (seguridad, modelo de datos, migraciones, reglas del negocio) están en el archivo `CLAUDE.md` del repositorio de código.

### Cómo publicar una nueva versión
Los programas instalados se actualizan desde el repositorio público **[OpTicXit/JurisControl-releases](https://github.com/OpTicXit/JurisControl-releases/releases)**. El código fuente sigue privado.

1. Trabaje en una rama (`feat/...` o `fix/...`), pruebe con `npm start` y una los cambios a `main`.
2. Suba el número de versión en `package.json`:
   - `1.0.0 → 1.0.1` para correcciones,
   - `1.0.0 → 1.1.0` para funciones nuevas,
   - `1.0.0 → 2.0.0` para cambios grandes.

   ```powershell
   npm version patch
   ```
   (o `npm version minor` / `npm version major`). El comando también crea el commit y la etiqueta de la versión.
3. Publique:
   ```powershell
   npm run publicar
   ```
   El script usa la sesión de GitHub que Git ya tiene guardada en Windows. Otra opción es definir la variable `GH_TOKEN` con un token que tenga permiso sobre `JurisControl-releases`.
4. Suba el código y la etiqueta al repositorio privado:
   ```powershell
   git push --follow-tags
   ```
5. En pocas horas, o enseguida si el usuario pulsa **Buscar actualizaciones**, todos los equipos con JurisControl instalado reciben la versión nueva.

> Si cambia la estructura de `datos.json`, suba `version` dentro de los datos y agregue una migración en `loadData()` (ver CLAUDE.md). Los usuarios conservan su información al actualizar, así que **nunca rompa datos existentes**.

### Licencia
MIT.
