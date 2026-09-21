# **CASOS DE USO**

- ## **ID:** CU-01

- ## **Modulo:** Register / Authentication

- ## **Nombre:** Registro de usuario

- ## **Objetivo:** Lograr que el usuario nuevo pueda registrarse de manera exitosa en la página Buggy Cars

- ## **ACTOR:** Usuario Nuevo

- ## **Precondiciones:** <br> 1. El usuario no ha iniciado sesión.<br> 2. El usuario se encuentra en la ventana de Register

- ## **Desencadenante (Trigger):** El usuario da clic en el botón de registrarse (**Register**)

- ## **Flujo Básico:** <br> 1. El usuario nuevo ingresa los datos solicitados (`Username`, `First Name`, `Last Name`, `Password` y `Confirm Password`).<br> 2. El usuario da clic en el Botón de registrarse.<br> 3. El sistema valida que los datos cumplan con las reglas de negocio.<br>4. El usuario se crea y almacena en la base de datos.<br> 5. El sistema muestra un mensaje confirmando la creación exitosa de la cuenta

- ## **Postcondiciones:** La cuenta del usuario queda registrada en la base de datos y lista para iniciar sesión

- ## **• Flujo Alternativo**

* ### **FA-1 Cancelar registro:** <BR>1. En el paso 1 o 2 del flujo básico, el usuario decide no completar el registro e interactúa con otro elemento de navegación o botón de cancelar.<BR> 2. El sistema cancela el proceso sin guardar ningún dato en la base de datos.<BR> 3. El sistema redirige al usuario a la página principal (*Home Page*).

## Flujos de Excepciones:
* ### **E-1 Longitud de contraseña:** Si se intenta ingresar una contraseña inferior a los 6 caracteres, el sistema muestra un mensaje de error: `"La contraseña debe tener al menos 6 caracteres"`.
* ### **E-2 Complejidad de contraseña:** Si se intenta ingresar una contraseña sin una letra mayúscula, minúscula, numeral o carácter especial, el sistema muestra un mensaje de error solicitando cumplir dichos requisitos.
* ### **E-3 Campos vacíos:** Si el usuario intenta registrarse dejando campos obligatorios en blanco, el sistema muestra el mensaje: `"Por favor complete todos los campos obligatorios"`.
* ### **E-4 Contraseñas no coinciden:** Si la contraseña ingresada en `Password` es distinta a la de `Confirm Password`, el sistema muestra el mensaje: `"Las contraseñas ingresadas no coinciden"`.
* ### **E-5 Usuario ya existente:** Si el usuario ya ha sido registrado previamente, el sistema muestra el mensaje de error: `"El nombre de usuario ya está en uso"`.