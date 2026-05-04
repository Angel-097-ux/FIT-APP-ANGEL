# FIT21 — App de entrenamiento 21 días 💪

App PWA instalable. Dark mode, registro de sets/pesos, timer de descanso, logros y progreso.

## Cómo instalar en el celular

### iOS (iPhone/iPad)
1. Abrí el archivo `index.html` en Safari
2. Tocá el botón de compartir (cuadrado con flecha ↑)
3. Seleccioná "Agregar a pantalla de inicio"
4. Tocá "Agregar"
→ La app aparece en tu pantalla como cualquier app nativa.

### Android (Chrome)
1. Abrí el archivo `index.html` en Chrome
2. Tocá los 3 puntos (menú) arriba a la derecha
3. Seleccioná "Instalar aplicación" o "Agregar a pantalla de inicio"
→ La app queda instalada y funciona offline.

## Cómo servir localmente (PC → celular)
```bash
# Instalar servidor simple
npm install -g serve

# Servir la carpeta
serve fitapp21/

# En el celular, abrí la IP que aparece (ej: http://192.168.1.x:3000)
# Luego instalá desde el navegador del celular
```

## Funciones incluidas
- Plan completo 21 días (Semana 1: Base, Semana 2: Potencia, Semana 3: Intensidad)
- Registro de sets, reps y peso por ejercicio
- Timer de sesión con anillo animado
- Timer de descanso automático entre series
- Sistema de logros (8 achievements)
- Historial de entrenamientos
- Gráfico de volumen por semana
- Progreso guardado localmente (localStorage)
- Funciona 100% offline después de la primera carga

## Migrar a Expo (React Native nativo)
Si querés el .apk o subirlo al App Store:
1. `npx create-expo-app FIT21`
2. Usá el mismo plan de datos (PLAN array) en el código JS
3. Reemplazá localStorage por `AsyncStorage` de @react-native-async-storage/async-storage
4. La lógica de negocio es idéntica
5. `npx expo build:android` para generar el APK

## Stack técnico
- HTML5 + CSS3 + JS vanilla (sin dependencias)
- PWA con Service Worker (offline support)
- localStorage para persistencia de datos
- Font: Barlow Condensed (Google Fonts)
