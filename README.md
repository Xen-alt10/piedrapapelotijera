🎮 ACTIVIDAD 7: MINI JUEGO "PIEDRA, PAPEL O TIJERA" CON PERSISTENCIA DE DATOS

**Asignatura:** Laboratorio de Programación (LPR) — 5° Año  
**Institución:** E.E.S.T. N°1 — Vicente López  
**Profesor:** Prof. Mansilla Muñoz York  
**Estudiante:** Alexander Veit  
**Grupo:** GAMY  
**Ciclo Lectivo:** 2026

## 🎯 DESCRIPCIÓN DEL PROYECTO

Este repositorio contiene la implementación en C++ del mini juego interactivo Piedra, Papel o Tijera contra una Inteligencia Artificial en consola. El sistema demuestra la diferencia práctica entre la Memoria RAM (volátil) y el Almacenamiento Secundario (persistente) mediante el uso de estructuras de datos (`struct`) y flujos de archivos (`<fstream>`).

## 🚀 FUNCIONALIDADES CLAVE

- **Modelado con `struct`:** Agrupación heterogénea de atributos de partida (`idPartida`, `jugador`, `eleccionJugador`, `eleccionIA`, `resultado`).
- **Persistencia en Disco (`ofstream`):** Registro de jugadas en modo anexado (`ios::app`). El programa guarda el historial intentando primero en `src/historial_partidas.txt` y, si no es posible, en `historial_partidas.txt` de la raíz.
- **Recuperación de Historial (`ifstream`):** Lectura e interpretación de registros persistidos delimitados por comas (CSV) con conteo total de partidas.
- **Generación aleatoria con IA:** Elección aleatoria de la IA con `srand(time(0))`.
- **Menú interactivo por consola:** Jugar, ver historial guardado, salir.

## 🗂️ ESTRUCTURA DEL REPOSITORIO

```text
piedrapapelotijera/
├── .gitignore
├── LICENSE                         <-- Licencia MIT
├── README.md                       <-- Portada técnica del proyecto
├── capturas/                       <-- Evidencias de ejecución
│   ├── archivo_disco.png
│   └── jugada_consola.png
├── docs/                           <-- Entregables formales
│   ├── CHANGELOG.md
│   ├── InformeEEST1_LPR2026_ACT07_G03_AlexanderVeit_Informe_v1.1.0.pdf
│   └── manuales/
│       ├── CHANGELOG.md
│       ├── manual_del_programador_v1.0.0.md
│       ├── manual_del_programador_v1.0.0.pdf
│       ├── manual_del_usuario_v1.0.0.md
│       └── manual_del_usuario_v1.0.0.pdf
└── src/                            <-- Código fuente C++
    ├── historial_partidas.txt      <-- Archivo de almacenamiento en disco
    ├── main.cpp                    <-- Programa principal del juego
    └── main.exe                    <-- Ejecutable (compilado)
```

## 💾 FORMATO DE ALMACENAMIENTO

El historial se guarda en formato CSV con el siguiente orden:
```text
idPartida,jugador,eleccionJugador,eleccionIA,resultado
```

Ejemplo:
```text
1,Alex,Tijera,Piedra,Perdiste!
```

## 🛠️ COMPILACIÓN Y EJECUCIÓN

### Compilar (g++)
Desde la raíz del proyecto:
```bash
g++ -std=c++17 -Wall -o src/main src/main.cpp
```

O desde `src/`:
```bash
cd src
g++ -std=c++17 -Wall -o main main.cpp
```

### Ejecutar
Desde la raíz:
```bash
src/main
```
o
```bash
./src/main.exe  # en Windows
```

## 📄 LICENCIA

Este proyecto se distribuye bajo licencia [MIT](LICENSE).

## 👤 AUTOR

**Alexander Veit** — E.E.S.T. N°1, Vicente López — Laboratorio de Programación (LPR), 5° Año, 2026
