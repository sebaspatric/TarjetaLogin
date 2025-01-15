# Registro de Usuario

Este proyecto es una sencilla aplicación web que permite a los usuarios registrarse y visualizar su información en un perfil. Incluye un formulario para capturar datos y una tarjeta de perfil que se actualiza con la información ingresada.

## Tecnologías utilizadas

- **HTML5**: Estructura de la página.
- **CSS3**: Estilizado de la interfaz con Bootstrap y un archivo personalizado `styles.css`.
- **JavaScript**: Lógica para capturar y procesar los datos del formulario.
- **Bootstrap 4.5**: Framework CSS para un diseño responsivo.

## Estructura del proyecto

El proyecto consta de los siguientes archivos:

1. **index.html**: Archivo principal que contiene la estructura del formulario y la tarjeta de perfil.
2. **styles.css**: Archivo de estilos personalizado para complementar Bootstrap.
3. **script.js**: Archivo JavaScript que contiene la lógica para gestionar el registro de usuarios.

## Características

- **Formulario de registro**: Permite capturar el nombre, correo, trabajo, teléfono y una descripción sobre el usuario.
- **Vista del perfil**: Los datos ingresados en el formulario se muestran en una tarjeta de perfil.
- **Diseño responsivo**: Compatible con dispositivos móviles y escritorios gracias a Bootstrap.

## Cómo usar el proyecto

1. Clona el repositorio o descarga los archivos.
2. Abre el archivo `index.html` en tu navegador.
3. Llena el formulario con tus datos.
4. Haz clic en el botón **Enviar** para generar y visualizar tu perfil.

## Código JavaScript destacado

### Constructor de usuario

```javascript
class Usuario {
  constructor(nombre, correo, trabajo, telefono, sobreTi) {
      this.nombre = nombre;
      this.correo = correo;
      this.trabajo = trabajo;
      this.telefono = telefono;
      this.sobreTi = sobreTi;
  }
}
```

### Función para registrar al usuario

```javascript
function registerUser() {
  const nombre = document.getElementById("name").value;
  const correo = document.getElementById("email").value;
  const trabajo = document.getElementById("job").value;
  const telefono = document.getElementById("phone").value;
  const sobreTi = document.getElementById("about").value;

  const usuario = new Usuario(nombre, correo, trabajo, telefono, sobreTi);

  document.getElementById("displayName").innerText = usuario.nombre;
  document.getElementById("displayEmail").innerText = usuario.correo;
  document.getElementById("displayJob").innerText = usuario.trabajo;
  document.getElementById("displayPhone").innerText = usuario.telefono;
  document.getElementById("displayAbout").innerText = usuario.sobreTi;

  document.getElementById("profileCard").style.display = "block";
}
```

## Capturas de pantalla

1. **Formulario de registro**: El usuario ingresa sus datos.
2. **Perfil generado**: La información ingresada se muestra en una tarjeta de perfil.

## Estilo personalizado

Algunos estilos adicionales fueron definidos en `styles.css` para personalizar la apariencia del formulario y la tarjeta de perfil.

## Dependencias externas

- [Bootstrap 4.5.2](https://getbootstrap.com/): Framework CSS utilizado para el diseño.

## Mejoras futuras

- Validación adicional de los campos del formulario.
- Almacenamiento de datos en localStorage para persistencia.
- Integración con una base de datos para almacenar usuarios.

## Licencia

Este proyecto está disponible bajo la licencia MIT.

https://sebaspatric.github.io/TarjetaLogin/