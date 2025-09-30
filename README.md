<a href="https://deepwiki.com/RMJGLUCKY27/MY-proyects">
  <img src="https://deepwiki.com/badge.svg" alt="Ask DeepWiki">
</a>

<h1>☕ Coffee Shop Web Application</h1>

<p>
  Una aplicación web cliente para una cafetería, que permite a los usuarios 
  explorar productos de café, gestionar un carrito de compras y mantener persistencia 
  con <code>localStorage</code>. 
</p>

<hr>

<h2>📂 Archivos Relevantes</h2>
<ul>
  <li><b>index.html</b> (1–306)</li>
  <li><b>app.js</b> (1–129)</li>
  <li><b>custom.css</b> (1–204)</li>
</ul>

<hr>

<h2>🎯 Propósito y Alcance</h2>
<p>
  Este documento ofrece una visión general de la aplicación, incluyendo diseño 
  arquitectónico, componentes principales y patrones de flujo de datos.  
  Para más detalle, consultar: 
  <i>Arquitectura de la Aplicación Frontend, Framework de Estilos y Biblioteca de Recursos Visuales</i>.
</p>

<hr>

<h2>🏗️ Arquitectura del Sistema</h2>
<p>
  El sistema sigue un patrón <b>client-side architecture</b> con tres capas principales:
</p>
<ol>
  <li><b>Presentación</b></li>
  <li><b>Lógica</b></li>
  <li><b>Persistencia</b></li>
</ol>
<p>
  Toda la lógica corre en el navegador, sin necesidad de procesamiento en el servidor.
</p>

<hr>

<h2>🧩 Componentes Principales</h2>
<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th>Componente</th>
      <th>Archivo</th>
      <th>Funciones Clave</th>
      <th>Propósito</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Interfaz de Usuario</td>
      <td>index.html</td>
      <td>Catálogo de productos, navegación, carrito</td>
      <td>Presentación e interacción con el usuario</td>
    </tr>
    <tr>
      <td>Gestión del Carrito</td>
      <td>app.js</td>
      <td><code>comprarCafe()</code>, <code>eliminarCafe()</code>, <code>vaciarCarrito()</code></td>
      <td>Lógica de negocio del carrito</td>
    </tr>
    <tr>
      <td>Diseño Visual</td>
      <td>custom.css</td>
      <td>.card, .submenu, #hero styling</td>
      <td>Tematización y diseño responsivo</td>
    </tr>
    <tr>
      <td>Persistencia de Datos</td>
      <td>app.js</td>
      <td><code>guardarCafeLocalStorage()</code>, <code>leerLocalStorage()</code></td>
      <td>Gestión de estado y persistencia</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>⚙️ Tecnologías Utilizadas</h2>
<ul>
  <li><b>HTML5</b>: marcado semántico con grid de Skeleton CSS</li>
  <li><b>CSS Framework</b>: normalize.css + skeleton.css + custom.css</li>
  <li><b>JavaScript</b>: ES5 con manipulación del DOM y localStorage</li>
  <li><b>APIs del Navegador</b>: localStorage, DOM Events API</li>
</ul>

<hr>

<h2>🔄 Flujo de Datos y Persistencia</h2>
<p>El sistema implementa un flujo de datos unidireccional con <code>localStorage</code> como capa de persistencia.</p>

<pre><code>// Estructura de datos del carrito (app.js:24-29)
const infoCafe = {
    imagen: cafe.querySelector('img').src,
    titulo: cafe.querySelector('h4').textContent,
    precio: cafe.querySelector('.precio span').textContent,
    id: cafe.querySelector('a').getAttribute('date-id')
}
</code></pre>

<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th>Operación</th>
      <th>Función</th>
      <th>Propósito</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Guardar Item</td>
      <td><code>guardarCafeLocalStorage()</code></td>
      <td>Añadir producto al carrito en localStorage</td>
    </tr>
    <tr>
      <td>Cargar Carrito</td>
      <td><code>leerLocalStorage()</code></td>
      <td>Restaurar el estado del carrito al cargar la página</td>
    </tr>
    <tr>
      <td>Eliminar Item</td>
      <td><code>eliminarCafeLocalStorage()</code></td>
      <td>Eliminar un producto específico</td>
    </tr>
    <tr>
      <td>Vaciar Todo</td>
      <td><code>vaciarLocalStorage()</code></td>
      <td>Vaciar el carrito completo</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>✨ Funcionalidades de la Aplicación</h2>

<h3>📦 Catálogo de Productos</h3>
<ul>
  <li>Diseño en grid con Skeleton CSS</li>
  <li>Información de producto: título, marca, precio, rating</li>
  <li>Imágenes consistentes: coffee1.jpg – coffee5.jpg</li>
</ul>

<h3>🛒 Carrito de Compras</h3>
<ul>
  <li><b>Añadir Productos:</b> <code>comprarCafe()</code></li>
  <li><b>Visualización:</b> dropdown con <code>.submenu:hover #carrito</code></li>
  <li><b>Eliminar Items:</b> <code>eliminarCafe()</code></li>
  <li><b>Persistencia:</b> guardado automático en localStorage</li>
</ul>

<h3>🎨 Elementos de Interfaz</h3>
<ul>
  <li>Sección Hero con banner y buscador</li>
  <li>Navegación con logo y carrito</li>
  <li>Diseño responsive (breakpoints en 550px y 750px)</li>
</ul>

<hr>

<footer>
  <p>📖 Documentación generada para <b>Coffee Shop Web Application</b> | 
  <a href="https://deepwiki.com/RMJGLUCKY27/MY-proyects">Ver más proyectos</a></p>
</footer>
