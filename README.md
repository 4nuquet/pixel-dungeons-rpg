# Pixel Dungeons RPG

Proyecto de juego de mazmorras en estilo pixel art desarrollado con C# y MonoGame, con una base de motor propio para facilitar la evolución del juego hacia un sistema más completo.

## Estado actual

El repositorio contiene una base funcional inicial del juego:
- una ventana principal del juego configurada en MonoGame,
- un motor base llamado `PixelEngine`,
- una clase `PixelDungeonsGame` que hereda de `EngineGame`,
- soporte para MonoGame Content Builder (`mgcb`) ya configurado,
- estructura inicial lista para continuar con lógica de juego, entidades y contenido visual.

Actualmente el proyecto se encuentra en una etapa de prototipo inicial, con la infraestructura base creada y varios puntos marcados con `TODO` para continuar el desarrollo del sistema de juego.

## Tecnologías

- C#
- .NET 9
- MonoGame 3.8
- Visual Studio / VS Code
- .NET CLI

## Estructura del proyecto

```text
pixel-dungeons-rpg/
├── README.md
├── CHANGELOG.md
├── .gitignore
└── PixelDungeons/
    ├── PixelDungeons.slnx
    ├── PixelDungeons/
    │   ├── .config/
    │   │   └── dotnet-tools.json
    │   ├── Content/
    │   │   └── Content.mgcb
    │   ├── app.manifest
    │   ├── Icon.ico
    │   ├── Icon.bmp
    │   ├── PixelDungeons.csproj
    │   ├── PixelDungeonsGame.cs
    │   └── Program.cs
    └── PixelEngine/
        ├── PixelEngine.cs
        └── PixelEngine.csproj
```

## Componentes principales

### PixelDungeonsGame
La clase principal del juego crea una ventana con título, resolución y configuración base del motor. En este momento incluye:
- inicialización del juego,
- control de salida con `Esc` y `Back`,
- fondo de color magenta por defecto,
- placeholders para lógica del juego y renderizado.

### PixelEngine
La clase `EngineGame` actúa como base para la arquitectura del juego y encapsula:
- creación del `GraphicsDeviceManager`,
- configuración de la ventana,
- acceso global a `GraphicsDevice`, `SpriteBatch` y `Content`,
- inicialización del entorno MonoGame.

## Requisitos

- .NET SDK 9.0
- Visual Studio 2022 o VS Code con C# Dev Kit
- Soporte de MonoGame DesktopGL

## Cómo ejecutar

Desde la raíz del repositorio, puedes arrancar el proyecto con:

```bash
dotnet restore PixelDungeons/PixelDungeons.slnx
dotnet run --project PixelDungeons/PixelDungeons/PixelDungeons.csproj
```

Si prefieres trabajar desde Visual Studio, abre la solución `PixelDungeons.slnx` y ejecuta el proyecto `PixelDungeons`.

## Roadmap inicial

- [ ] Crear sistema de entrada de jugador
- [ ] Añadir tiles y generación de mapas
- [ ] Implementar movimiento y cámara
- [ ] Añadir entidades enemigas
- [ ] Diseñar sistema de combate
- [ ] Crear inventario y objetos
- [ ] Añadir música, efectos y UI
- [ ] Preparar fase de pruebas y balance

## Notas

Este proyecto está pensado como una base para un RPG de mazmorras en estilo pixel art, con posibilidad de crecer hacia una estructura más robusta de entidades, niveles, NPCs, combate y progresión.
