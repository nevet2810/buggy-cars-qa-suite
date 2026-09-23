# Caso de Uso: CU-01 - Registro de Usuario

---

| Campo | Detalle |
| :--- | :--- |
| **ID** | `CU-01` |
| **Historia de Usuario Relacionada** | `HU-001` |
| **Módulo** | Register / Authentication |
| **Nombre** | Registro de usuario |
| **Objetivo** | Lograr que el usuario nuevo pueda registrarse de manera exitosa en la página Buggy Cars |
| **Actor** | Usuario Nuevo |
| **Desencadenante (Trigger)** | El usuario hace clic en el botón de registrarse (**Register**) |

---

## Precondiciones
1. El usuario no ha iniciado sesión.
2. El usuario se encuentra en la ventana de **Register**.

---

## Flujo Básico

1. El usuario nuevo ingresa los datos solicitados:
   * `Username`
   * `First Name`
   * `Last Name`
   * `Password`
   * `Confirm Password`
2. El usuario hace clic en el botón **Register**.
3. El sistema valida que los datos ingresados estén completos y cumplan con las reglas de negocio (longitud, complejidad, coincidencia y unicidad).
4. El sistema crea el registro del usuario y lo almacena en la base de datos.
5. El sistema muestra un mensaje confirmando la creación exitosa de la cuenta.

---

## Postcondiciones
* La cuenta del usuario queda registrada en la base de datos y lista para iniciar sesión.

---

## Flujo Alternativo

### FA-1: Cancelar registro
1. En el paso 1 o 2 del flujo básico, el usuario decide no completar el registro e interactúa con otro elemento de navegación o hace clic en el botón **Cancelar**.
2. El sistema cancela el proceso sin guardar ningún dato en la base de datos.
3. El sistema redirige al usuario a la página principal (*Home Page*).

---

## Flujos de Excepciones

* **E-1: Campos vacíos**
  * **Condición:** El usuario intenta registrarse dejando campos obligatorios en blanco.
  * **Resultado:** El sistema muestra el mensaje de error: `"Por favor complete todos los campos obligatorios"`.

* **E-2: Longitud de contraseña**
  * **Condición:** Se intenta ingresar una contraseña inferior a los 6 caracteres.
  * **Resultado:** El sistema muestra el mensaje de error: `"La contraseña debe tener al menos 6 caracteres"`.

* **E-3: Complejidad de contraseña**
  * **Condición:** Se intenta ingresar una contraseña sin al menos una letra mayúscula, una minúscula, un número o un carácter especial.
  * **Resultado:** El sistema muestra un mensaje de error solicitando cumplir con los requisitos de complejidad.

* **E-4: Contraseñas no coinciden**
  * **Condición:** La contraseña ingresada en `Password` es diferente a la ingresada en `Confirm Password`.
  * **Resultado:** El sistema muestra el mensaje de aviso: `"Las contraseñas ingresadas no coinciden"`.

* **E-5: Usuario ya existente**
  * **Condición:** El `Username` ingresado ya se encuentra registrado previamente en la base de datos.
  * **Resultado:** El sistema muestra el mensaje de error: `"El nombre de usuario ya está en uso"`.
  
---

