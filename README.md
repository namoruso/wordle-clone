# Wordle (Expo) — Proyecto

Versión local del juego Wordle creada con Expo + React Native. Incluye listas de palabras, modo para juegos combinatorios y soporte básico con Firebase para almacenamiento. Pensado para ejecución multiplataforma (iOS / Android / Web) mediante Expo.

## Características
- Juego Wordle en español e inglés.
- Listas de palabras amplias: [`allWords`](wordle/utils/allWords.ts) y [`words`](wordle/utils/targetWords.ts).
- Interfaz basada en Expo + React Native con layout global: [app/_layout.tsx](app/_layout.tsx) y pantalla principal: [app/index.tsx](app/index.tsx).
- Modal de suscripción: [`SubscribeModal`](wordle/components/SubscribeModal.tsx).
- Persistencia/servicios: configuración Firebase en [`FIREBASE_DB`](wordle/utils/FirebaseCongig.ts).
- Script de utilidad para reiniciar el proyecto: [app-example/scripts/reset-project.js](app-example/scripts/reset-project.js).
- Nuevo modo de dificultad: permite seleccionar niveles (Fácil / Normal / Difícil) que ajustan la longitud de la palabra objetivo, el número de intentos y las pistas disponibles.
- Modo "Estructuras Discretas": modo alternativo con vocabulario técnico y reglas adaptadas para practicar términos y problemas propios de estructuras discretas (activable desde la pantalla de selección de juego).

## Tecnologías
- Expo (React Native)
- TypeScript
- Firebase (Firestore)
- Clerk para autenticación (opcional)
- @gorhom/bottom-sheet, @expo-google-fonts, react-native-mmkv, etc. (ver [package.json](package.json))

## Estructura relevante
- [app/index.tsx](app/index.tsx) — Pantalla principal / navegación.
- [app/_layout.tsx](app/_layout.tsx) — Proveedor de temas, navegación y splash.
- [app/end.tsx](app/end.tsx) — Pantalla de fin de partida (compartir resultados).
- [wordle/utils/allWords.ts](wordle/utils/allWords.ts) — Lista completa de palabras válidas.
- [wordle/utils/targetWords.ts](wordle/utils/targetWords.ts) — Palabras objetivo/day list (`words`).
- [wordle/utils/FirebaseCongig.ts](wordle/utils/FirebaseCongig.ts) — Inicialización de Firebase y exportación de [`FIREBASE_DB`](wordle/utils/FirebaseCongig.ts).
- [wordle/components/SubscribeModal.tsx](wordle/components/SubscribeModal.tsx) — Modal de suscripción.
- [package.json](package.json) — Scripts y dependencias.
- [.gitignore](.gitignore) — Archivos ignorados por Git.


## Instalación y ejecución (local)

1. Clonar el repositorio desde GitHub y situarse en la carpeta del proyecto:
   ```bash
   git clone https://github.com/<usuario>/<repositorio>.git
   cd <repositorio>
   ```
   Reemplace `<usuario>` y `<repositorio>` por los valores reales del repositorio en GitHub.

2. Instalar dependencias:
   ```powershell
   npm install
   ```

3. (Opcional) Crear o revisar el archivo de entorno si el proyecto lo requiere:
   ```powershell
   copy .env.example .env
   # Editar .env según sea necesario
   ```

4. Ejecutar en modo desarrollo (Expo):
   ```powershell
   npm run start
   ```

5. Ejecutar en emulador o dispositivo:
   ```powershell
   npm run android   # Para Android
   npm run ios       # Para iOS (macOS necesario)
   ```

Notas:
- En Windows use PowerShell o la terminal integrada de VS Code.
- Asegúrese de disponer de Expo CLI y las herramientas de desarrollo nativas si desea ejecutar en dispositivos/emuladores.
- Actualice los scripts en package.json si su flujo de trabajo difiere.
