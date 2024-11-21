
# Planificador de eventos

Sitio web que es una extensión de la página www.swingtiago.com, la cuál permite a los administradores agendar eventos en una fecha determinada, detallando lugar, hora, fecha, precio y cupos. Y en donde un usuario no administrador puede interactuar con un calendario para revisar detalles y registrarse a dicho evento.

Los administradores pueden:
- Crear cuenta.
- Iniciar y cerrar sesión.
- Editar detalles de su perfil.
- Crear un evento.
- Eliminar un evento. 
- Añadir tareas a un evento visibles solo para el equipo de producción.

Los usuarios pueden: 
- Revisar en la página principal el calendario, el carrusel y la sección de próximo evento para entrar a estos enlaces.
- Registarse a un evento y recibir un código que identifique su registro.

## Tecnologías

**Client:** React, TailwindCSS, Tabler, Google, Yup, Zustand, Shadcn

**Server:** Node, Express, Mongodb, Celebrate, Dayjs, Multer

## Usos de herramientas en Frontend

- Componentes de biblioteca Shadcn.
- Iconos de librería Tabler
- Mapa de Google.
- Validador Yup.
- Almacen de contexto Zustand. 
- Diseño por medio de Tailwind.

## Usos de herramientas en Backend

- Express como base de maquetación.
- Bcrypt para hash de token. 
- Validador Celebrate.
- Normativa Cors para seguridad.
- Dayjs para gestionar fechas.
- Base de datos Mongoose.
- Multer para guardar archivo. 

## Shadcn

- AlertDialog
- Dialog
- Table
- Button
- Calendar
- Carousel
- Sheet
- Form
- Input
- Label

## Dominios

 - [Frontend](planificador-eventos-frontend.vercel.app)
 - [Backend](https://github.com/matiassingers/awesome-readme)

## API 

#### register

```http
  POST /signup
```

| Parameter  | Type      |
| :--------  | :-------  |
| `name`     | `string`  |
| `email`    | `string`  | 
| `password` | `string`  | 

#### authorize

```http
  POST /signin
```

| Parameter  | Type      |
| :--------  | :-------  |
| `email`    | `string`  | 
| `password` | `string`  | 

#### getUser
```http
  GET /users/me
```

| Parameter  | Type      |
| :--------  | :-------  |
| `token`    | `string`  | 


#### updateUserInfo
```http
  PATCH /users/me
```

| Parameter  | Type      |
| :--------  | :-------  |
| `name`     | `string`  |
| `email`    | `string`  | 

#### getAllEvents
```http
  GET /events
```

#### getEventsByDate
```http
  GET /events/${encodeURIComponent(date)}
```

| Parameter  | Type      |
| :--------  | :-------  |
| `date`    | `string`  | 

#### getEventsById
```http
  GET /events/date/${id}
```

| Parameter  | Type      |
| :--------  | :-------  |
| `id`    | `string`  | 

#### postEventAction
```http
  POST /events
```

| Parameter  | Type      | Description |
| :--------  | :-------  | :-------  |
| `valuesData`    | `object`  | Valores de EventAction

#### postRegisterToEvent
```http
  PATCH /events/${id}/attendees
```

| Parameter  | Type      | Description |
| :--------  | :-------  | :-------  |
| `id`    | `string`  | 
| `body`    | `object`  | Valores de RegisterForm

#### postTaskToEvent
```http
  PATCH /events/${id}/tasks
```

| Parameter  | Type      | Description |
| :--------  | :-------  | :-------  |
| `id`    | `string`  | 
| `body`    | `object`  | Valores de AddTaskForm

## Autor

- [@aaplv2](https://github.com/aaplv2)







