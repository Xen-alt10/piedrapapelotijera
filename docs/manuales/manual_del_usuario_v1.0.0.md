# 📕 GUÍA DE USUARIO Y OPERACIÓN DEL SISTEMA

**Proyecto:** Mini Juego "Piedra, Papel o Tijera" con Persistencia en Disco

**Institución:** E.E.S.T. N°1 — Vicente López

**Asignatura:** Laboratorio de Programación (LPR) — 5° Año

**Docente:** Mansilla Muñoz York Elías 

**Autor / Grupo:** Alexander Veit / GAMY

**Versión:** v1.0.0 | **Fecha:** 23 de octubre de 2026

---

## 💻 1. REQUISITOS MÍNIMOS DEL SISTEMA

- **Sistema Operativo:** Windows 10 / Windows 11 (64-bit) o GNU/Linux.
- **Consola:** Windows PowerShell, Terminal de VS Code o Símbolo del Sistema (CMD).
- **Memoria RAM:** 512 MB libres.
- **Almacenamiento Secundario:** 10 MB de espacio libre en disco.

---

## 🚀 2. PASO A PASO PARA EJECUTAR Y OPERAR EL JUEGO

### Paso 1: Apertura de la Terminal

Abra la carpeta del proyecto `juegopiedra` en VS Code o abra una ventana de PowerShell en la dirección física del proyecto.

### Paso 2: Ejecución del Programa

Ingrese el comando de ejecución y presione Enter:

```powershell
.\src\repasogeneral.exe
```

## Paso 3: Interacción con el Menú Principal 
```
=====================================================
LPR 2026 - ACTIVIDAD 7: PIEDRA, PAPEL O TIJERA
Resolucion de Catedra - Modelo de Replicacion
Estudiante / Grupo: Carl Menger
=====================================================

--- MENU PRINCIPAL DE JUEGO Y PERSISTENCIA ---
1. Jugar (Piedra, Papel o Tijera)
2. Ver Partidas Guardadas en el Historial del Disco (.txt)
3. Salir del Sistema
Ingresa una opcion (1-3):   
```

## Paso 4: Jugar (Opción 1)

- Ingrese 1 y presione Enter.
- Escriba su nombre o apodo (ej. Cazador01).
- Seleccione su jugada (1. Piedra, 2. Papel, 3. Tijera).
- El sistema generará la jugada de la IA, mostrará el resultado en pantalla y confirmará la escritura física en disco:
```
[DISCO] Partida resguardada con exito en 'historial_partidas.txt'.
```
## Paso 5: Consultar el Historial (Opción 2)

Seleccione la Opción 2 para recuperar y visualizar todas las partidas anteriores guardadas en el archivo historial_partidas.txt.

## 3. PREGUNTAS FRECUENTES Y SOLUCIÓN DE PROBLEMAS (FAQ)
   
1. ¿Por qué se saltea la pregunta del Nombre del Jugador?
Causa: Falta de limpieza en el búfer de entrada.
Solución: Verifique que la función jugarPartida() contenga la llamada cin.ignore() antes de ejecutar getline(cin, p.jugador).

2. ¿Dónde se guardan mis partidas?
Los datos se almacenan automáticamente en el archivo plano src/historial_partidas.txt en formato separado por comas (CSV).









