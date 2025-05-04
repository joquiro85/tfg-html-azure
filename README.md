# TFG: Automatización del Despliegue de Infraestructura en Azure con Terraform

Este proyecto es el Trabajo Final de Grado de Jesús Omar Quimbay Rojas para el ciclo de Administración de Sistemas Informáticos en Red (ASIR). Utiliza **Terraform** para automatizar el despliegue de recursos en **Microsoft Azure**, e incluye una sencilla interfaz web estática para documentar tecnologías y recursos.

---

## Estructura del proyecto

```
/ (raíz)
├─ index.html         # Página principal
├─ recursos.html      # Documentación de recursos desplegados en Azure
├─ tecnologias.html   # Listado de tecnologías usadas y enlaces
├─ style.css          # Estilos globales y responsive
└─ Images/            # Iconos y logos utilizados en las páginas
```

---

## index.html

* **Sección superior**: título del TFG y botones de navegación a las páginas de Tecnologías y Recursos.
* **Sección de detalles**: nombre del autor, descripción del ciclo ASIR y logos de Terraform y Azure.
* **Sección inferior**: placeholder para mostrar el ID de la instancia (simulado).
* Enlaza con `style.css` y define un favicon.

---

## recursos.html

Presenta en un grid responsivo (mínimo 280px, auto-ajustable) las tarjetas con los recursos principales desplegados en Azure:

* **Zona DNS**: A record y CNAME para el dominio raíz y `www`.
* **Resource Group**: referencia al grupo `TFG-Infra`.
* **Load Balancer**: estándar que reparte tráfico HTTP/80.
* **Jumpbox VM**: VM Linux en la subred pública para administración.
* **MySQL VM**: instancia con MariaDB en subred privada.
* **Autoscale Setting**: escala instancias según CPU.
* **NAT Gateway**: salida a internet para subred privada.
* **Network Security Groups**: reglas para MySQL, HTTP y SSH.
* **IP Públicas**: IP estática para LB, NAT y jumpbox.
* **Subnets**: pública y privada (asociada al NAT).
* **Virtual Network**: red virtual que engloba las subredes.

---

## tecnologias.html

Muestra un grid de tecnologías empleadas, cada tarjeta enlaza a la web oficial:

* **Terraform** (`https://www.terraform.io`)
* **Microsoft Azure** (`https://portal.azure.com`)
* **GitHub** (`https://github.com`)
* **Visual Studio Code** (`https://code.visualstudio.com`)
* **Nginx** (`https://nginx.org`)

---

## style.css

Define estilos globales y responsive:

* **Reset y base**: margin/padding a 0, `box-sizing: border-box`, fuente Roboto.
* **Flex layout** en contenedor principal y cabecera.
* **Botones** con `clamp()` para tipografía fluida y efectos `hover`.
* **Grid** de tarjetas con `repeat(auto-fit, minmax(280px,1fr))` y `gap: clamp(10px,2vw,20px)`.
* **Hover states** con `transform` y `drop-shadow`.
* **Media queries mínimas** para dispositivos <600px y <768px: logos ajustados, cabecera y textos en columna, botones al 50%.

---

## Uso

1. Clona o descarga el repositorio.
2. Sitúa `index.html`, `recursos.html`, `tecnologias.html`, `style.css` y la carpeta `Images/` en tu servidor (o abre localmente).
3. Abre `index.html` en el navegador para navegar por la documentación.

---

## Contribución y licencias

Este proyecto es de carácter académico. Para sugerencias o mejoras, puedes abrir un issue o pull request en el repositorio de GitHub del autor.
