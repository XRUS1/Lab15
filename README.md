# Lab 15 — Interacción Híbrida en WebXR

## Descripción
Aplicación WebXR que combina dos modos de interacción según el contexto del usuario.

## Modos de uso

### 1. Modo Desktop (antes de presionar el botón AR)
- **TransformControls**: toca y arrastra los ejes de colores para mover el trofeo en X, Y o Z.
- **OrbitControls**: arrastra con dos dedos para rotar la cámara alrededor de la escena.

### 2. Modo AR (después de presionar el botón "Start AR")
- **Drag con controlador**: apunta al trofeo con el rayo del controlador (o toca la pantalla en móvil), presiona para agarrar, mueve y suelta.
- **Oclusión por profundidad**: el trofeo se oculta parcialmente cuando hay objetos reales (mesa, silla, mano) entre la cámara y el modelo.
- **Orientación fija**: la base del trofeo siempre mira hacia abajo, sin importar cómo se mueva.

## Estructura del modelo
- **Cubo padre** (invisible): recibe el raycasting y el drag.
- **Trofeo GLB** (hijo): animado con rotación continua y levitación.

## Tecnologías
- three.js (WebXR, TransformControls, GLTFLoader)
- WebXR Device API
- Depth Sensing (cuando el dispositivo lo soporta)

## Instrucciones
1. Abre la página en Chrome de tu celular.
2. Antes del botón: usa los ejes de colores para mover el trofeo.
3. Presiona **"Start AR"**.
4. Apunta al trofeo y toca para agarrarlo.
5. Pon tu mano entre la cámara y el trofeo para ver la oclusión.
