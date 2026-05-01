# Curso de C# — De cero a PRO

Guía práctica y progresiva para aprender C# moderno (.NET 8+) entendiendo cómo
se comporta una aplicación de consola o de backend dentro del ecosistema .NET.

Repositorio oficial: [https://github.com/yetsin7/Curso-de-C-Sharp](https://github.com/yetsin7/Curso-de-C-Sharp)

---

## 🇳🇮 Para estudiantes de Nicaragua (y de toda Latinoamérica)

Si estás en Nicaragua y quieres aprender a programar, este libro es para ti.

No necesitas pagar un curso caro, no necesitas registrarte en ninguna plataforma,
no necesitas mandar correos ni dar tus datos. Tampoco necesitas tener internet
todo el tiempo: una vez que clonas el repositorio, puedes estudiar completamente
**offline** desde tu computadora.

Este material está pensado para que cualquier persona, sin importar su ciudad,
su edad o su situación económica, pueda formarse como programadora o programador
profesional desde cero. Si eres de León, Managua, Estelí, Matagalpa, Granada,
Bluefields o de cualquier rincón del país, este libro está hecho para ti.

Y si no eres de Nicaragua, también eres bienvenido. El contenido está escrito
en español neutro y funciona igual de bien para estudiantes de cualquier país
de Centroamérica y Latinoamérica.

---

## ¿Por qué existe este libro?

La misión de este proyecto es simple: **que más nicaragüenses puedan aprender
a programar de forma gratuita, sin barreras**.

En Nicaragua muchos estudiantes y autodidactas tienen el talento y las ganas,
pero no siempre tienen acceso a:

- cursos pagados que cuestan cientos de dólares;
- internet rápido o estable las 24 horas;
- libros técnicos en español bien explicados;
- alguien que les guíe paso a paso desde cero.

Este libro busca cerrar esa brecha. Es **100% gratuito**, no requiere registro,
funciona **sin internet** una vez clonado, y está escrito en español claro,
sin tecnicismos innecesarios. No hace falta haber programado antes.

Si este material te sirve, compártelo con otros estudiantes nicaragüenses,
con tu colegio, tu universidad, tu grupo de amigos o cualquier persona que
quiera aprender. Mientras más seamos, más fuerte se hace la comunidad.

---

## ¿Para quién es este libro?

- Personas que quieren aprender a programar desde cero usando C#
- Desarrolladores de otros lenguajes (Java, Python, JS) que quieren migrar a .NET
- Estudiantes que buscan entender C# moderno con ejemplos ejecutables
- Cualquier persona que quiera entender el ecosistema .NET de forma ordenada

## Qué aprenderás

Este libro explica C# como lenguaje y como plataforma:

- sintaxis clara y tipada;
- cómo .NET compila y ejecuta el código;
- cómo se organizan clases, objetos y colecciones;
- cómo se maneja memoria de forma administrada;
- cómo construir programas confiables y mantenibles.

---

## Requisitos previos

Solo necesitas tener instalado el SDK de .NET 8 o superior.

### Instalar .NET SDK

1. Ve a [https://dotnet.microsoft.com/download](https://dotnet.microsoft.com/download)
2. Descarga el **.NET 8 SDK** (o superior) para tu sistema operativo
3. Instálalo siguiendo el asistente
4. Verifica la instalación abriendo una terminal:

```bash
dotnet --version
# Debe mostrar algo como: 8.0.xxx
```

---

## Qué ocurre cuando ejecutas C#

Cuando corres un programa en C#:

- el código se compila a un lenguaje intermedio;
- el runtime de .NET lo carga;
- el recolector de basura administra gran parte de la memoria;
- el programa usa CPU, RAM, disco o red según la lógica que escribiste.

Esto hace que C# sea amigable para aprender y muy potente para software real.

---

## Crear y ejecutar un proyecto

Cada capítulo tiene su propio `Program.cs`. Para ejecutarlo:

```bash
# Crear un nuevo proyecto de consola
dotnet new console -n MiProyecto
cd MiProyecto

# Ejecutar el proyecto
dotnet run

# Compilar sin ejecutar
dotnet build
```

Si quieres ejecutar directamente el `Program.cs` de un capítulo:

```bash
cd 01-introduccion
dotnet run
```

---

## 📚 Tabla de capítulos

| #  | Capítulo                        | Temas principales                                          |
|----|---------------------------------|------------------------------------------------------------|
| 01 | Introducción                    | Qué es C#, .NET, hola mundo, estructura básica             |
| 02 | Variables y tipos               | Tipos primitivos, var, nullable, const, interpolación      |
| 03 | Operadores                      | Aritméticos, lógicos, ternario, null-coalescing            |
| 04 | Control de flujo                | if/else, switch expression, foreach, while, pattern match  |
| 05 | funciones y métodos             | Parámetros, lambdas, Func, Action, métodos de extensión    |
| 06 | POO — Clases                    | Clases, propiedades, constructores, records                |
| 07 | herencia y polimorfismo         | virtual/override, clases abstractas, sealed                |
| 08 | Interfaces y abstracciones      | Interfaces, default methods, comparación con abstractas    |
| 09 | Colecciones y LINQ              | List, Dictionary, HashSet, LINQ completo                   |
| 10 | Manejo de errores               | try/catch/finally, excepciones personalizadas, using       |
| 11 | Archivos e I/O                  | File, Stream, Path, Directory, JSON                        |
| 12 | Async y Tasks                   | async/await, Task<T>, CancellationToken, HttpClient        |
| 13 | Proyecto Biblia                 | SQLite con Microsoft.Data.Sqlite, consultas reales         |

---

## Base de datos de la Biblia

A partir del capítulo 11 se usa opcionalmente, y en el **capítulo 13** se usa directamente la base de datos SQLite de la Biblia ubicada en:

```
../../datos/biblia_rv60.sqlite3
```

Esta base de datos contiene los textos de la Reina-Valera 1960 organizados en tablas de libros, capítulos y versículos.

Para el capítulo 13, necesitas instalar el paquete NuGet:

```bash
dotnet add package Microsoft.Data.Sqlite
```

---

## convenciones del libro

- Todos los comentarios en el código están en **español**
- El código es compatible con **.NET 8+**
- Cada `Program.cs` es autocontenido y ejecutable por separado
- Ningún archivo supera las 200 líneas

---

## Estructura del proyecto

```
Curso de C#/
├── README.md                  ← Este archivo
├── datos/
│   └── README.md              ← Información sobre la BD de la Biblia
├── 01-introduccion/
├── 02-variables-y-tipos/
├── 03-operadores/
├── 04-control-de-flujo/
├── 05-funciones-y-metodos/
├── 06-poo-clases/
├── 07-herencia-y-polimorfismo/
├── 08-interfaces-y-abstracciones/
├── 09-colecciones-y-linq/
├── 10-manejo-de-errores/
├── 11-archivos-e-io/
├── 12-async-y-tasks/
└── 13-proyecto-biblia/
```

---

## ⭐ Cómo apoyar este proyecto

Si este libro te está ayudando a aprender, hay varias formas de apoyar el proyecto.
Todas son gratis y suman muchísimo:

- **Dale una estrella** ⭐ al repositorio en GitHub. Eso ayuda a que más personas
lo encuentren: [github.com/yetsin7/Curso-de-C-Sharp](https://github.com/yetsin7/Curso-de-C-Sharp)
- **Compártelo** con tus amigos, compañeros de clase, profesores o cualquier
  persona en Nicaragua o Latinoamérica que quiera aprender a programar.
- **Abre un issue** si encuentras un error, una explicación confusa o un ejemplo
  que no funciona. Tu reporte mejora el libro para todos.
- **Manda un pull request** si quieres aportar mejoras, correcciones, ejemplos
  nuevos o traducciones. Toda contribución es bienvenida.
- **Estudia y termina el libro.** Tu progreso ya es parte del impacto: cada
  persona que aprende fortalece la comunidad de programadores del país.

---

Hecho con cariño desde Nicaragua para todo el que quiera aprender. 🇳🇮
