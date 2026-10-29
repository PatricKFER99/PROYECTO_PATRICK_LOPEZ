*Sistema Web de Inventario, Catálogo y Ventas (Plug & Play Open Source)*

Una plantilla web de código abierto (Open Source) diseñada para transformar cualquier negocio local (cafeterías, ferreterías, bodegas, tiendas de abarrotes o ropa) en un e-commerce moderno con panel de administración, control de inventario en tiempo real y personalización visual instantánea.

*_Desarrollado con HTML puro, CSS, JavaScript (Vanilla ES6), almacenamiento en la nube y Supabase como backend relacional._*

Características Principales

Ecosistema Plug & Play: Cambia el nombre del negocio, la identidad de marca, los colores corporativos y el número de soporte técnico desde un único archivo central (config.js) o mediante un Editor Visual en Vivo (editor.html).

Catálogo Dinámico e Imágenes en la Nube: Gestión de productos por categorías (Cafés, Postres, Jugos/Artículos, Promociones) con carga directa de imágenes al Cloud Storage de Supabase.

Carrito de Compras y Checkout: Cálculo automático de totales, selección de distritos de reparto (zonas de delivery) y múltiples pasarelas de pago simuladas (Yape/Plin, Tarjeta de Crédito/Débito, Efectivo contra entrega).

Módulo de Autenticación y Seguridad CRUD: Registro e inicio de sesión de clientes, validación de comprobantes (Boleta/Factura según RUC) y acceso restringido al panel de inventarios (admin.html) exclusivo para el administrador.

Soporte y Atención al Cliente: Formulario de contacto integrado directamente a la base de datos y botón de asistencia flotante en tiempo real vía WhatsApp.


 Instrucciones de Instalación (En 3 Pasos)

Paso 1: Clonar o Descargar el Proyecto

Haz un "Fork" o descarga este repositorio en tu computadora para usarlo como base de tu propio negocio.

Paso 2: Configurar la Base de Datos en Supabase

El sistema utiliza Supabase (PostgreSQL en la nube) para la persistencia de datos y la gestión de archivos multimedia.

Crea una cuenta gratuita en Supabase y crea un nuevo proyecto.

Dirígete a la sección SQL Editor en el menú de la izquierda.

Copia todo el contenido del archivo setup.sql incluido en este repositorio, pégalo en el editor SQL de Supabase y presiona Run. Esto creará automáticamente las 6 tablas relacionales, las políticas públicas de almacenamiento (fotos) y los datos iniciales de prueba.

Paso 3: Conectar el Sistema

En tu panel de Supabase, ve a Project Settings > API.

Copia tu Project URL y tu llave pública anon public.

Abre el archivo conexion.js de este proyecto e inserta tus credenciales:

const supabaseUrl = 'https://tu-proyecto.supabase.co';
const supabaseKey = 'tu-llave-anon-publica';


 Personalización y Branding

Puedes adaptar el software a tu propio negocio de dos formas:

Configuración Rápida por Código (config.js):
Abre el archivo config.js y modifica las variables globales:

export const config = {
    correoAdmin: "tu-correo@dominio.com",
    whatsappSoporte: "51999999999",
    nombreNegocio: "Tu Negocio S.A.C."
};


Personalización Visual en Vivo (editor.html):
Inicia sesión en la plataforma con el correo del administrador, ingresa al Panel Admin (admin.html) y haz clic en " Personalizar Página Web". Desde allí podrás cambiar la paleta de colores corporativos, subir logotipos, editar textos de portada y cambiar imágenes con un solo clic, o restaurar el diseño original de Sonqo Café instantáneamente.

📄 Licencia

Este proyecto se distribuye bajo la Licencia MIT. Es software 100% libre, gratuito y de código abierto. Puedes copiarlo, modificarlo, adaptarlo y distribuirlo con fines comerciales o personales sin restricciones.

Desarrollado originalmente como proyecto académico de Ingeniería de Software / Diseño Web (IESTP Arturo Sabroso Montoya) orientado al empoderamiento digital de micro y pequeños emprendedores.