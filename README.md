Sistema de Autenticación Básico en PHP:
  Este proyecto es una aplicación web básica en PHP que implementa un sistema de autenticación. 
  Fue diseñado para cumplir con los requisitos de manejo de sesiones, redirección y validación de credenciales. 
  Es ideal como punto de partida para aplicaciones más complejas.

Características:
El sistema incluye las siguientes funcionalidades:

  *Pantalla de Login:
  Un formulario donde el usuario introduce su nombre de usuario y contraseña.
  Validación en el servidor de las credenciales utilizando un array predefinido.

  *Pantalla de Bienvenida:
    Muestra un mensaje personalizado con:
    El nombre del usuario.
    La hora actual.
    Un mensaje de bienvenida específico.
    Incluye un enlace para cerrar la sesión.
  
  *Pantalla de Sin Permisos:
    Si un usuario intenta acceder a la pantalla de bienvenida sin estar autenticado, es redirigido automáticamente a esta página.
  
  *Funcionalidad para Cerrar Sesión:
    Permite al usuario cerrar la sesión y regresar a la pantalla de login.
  
Requisitos Técnicos:
  El proyecto cumple con los siguientes requisitos:

     *Manejo de Sesiones:
       Uso de session_start, $_SESSION y session_destroy para la autenticación y manejo de sesión.
  
     *Redirecciones con header():
       Las páginas restringidas redirigen automáticamente a los usuarios no autenticados.
       
     *Validación con un Array Predefinido:
       Las credenciales son validadas contra un array en el código, simulando una base de datos.
       
Estructura del Proyecto:
   El proyecto tiene los siguientes archivos principales:

       login.php:
        Contiene el formulario de inicio de sesión.
        Valida las credenciales contra un array predefinido.
        Redirige a bienvenida.php si las credenciales son correctas.
        
       bienvenida.php:
        Pantalla principal para usuarios autenticados.
        Muestra un mensaje personalizado con el nombre del usuario, la hora actual y un mensaje adicional.
        Incluye un enlace para cerrar la sesión.
        
        permisos.php:
         Página que se muestra si un usuario no autenticado intenta acceder a una página restringida.
         
        logout.php:
         Cierra la sesión destruyendo los datos almacenados en $_SESSION.
         Redirige a la pantalla de login.
         Cómo Usar el Proyecto
    
El sistema utiliza las siguientes credenciales predefinidas:

  Usuario: admin	
  Contraseña: 1234

  Usuario: 1234
  Contraseña: abcd

Iniciar el Proyecto
Inicia tu servidor local.
Accede al archivo login.php desde tu navegador
Introduce las credenciales válidas y explora las funcionalidades.

Cumplimiento de Requisitos:
-Requisito	Implementación
-Pantalla de login	Formulario HTML en login.php.
-Validación de credenciales	Array predefinido en login.php.
-Manejo de sesiones	Uso de session_start y $_SESSION.
-Redirección para usuarios no autenticados	header() en bienvenida.php.
-Pantalla de bienvenida con datos personalizados	bienvenida.php.
-Cerrar sesión	logout.php con session_destroy().

Ejemplo de Flujo:
Inicio de Sesión:
 El usuario accede a login.php e introduce sus credenciales.
 Si son válidas, es redirigido a bienvenida.php.
Redirección de Seguridad:
 Si alguien intenta acceder directamente a bienvenida.php sin autenticarse, es redirigido a permisos.php.
Cerrar Sesión:
Desde bienvenida.php, el usuario puede cerrar la sesión y volver a login.php.
