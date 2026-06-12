### 2. CLIENTES

#### CUMST
Descripcion: Archivo de Maestro de Clientes

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_cliente | VARCHAR | 30 | SI | NO | - |
| tipo_persona | VARCHAR | 20 | NO | NO | - |
| tipo_identificacion | VARCHAR | 20 | NO | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| nombres | VARCHAR | 80 | NO | NO | - |
| apellidos | VARCHAR | 80 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| fecha_nacimiento | DATE | - | NO | NO | - |
| direccion | VARCHAR | 120 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| pais_residencia | VARCHAR | 50 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cumst_pk`: (id_cliente)
- `idx_cumst_created_at`: (created_at)

#### CUMAD
Descripcion: Archivo de Direcciones de Correo y Beneficiarios de Operaciones/Clientes.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_cliente_operacion | VARCHAR | 30 | SI | SI | CUMST.id_cliente |
| tipo_registro | VARCHAR | 20 | SI | NO | - |
| secuencia | INT | - | SI | NO | - |
| tipo_persona | VARCHAR | 20 | NO | NO | - |
| tipo_identificacion | VARCHAR | 20 | NO | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| nombres | VARCHAR | 80 | NO | NO | - |
| apellidos | VARCHAR | 80 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| fecha_nacimiento | DATE | - | NO | NO | - |
| direccion | VARCHAR | 120 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| pais_residencia | VARCHAR | 50 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cumad_pk`: (id_cliente_operacion, tipo_registro)
- `idx_cumad_created_at`: (created_at)

#### CUMPR
Descripcion: Archivo Maestro de Palabras Reservadas que se omiten en Búsqueda de Clientes por String de Caracteres.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| palabra | VARCHAR | 50 | SI | NO | - |
| tipo_persona | VARCHAR | 20 | NO | NO | - |
| tipo_identificacion | VARCHAR | 20 | NO | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| nombres | VARCHAR | 80 | NO | NO | - |
| apellidos | VARCHAR | 80 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| fecha_nacimiento | DATE | - | NO | NO | - |
| direccion | VARCHAR | 120 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| pais_residencia | VARCHAR | 50 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cumpr_pk`: (palabra)
- `idx_cumpr_created_at`: (created_at)

#### CUMSD
Descripcion: Archivo Maestro de Clientes para búsqueda de Clientes a través de un String de Caracteres.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_cliente | VARCHAR | 30 | SI | SI | CUMST.id_cliente |
| tipo_persona | VARCHAR | 20 | NO | NO | - |
| tipo_identificacion | VARCHAR | 20 | NO | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| nombres | VARCHAR | 80 | NO | NO | - |
| apellidos | VARCHAR | 80 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| fecha_nacimiento | DATE | - | NO | NO | - |
| direccion | VARCHAR | 120 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| pais_residencia | VARCHAR | 50 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cumsd_pk`: (id_cliente)
- `idx_cumsd_created_at`: (created_at)

#### SPINS
Descripcion: Archivo de Instrucciones especiales (Usos)

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| tipo_informacion | VARCHAR | 50 | SI | NO | - |
| cuenta_o_cliente | VARCHAR | 50 | SI | SI | CUMST/ACMST.id_cliente/numero_cuenta |
| secuencia | INT | - | SI | NO | - |
| tipo_persona | VARCHAR | 20 | NO | NO | - |
| tipo_identificacion | VARCHAR | 20 | NO | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| nombres | VARCHAR | 80 | NO | NO | - |
| apellidos | VARCHAR | 80 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| fecha_nacimiento | DATE | - | NO | NO | - |
| direccion | VARCHAR | 120 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| pais_residencia | VARCHAR | 50 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_spins_pk`: (tipo_informacion, cuenta_o_cliente)
- `idx_spins_created_at`: (created_at)
