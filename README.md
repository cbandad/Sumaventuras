# Sumaventuras

Juego educativo en español para practicar las tablas de sumar del 1 al 9. Incluye perfiles infantiles con progreso separado y opción de sincronización entre dispositivos.

## 1. Publicar en GitHub Pages

1. Sube los archivos del proyecto a la raíz de tu repositorio GitHub.
2. Entra en **Settings → Pages**.
3. En **Build and deployment**, selecciona **Deploy from a branch**, rama `main` y carpeta `/(root)`.
4. Pulsa **Save**. La web aparecerá en `https://TU-USUARIO.github.io/sumaventuras/`.

## 2. Activar sincronización entre dispositivos con Supabase

GitHub Pages solo aloja la web; para compartir el progreso entre dispositivos se necesita una base de datos online.

1. Crea un proyecto en [Supabase](https://supabase.com/).
2. En **SQL Editor**, crea una consulta nueva, pega el contenido de `supabase-setup.sql` y ejecútala.
3. En **Project Settings → API** (o **Connect**, según la interfaz), copia la URL del proyecto y la clave pública `anon` / publishable.
4. Copia `config.example.js` con el nombre `config.js` y sustituye `TU-PROYECTO` y `TU_CLAVE_PUBLICA_ANON` por tus valores.
5. Sube `config.js` a la raíz del repositorio. No publiques nunca una clave `service_role` o secret.
6. Recarga la web. Crea perfiles una vez; al abrir el juego desde otro dispositivo, selecciona el mismo nombre para cargar el progreso de la nube.

Si no configuras Supabase, los perfiles funcionan en modo local y los datos solo permanecen en ese navegador/dispositivo.

## Importante sobre perfiles solo con nombre

Esta versión implementa deliberadamente la entrada sin contraseña que has pedido. Por tanto, el nombre es una forma cómoda de seleccionar el perfil, no una identidad verificada: cualquiera que conozca la URL puede seleccionar o alterar los perfiles y su progreso. La política SQL es abierta para permitir el uso anónimo sin cuentas. Úsalo para un entorno familiar no sensible; si más adelante quieres proteger el progreso, habría que añadir autenticación o códigos de acceso y restringir las políticas de la base de datos.
