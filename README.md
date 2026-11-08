# ffmpeg-aar-builder

Compila **FFmpegKitNext 9.0.2** (continuación oficial de FFmpegKit) para Android
**arm64-v8a** y publica el `.aar` como artefacto descargable.

## Qué genera

| Build | Contenido | Tiempo aprox. |
|-------|-----------|---------------|
| `core` | FFmpeg 9.0.2 solo, sin librerías externas | 25-40 min |
| `full-gpl` | FFmpeg 9.0.2 + todas las librerías externas, GPL | 60-120 min |

Solo `arm64-v8a` (64 bits); 32 bits y x86 quedan desactivadas.

## Cómo se usa

1. Actions → *FFmpeg AAR arm64* → **Run workflow**.
2. Al terminar, descarga `aar-core` o `aar-full-gpl`.
3. Dentro está `bundle-android-aar-<api>-maven/` con el `.aar`, su `.pom` y `build.log`.

El `.aar` se guarda una sola vez en el proyecto que lo consume; no se recompila para cada build de la app.
