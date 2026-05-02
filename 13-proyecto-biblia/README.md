# Capítulo 13 — Proyecto Biblia (SQLite)

## Descripción

Este proyecto integra todo lo aprendido en el libro para crear una aplicación de consola que consulta la base de datos SQLite de la Biblia Reina-Valera 1960.

---

## Requisitos

### 1. Base de datos

La base de datos debe estar en:

```bash
datos/biblia_rv60.sqlite3
```

El programa busca la ruta correcta automaticamente al ejecutar `dotnet run`.

### 2. Paquete NuGet

El driver `Microsoft.Data.Sqlite` ya esta incluido en `13-proyecto-biblia.csproj`.

---

## Estructura de la base de datos

```sql
-- Tabla de libros
CREATE TABLE libro (
    id         INTEGER PRIMARY KEY,
    nombre     TEXT NOT NULL,
    abrev      TEXT NOT NULL,
    testamento TEXT          -- 'AT' (Antiguo) o 'NT' (Nuevo Testamento)
);

-- Tabla de versículos
CREATE TABLE versiculo (
    id       INTEGER PRIMARY KEY,
    libro_id INTEGER NOT NULL,
    capitulo INTEGER NOT NULL,
    numero   INTEGER NOT NULL,
    texto    TEXT    NOT NULL,
    FOREIGN KEY (libro_id) REFERENCES libro(id)
);
```

---

## Funcionalidades del programa

El programa `Program.cs` demuestra las siguientes consultas:

| # | Consulta                                          |
|---|---------------------------------------------------|
| 1 | Listar los primeros 10 libros de la Biblia        |
| 2 | Buscar el versículo Juan 3:16                     |
| 3 | Contar versículos por libro (top 10)              |
| 4 | Buscar versículos que contienen una palabra clave |
| 5 | Estadísticas generales de la base de datos        |

---

## Ejecutar

```bash
cd 13-proyecto-biblia

# Ejecutar
dotnet run
```

---

## Notas técnicas

- Se usa `using var conexión = ...` para garantizar el cierre de la conexión
- Los parámetros de consulta usan `@param` para prevenir SQL injection
- La ruta de la BD se resuelve automaticamente desde el proyecto
- Si la BD no existe, el programa muestra un mensaje de error claro

---

## Ejemplo de conexión

```csharp
using Microsoft.Data.Sqlite;

string rutaBD = Path.GetFullPath(Path.Combine(Environment.CurrentDirectory, "..", "datos", "biblia_rv60.sqlite3"));

if (!File.Exists(rutaBD))
{
    Console.WriteLine($"Base de datos no encontrada: {rutaBD}");
    return;
}

using var conexion = new SqliteConnection($"Data Source={rutaBD}");
conexion.Open();
Console.WriteLine("Conexión exitosa.");
```
