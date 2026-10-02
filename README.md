# NodoTech CR

Marketplace de tecnología donde varias tiendas pequeñas y medianas de Costa Rica publican y venden sus productos en un mismo sitio. Los clientes pueden buscar, filtrar, ver la ficha técnica de cada producto y comprar con pago simulado.

Proyecto final del curso **SC-403 Desarrollo de Aplicaciones Web y Patrones**, Universidad Fidélitas, III cuatrimestre 2026.

## Estado del proyecto

| Entrega | Semana | Estado |

| Avance 1: historias de usuario y prototipo | 5 | En progreso |
| Avance 2: 50 % del proyecto funcionando | 9 | Pendiente |
| Entrega final, artículo y defensa | 15 | Pendiente |

## Integrantes

| Integrante | Usuario de GitHub | Módulo a cargo |

| María Natalia Otárola Rodríguez | @natior99-rgb | Catálogo público, plantilla general e idioma |
| Axel Alberto Corrales Montero | @pendiente | Cuentas, seguridad y administración |
| Sofía Herra Jiménez | @pendiente | Panel de tienda aliada: productos, ficha técnica, departamentos y marcas |
| Kendrick (apellidos) | @pendiente | Carrito, compra y pedidos |

## Roles del sistema

| Rol | Qué puede hacer |

| Visitante (sin sesión) | Ver el catálogo, buscar, filtrar, ver el detalle de los productos, armar el carrito y cambiar el idioma |
| CLIENTE | Lo mismo que el visitante, más confirmar compras y ver sus pedidos |
| TIENDA_ALIADA | Registrar, editar y desactivar sus productos con su ficha técnica y ver sus ventas |
| ADMINISTRADOR | Aprobar o rechazar tiendas, mantener departamentos y marcas y cambiar el estado de los pedidos |

## Funcionalidades principales

- Catálogo de productos de varias tiendas, organizado por departamentos.
- Búsqueda por nombre o marca y filtros por marca y rango de precio.
- Detalle del producto con ficha técnica (procesador, RAM, almacenamiento, etc.).
- Carrito de compras y confirmación de compra con pago simulado (SINPE Móvil o tarjeta).
- Seguimiento del estado del pedido: Pendiente, Enviado, Entregado o Cancelado.
- Registro de clientes con correo de bienvenida.
- Solicitud y aprobación de tiendas aliadas.
- Sitio en español e inglés.

## Tecnologías

- Java y Spring Boot
- Thymeleaf (plantillas, fragmentos e internacionalización)
- Bootstrap por webjars
- Hibernate/JPA con MySQL
- Spring Security para el inicio de sesión y los roles
- Firebase Storage para las imágenes de los productos
- Spring Mail para los correos
- OpenPDF para el comprobante del pedido (investigación adicional, entrega final)

## Base de datos

La base `nodotech` tiene 10 tablas: `usuario`, `rol`, `usuario_rol`, `tienda_aliada`, `departamento`, `marca`, `producto`, `especificacion`, `pedido` y `detalle_pedido`. Las tablas `pedido` y `detalle_pedido` registran las transacciones del sistema.

## Estructura del proyecto
De como va hacer el proyecto final
```
src/main/java/com/nodotech/
├── controller/
├── domain/
├── repository/
└── service/
src/main/resources/
├── templates/
├── static/
├── messages*.properties
└── nodotech.sql
```

## Cómo ejecutarlo (preliminar)

1. Clonar el repositorio desde NetBeans: Team → Git → Clone.
2. Ejecutar `src/main/resources/nodotech.sql` en MySQL Workbench para crear la base `nodotech` con datos de prueba.
3. Revisar la conexión a la base de datos en `application.properties`.
4. Correr el proyecto y abrir http://localhost.

Los usuarios de prueba por rol se agregan cuando esté lista la seguridad.

## Cómo trabajamos en el repositorio

- La rama `master` siempre debe funcionar y está protegida: los cambios entran solo por pull request aprobado por otra persona del equipo.
- Cada historia se trabaja en su propia rama, creada desde `master` actualizado. Ejemplos: docs/readme-avance1.
- Antes de crear una rama se hace **Pull** de `master` para tener la última versión.
- Los commits son cortos y dicen qué se hizo, por ejemplo: `Agrega CRUD de marcas`.
- En cada commit, el Author y el Committer llevan el correo de la cuenta de GitHub de cada integrante, para que el aporte quede registrado a su nombre.
- El título del pull request lleva el ID de la historia, por ejemplo `HU-14 · Registrar productos`.
- Rotación de revisión: Natalia revisa a Axel, Axel a Sofía, Sofía a Kendrick y Kendrick a Natalia.
- Los pull requests se unen con *Create a merge commit* para conservar el historial de cada integrante.
- No se suben contraseñas reales, tokens ni el archivo de credenciales de Firebase.

## Enlaces

- Prototipo en Figma: (pendiente)
- Tablero del backlog: pestaña **Projects** de este repositorio
