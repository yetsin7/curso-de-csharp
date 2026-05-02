# Curso de C# — De cero a una base moderna y ejecutable en .NET

Repositorio oficial: [https://github.com/yetsin7/Curso-de-C-sharp](https://github.com/yetsin7/Curso-de-C-sharp)

## Documentacion de referencia

Consulta [Documentación-C-sharp.md](./Documentación-C-sharp.md) para estudiar
con la referencia oficial de Microsoft y una ruta recomendada por temas.

## Para que sirve este curso

Este curso esta pensado para aprender C# como lenguaje y como puerta de entrada
al ecosistema .NET. La meta no es solo entender sintaxis, sino ejecutar codigo,
resolver problemas reales y avanzar desde consola hasta acceso a datos.

## Como esta organizado cada capitulo

Cada carpeta principal del curso incluye ahora una estructura mas util para estudiar:

- `README.md` con explicacion del tema;
- `Program.cs` con ejemplo ejecutable;
- `*.csproj` para correr el capitulo como proyecto real de .NET;
- `02_practica-guiada.md` con ejercicios concretos para probar y modificar.

## Modulos del curso

1. `01-introduccion`
2. `02-variables-y-tipos`
3. `03-operadores`
4. `04-control-de-flujo`
5. `05-funciones-y-metodos`
6. `06-poo-clases`
7. `07-herencia-y-polimorfismo`
8. `08-interfaces-y-abstracciones`
9. `09-colecciones-y-linq`
10. `10-manejo-de-errores`
11. `11-archivos-e-io`
12. `12-async-y-tasks`
13. `13-proyecto-biblia`

## Como ejecutar cualquier tema

```bash
cd 01-introduccion
dotnet run
```

Tambien puedes compilar antes si quieres validar errores:

```bash
dotnet build
```

## Resultado esperado

Al terminar deberias poder:

- entender la sintaxis base de C#;
- modelar datos con clases e interfaces;
- trabajar con colecciones y LINQ;
- manejar errores y archivos;
- usar async/await;
- consultar una base de datos SQLite desde .NET.

## Base de datos del proyecto final

El capitulo `13-proyecto-biblia` usa la base SQLite ubicada en:

```bash
datos/biblia_rv60.sqlite3
```

El proyecto ya incluye la dependencia `Microsoft.Data.Sqlite` en su archivo `.csproj`.

## Recomendacion para respaldo y trabajo colaborativo

Se recomienda subir los cambios del proyecto a GitHub y trabajar mediante Pull Request (PR).
GitHub permite guardar el codigo, mantener historial de cambios y conservar una copia segura en la nube.
Un Pull Request ayuda a revisar cambios antes de integrarlos, reduce errores y deja registro claro de lo modificado.

## Que estudiar despues

Si quieres seguir una ruta util despues de C#, lo mas recomendable es continuar con:

1. SQL: <https://github.com/yetsin7/Curso-de-SQL>
2. Git y GitHub: <https://github.com/yetsin7/Curso-de-GitHub>
3. HTML, CSS y JavaScript si quieres entrar luego a web full stack
