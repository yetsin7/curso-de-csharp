# Practica guiada — Interfaces y abstracciones

## Objetivo

Diseñar contratos reutilizables y reducir acoplamiento.

## Actividades

1. Define una interfaz `INotificador` con un metodo `Enviar`.
2. Implementa `EmailNotificador` y `SmsNotificador`.
3. Crea una clase que reciba `INotificador` por parametro.
4. Compara el uso de interfaz frente a clase abstracta.
5. Agrega una implementacion falsa para pruebas.

## Mini reto

Construye un flujo de pedidos donde el sistema pueda cambiar el canal de notificacion sin tocar la logica principal.

## Como validar

```bash
cd 08-interfaces-y-abstracciones
dotnet run
```
