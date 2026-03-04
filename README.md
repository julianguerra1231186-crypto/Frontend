![](https://github.com/julianguerra1231186-crypto/Frontend/blob/main/frontend/25.png).png)
# Frontend - PulpApp

## Descripción

El **frontend de PulpApp** es la interfaz web que permite a los usuarios visualizar el catálogo de pulpas naturales, agregar productos al carrito de compras y realizar pedidos a través de WhatsApp.

La aplicación está diseñada como un **MVP (Minimum Viable Product)** que permite demostrar la interacción entre el cliente, el catálogo de productos y el sistema de pedidos.

Este frontend consume la API del microservicio **ms-users**, el cual gestiona la información de los usuarios.

---

# Funcionalidades

El frontend incluye las siguientes funcionalidades principales:

* Visualización del catálogo de pulpas naturales
* Buscador de productos
* Carrito de compras dinámico
* Conteo de productos agregados
* Visualización ampliada de productos
* Confirmación de pedido por WhatsApp
* Persistencia del carrito utilizando LocalStorage
* Integración con el microservicio de usuarios

---

# Tecnologías utilizadas

El frontend fue desarrollado utilizando tecnologías web básicas para garantizar simplicidad y facilidad de despliegue.

* HTML5
* CSS3
* JavaScript
* Fetch API
* LocalStorage
* Servidor HTTP local

---

# Estructura del frontend

```id="zt6mnp"
frontend
│
├── index.html
├── app.js
├── style.css
│
└── img
    ├── fresa.png
    ├── mora.png
    ├── maracuya.png
    ├── lulo.png
    ├── coco.png
    └── durazno.png
```

---

# Catálogo de productos

El catálogo muestra diferentes pulpas naturales disponibles para compra:

* Pulpa de Fresa
* Pulpa de Mora
* Pulpa de Maracuyá
* Pulpa de Lulo
* Pulpa de Coco
* Pulpa de Durazno

Cada producto incluye:

* Imagen
* Nombre
* Precio
* Botón para agregar al carrito

---

# Funcionamiento del carrito

El carrito permite:

* Agregar productos
* Aumentar o disminuir cantidades
* Eliminar productos
* Calcular el total del pedido
* Guardar el carrito en LocalStorage

Esto permite que el carrito se mantenga incluso si el usuario recarga la página.

---

# Confirmación del pedido

Cuando el usuario confirma el pedido:

1. El sistema genera un resumen del pedido.
2. Se incluye la dirección de entrega.
3. Se abre automáticamente una conversación en WhatsApp con el pedido.

Ejemplo del mensaje generado:

```id="dzt4pa"
Pedido PulpApp:

Pulpa de Fresa x2
Pulpa de Mora x1

Total: $18500

Dirección: Calle 10 #15-25
```

---

# Integración con backend

El frontend consume la API del microservicio **ms-users** para la gestión de usuarios.

Endpoint utilizado:

```id="n51csx"
http://localhost:8081/users
```

Esto permite registrar y consultar usuarios desde la interfaz web.

---

# Ejecución del frontend

Para ejecutar el frontend se utiliza un servidor HTTP simple.

Desde la carpeta del frontend ejecutar:

```id="2e2qgq"
python -m http.server 5500
```

Luego abrir en el navegador:

```id="7nmb21"
http://localhost:5500
```

---

# Flujo de uso

El flujo básico de uso del sistema es:

1. El usuario ingresa al catálogo de productos.
2. Selecciona las pulpas que desea comprar.
3. Agrega los productos al carrito.
4. Ingresa su dirección de entrega.
5. Confirma el pedido.
6. El pedido se envía por WhatsApp.

---

# Autor

Proyecto desarrollado como parte de la asignatura **Sistemas Distribuidos**.

Autor:

Julian Guerra
