# TodoExpressEjer4
---

Esta app esta hecha con Express y Test con jest.
Contiene frontend en la carpeta public (index.html)
Ejecuta el proyecto usando public/index.html como pagina inicial en port 3000
La app pide a un usuario que: crie una tarea, actualice una tarea con nuevos datos o delete una tarea.
tambien tiene la opcion de ver la basedatos para comprobar que se an cuardado los cambios correctamente.

---

# URL END POINT
---

`exp.use('/api/todos', router)`

---

# URL GET ALL TASKS
---

`exp.use('/api/todos/allTasks', router)`

`router.get('/alltasks', (_req, res) => {
    res.status(200).send(app.getAllTasks())
})`

---

# URL GET ALL TASKS
---

`exp.use('/api/todos/', router)`

`router.get('/', (_req, res) => {
    res.status(200).send(app.getAllTasks())
})`

---




# Ejemplo básico de TS

---

En este ejemplo básico hay:

- ESLint
- Prettier
- ts-jest
- nodemon
- VSCode Debugging
- Github Actions
- Pequeño ejemplo de código funcional con import

La configuración del debugger apunta a src/index.ts como archivo de inicio del proyecto.

Comandos:

Testing:

```sh
npm run test
```

Ejecuta los tests ignorando los que existan en dist/

Prettier format:

```sh
npm run prettier-format
```

Ejecuta manualmente el prettier en el proyecto, recomiendo instalar la extensión prettier y que se autoejecute al guardar.

Watcher:

```sh
npm run dev:watcher
```

Ejecuta nodemon usando src/index.ts como archivo inicial

Dev Run:

```sh
npm run dev
```

Ejecuta el proyecto usando public/index.html como pagina inicial en port 3000

```sh
npm run dev:run
```

Ejecuta el proyecto sin watcher

Build:

```sh
npm run dist
```

Transpila el proyecto en dist/

---

## Debugger

en el archivo .vscode/launch.json está la configuración del debugger.

```json
{
  // Use IntelliSense to learn about possible attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Lanza debug",
      "preLaunchTask": "tsc: build - tsconfig.json",
      "skipFiles": ["<node_internals>/**"],
      "program": "${workspaceFolder}/src/index.ts",
      "outFiles": ["${workspaceFolder}/dist/**/*.js"]
    }
  ]
}
```
