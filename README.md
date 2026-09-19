# Seatly

Aplicación full stack para explorar películas, sesiones, butacas y reservas.

Actualmente el frontend está desarrollado con **Angular** dentro de un **workspace Nx**.

## Empezar

Instalar dependencias:

```bash
npm install
```

Arrancar el frontend:

```bash
npx nx serve Seatly
```

Abrir:

```text
http://localhost:4200
```

## Nx

Nx organiza las distintas aplicaciones del proyecto dentro del mismo repositorio.

Actualmente:

```text
Seatly
└── apps/
    └── Seatly/    → Angular
```

Más adelante tendremos, por ejemplo:

```text
apps/
├── web/           → Angular
└── api/           → NestJS
```

### Comandos útiles

Ver los proyectos del workspace:

```bash
npx nx show projects
```

Ver la configuración y tareas disponibles del frontend:

```bash
npx nx show project Seatly
```

Arrancar Angular:

```bash
npx nx serve Seatly
```

Compilar:

```bash
npx nx build Seatly
```

Ejecutar tests:

```bash
npx nx test Seatly
```

Ver el grafo del workspace:

```bash
npx nx graph
```

## Angular CLI → Nx

| Antes | Con Nx |
|---|---|
| `ng serve` | `npx nx serve Seatly` |
| `ng build` | `npx nx build Seatly` |
| `ng test` | `npx nx test Seatly` |

## Estructura

```text
Seatly/
├── apps/
│   └── Seatly/
│       ├── public/
│       ├── src/
│       │   ├── app/
│       │   ├── main.ts
│       │   └── styles.scss
│       └── project.json
├── libs/
├── tools/
├── nx.json
├── tsconfig.base.json
└── package.json
```

### Recursos estáticos

Imágenes, logos, fondos e iconos:

```text
apps/Seatly/public/
```

Por ejemplo:

```text
apps/Seatly/public/images/
apps/Seatly/public/icons/
```

### Estilos

Estilos globales:

```text
apps/Seatly/src/styles.scss
```

Los estilos específicos de cada componente se mantienen junto al propio componente.