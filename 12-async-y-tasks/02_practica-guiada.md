# Practica guiada — Async y Tasks

## Objetivo

Entender concurrencia basica y operaciones no bloqueantes.

## Actividades

1. Crea un metodo `async` que espere un segundo y luego responda.
2. Ejecuta dos tareas en paralelo con `Task.WhenAll`.
3. Usa `Task.WhenAny` para detectar la primera en terminar.
4. Prueba un `CancellationTokenSource`.
5. Haz una peticion HTTP y captura errores de red.

## Mini reto

Simula una app que consulta clima, noticias y una API externa al mismo tiempo, y luego muestra un resumen en consola.

## Como validar

```bash
cd 12-async-y-tasks
dotnet run
```
