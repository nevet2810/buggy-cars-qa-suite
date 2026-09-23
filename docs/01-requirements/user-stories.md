 ## Historia de Usuario relacionada: HU-001
---

| Campo | Detalle |
| :--- | :--- |
| **ID** | `HU-001` |
|**Titulo**|Registro de nuevo usuario|
|**Descripcion**| Como usuario nuevo, quiero registrarme en la plataforma ingresando un usuario, nombre, apellido y contraseña para poder votar por mis carros favoritos.|

---

### Criterios de aceptacion
**1. Campos obligatorios:** Los campos `"Username"`, `"First Name"`, `"Last Name"`, `"Password"` y `"Confirm Password"` son obligatorios.
**2. Fortaleza de la contraseña:** La contraseña debe tener una longitud mínima de 6 caracteres e incluir al menos una letra mayúscula, una minúscula, un número y un carácter especial.
**3. Coincidencia de contraseña:** El valor del campo `"Confirm Password"` debe ser exactamente igual al de `"Password"`.
**4. Registro exitoso:** Si los datos son válidos, el sistema confirma la creación de la cuenta y la almacena en la base de datos.
**5. Validación de usuario existente:** Si el `"Username"` ya está registrado, el sistema impide el registro y muestra un mensaje explicativo.
**6. Acción de cancelación:** Al presionar `"Cancelar"`, el sistema interrumpe el registro sin guardar información y redirige a la página principal `(Home)`.

---