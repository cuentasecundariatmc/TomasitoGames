# La Palabra del Día — app para Android

Este proyecto envuelve el juego (`app/src/main/assets/index.html`) en una app Android.
Funciona sin internet y no pide ningún permiso.

El APK que se genera es de tipo "debug": sirve para instalar en tu celular, pero no para subir a Google Play.

## Camino A: sacar el APK con GitHub (gratis, sin instalar nada)

1. Creá una cuenta gratuita en github.com y un repositorio nuevo (por ejemplo `palabra-del-dia`).
2. Subí **todo el contenido de esta carpeta** al repositorio (botón "Add file" > "Upload files").
   - Asegurate de que se suba también la carpeta oculta `.github`. Si tu sistema no la muestra,
     entrá al repo > pestaña **Actions** > "set up a workflow yourself", pegá el contenido de
     `.github/workflows/build-apk.yml` y guardalo con ese mismo nombre.
3. Abrí la pestaña **Actions**. Si no arrancó sola, elegí "Compilar APK" > **Run workflow**.
4. Esperá unos 3 a 6 minutos hasta que aparezca el tilde verde.
5. Entrá a esa ejecución y, abajo en **Artifacts**, descargá `la-palabra-del-dia-apk`.
   Adentro del ZIP está `app-debug.apk`.

## Camino B: con Android Studio

1. Abrí Android Studio > **Open** > elegí esta carpeta y esperá a que termine "Gradle sync".
2. Menú **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
3. El archivo queda en `app/build/outputs/apk/debug/app-debug.apk`.

## Instalar en el celular

1. Pasá `app-debug.apk` al teléfono (cable, Drive, WhatsApp, mail).
2. Abrilo desde "Archivos". Android va a pedir permiso para **instalar apps de esta fuente**: aceptalo.
3. Si Google Play Protect muestra un aviso, elegí "Instalar de todos modos" (es tu propia app).

## Cambiar el juego más adelante

Reemplazá `app/src/main/assets/index.html` por la nueva versión y volvé a compilar.
