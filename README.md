# Welcome to your Expo app 👋

This is an [Expo](https://expo.dev) project created with [`create-expo-app`](https://www.npmjs.com/package/create-expo-app).

## Get started

1. Install dependencies

   ```bash
   npm install
   ```

2. Start the app

   ```bash
   npx expo start
   ```

In the output, you'll find options to open the app in a

- [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go), a limited sandbox for trying out app development with Expo

You can start developing by editing the files inside the **app** directory. This project uses [file-based routing](https://docs.expo.dev/router/introduction).

## Get a fresh project

When you're ready, run:

```bash
npm run reset-project
```

This command will move the starter code to the **app-example** directory and create a blank **app** directory where you can start developing.

## Learn more

To learn more about developing your project with Expo, look at the following resources:

- [Expo documentation](https://docs.expo.dev/): Learn fundamentals, or go into advanced topics with our [guides](https://docs.expo.dev/guides).
- [Learn Expo tutorial](https://docs.expo.dev/tutorial/introduction/): Follow a step-by-step tutorial where you'll create a project that runs on Android, iOS, and the web.

## Join the community

Join our community of developers creating universal apps.

- [Expo on GitHub](https://github.com/expo/expo): View our open source platform and contribute.
- [Discord community](https://chat.expo.dev): Chat with Expo users and ask questions.


# Wordle (Expo) — Proyecto

Versión local del juego Wordle creada con Expo + React Native. Incluye listas de palabras, modo para juegos combinatorios y soporte básico con Firebase para almacenamiento. Pensado para ejecución multiplataforma (iOS / Android / Web) mediante Expo.

## Características
- Juego Wordle en español e inglés.
- Listas de palabras amplias: [`allWords`](wordle/utils/allWords.ts) y [`words`](wordle/utils/targetWords.ts).
- Interfaz basada en Expo + React Native con layout global: [app/_layout.tsx](app/_layout.tsx) y pantalla principal: [app/index.tsx](app/index.tsx).
- Modal de suscripción: [`SubscribeModal`](wordle/components/SubscribeModal.tsx).
- Persistencia/servicios: configuración Firebase en [`FIREBASE_DB`](wordle/utils/FirebaseCongig.ts).
- Script de utilidad para reiniciar el proyecto: [app-example/scripts/reset-project.js](app-example/scripts/reset-project.js).

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
