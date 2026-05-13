# Entidades del Sistema — Great Smile Clinic 🦷

## Basadas en el Modelo Relacional Proporcionado

---

# 1. Entidad: PACIENTES

Almacena la información general y médica de los pacientes de la clínica.

| Atributo         | Tipo de Dato | Llave | Descripción                      |
| ---------------- | ------------ | ----- | -------------------------------- |
| id_paciente      | INT          | PK    | Identificador único del paciente |
| nombre           | VARCHAR(50)  |       | Nombre del paciente              |
| apellido         | VARCHAR(50)  |       | Apellido del paciente            |
| fecha_nacimiento | DATE         |       | Fecha de nacimiento              |
| sexo             | VARCHAR(10)  |       | Género del paciente              |
| telefono         | VARCHAR(15)  |       | Número telefónico                |
| correo           | VARCHAR(100) |       | Correo electrónico               |
| direccion        | VARCHAR(150) |       | Dirección del paciente           |
| alergias         | TEXT         |       | Alergias registradas             |

---

# 2. Entidad: CITAS

Gestiona las citas programadas entre pacientes y dentistas.

| Atributo    | Tipo de Dato | Llave | Descripción              |
| ----------- | ------------ | ----- | ------------------------ |
| id_cita     | INT          | PK    | Identificador de la cita |
| id_paciente | INT          | FK    | Relación con pacientes   |
| id_dentista | INT          | FK    | Relación con dentistas   |
| fecha       | DATE         |       | Fecha de la cita         |
| hora        | TIME         |       | Hora asignada            |
| motivo      | VARCHAR(200) |       | Motivo de consulta       |
| estado      | VARCHAR(20)  |       | Estado de la cita        |

---

# 3. Entidad: DENTISTAS

Contiene la información profesional de los odontólogos.

| Atributo           | Tipo de Dato | Llave | Descripción                  |
| ------------------ | ------------ | ----- | ---------------------------- |
| id_dentista        | INT          | PK    | Identificador del dentista   |
| nombre             | VARCHAR(50)  |       | Nombre                       |
| apellido           | VARCHAR(50)  |       | Apellido                     |
| especialidad       | VARCHAR(100) |       | Especialidad odontológica    |
| telefono           | VARCHAR(15)  |       | Número telefónico            |
| correo             | VARCHAR(100) |       | Correo electrónico           |
| cedula_profesional | VARCHAR(30)  |       | Número de cédula profesional |

---

# 4. Entidad: HISTORIAL_CLINICO

Registra antecedentes médicos y diagnósticos del paciente.

| Atributo       | Tipo de Dato | Llave | Descripción                 |
| -------------- | ------------ | ----- | --------------------------- |
| id_historial   | INT          | PK    | Identificador del historial |
| id_paciente    | INT          | FK    | Relación con pacientes      |
| diagnostico    | TEXT         |       | Diagnóstico clínico         |
| observaciones  | TEXT         |       | Observaciones médicas       |
| enfermedades   | TEXT         |       | Enfermedades registradas    |
| fecha_registro | DATE         |       | Fecha de registro           |

---

# 5. Entidad: CONSULTAS

Almacena información de las consultas odontológicas realizadas.

| Atributo       | Tipo de Dato  | Llave | Descripción               |
| -------------- | ------------- | ----- | ------------------------- |
| id_consulta    | INT           | PK    | Identificador de consulta |
| id_paciente    | INT           | FK    | Relación con pacientes    |
| id_dentista    | INT           | FK    | Relación con dentistas    |
| id_tratamiento | INT           | FK    | Relación con tratamientos |
| fecha          | DATE          |       | Fecha de consulta         |
| observaciones  | TEXT          |       | Observaciones clínicas    |
| costo_final    | DECIMAL(10,2) |       | Costo total               |

---

# 6. Entidad: TRATAMIENTOS

Contiene los tratamientos disponibles en la clínica.

| Atributo           | Tipo de Dato  | Llave | Descripción                   |
| ------------------ | ------------- | ----- | ----------------------------- |
| id_tratamiento     | INT           | PK    | Identificador del tratamiento |
| nombre_tratamiento | VARCHAR(100)  |       | Nombre del tratamiento        |
| descripcion        | TEXT          |       | Descripción del procedimiento |
| costo              | DECIMAL(10,2) |       | Precio del tratamiento        |
| duracion_aprox     | VARCHAR(50)   |       | Duración aproximada           |

---

# 7. Entidad: PAGOS

Controla los pagos realizados por los pacientes.

| Atributo    | Tipo de Dato  | Llave | Descripción            |
| ----------- | ------------- | ----- | ---------------------- |
| id_pago     | INT           | PK    | Identificador del pago |
| id_paciente | INT           | FK    | Relación con pacientes |
| monto       | DECIMAL(10,2) |       | Cantidad pagada        |
| metodo_pago | VARCHAR(30)   |       | Método de pago         |
| fecha_pago  | DATE          |       | Fecha del pago         |
| estado_pago | VARCHAR(20)   |       | Estado del pago        |

---

# 8. Entidad: PROVEEDORES

Registra la información de proveedores de materiales odontológicos.

| Atributo       | Tipo de Dato | Llave | Descripción                 |
| -------------- | ------------ | ----- | --------------------------- |
| id_proveedor   | INT          | PK    | Identificador del proveedor |
| nombre_empresa | VARCHAR(100) |       | Nombre de la empresa        |
| telefono       | VARCHAR(15)  |       | Número telefónico           |
| correo         | VARCHAR(100) |       | Correo electrónico          |
| direccion      | VARCHAR(150) |       | Dirección del proveedor     |

---

# 9. Entidad: INVENTARIO

Administra los productos y materiales clínicos.

| Atributo        | Tipo de Dato  | Llave | Descripción                |
| --------------- | ------------- | ----- | -------------------------- |
| id_producto     | INT           | PK    | Identificador del producto |
| nombre_producto | VARCHAR(100)  |       | Nombre del producto        |
| cantidad        | INT           |       | Stock disponible           |
| fecha_caducidad | DATE          |       | Fecha de vencimiento       |
| precio          | DECIMAL(10,2) |       | Precio del producto        |
| id_proveedor    | INT           | FK    | Relación con proveedores   |

---

# Relaciones Principales del Sistema

| Relación                      | Cardinalidad |
| ----------------------------- | ------------ |
| PACIENTES → CITAS             | 1 : N        |
| DENTISTAS → CITAS             | 1 : N        |
| PACIENTES → HISTORIAL_CLINICO | 1 : N        |
| PACIENTES → CONSULTAS         | 1 : N        |
| DENTISTAS → CONSULTAS         | 1 : N        |
| TRATAMIENTOS → CONSULTAS      | 1 : N        |
| PACIENTES → PAGOS             | 1 : N        |
| PROVEEDORES → INVENTARIO      | 1 : N        |
