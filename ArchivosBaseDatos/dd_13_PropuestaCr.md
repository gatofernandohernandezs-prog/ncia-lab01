
### 13. PROPUESTA DE CRÉDITO

#### PLPCR
Descripcion: Propuestas de Crédito

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_propuesta | VARCHAR | 30 | SI | NO | - |
| fecha_propuesta | DATE | - | NO | NO | - |
| monto_solicitado | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| tasa_propuesta | DECIMAL | 18,2 | NO | NO | - |
| dictamen_credito | VARCHAR | 120 | NO | NO | - |
| estado_propuesta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_plpcr_pk`: (numero_propuesta)
- `idx_plpcr_created_at`: (created_at)

#### PLPRD
Descripcion: Detalle de Productos asociados a una propuesta.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_propuesta | VARCHAR | 30 | SI | SI | PLPCR.numero_propuesta |
| codigo_producto | VARCHAR | 20 | SI | NO | - |
| tipo_producto | VARCHAR | 20 | SI | NO | - |
| fecha_propuesta | DATE | - | NO | NO | - |
| monto_solicitado | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| tasa_propuesta | DECIMAL | 18,2 | NO | NO | - |
| dictamen_credito | VARCHAR | 120 | NO | NO | - |
| estado_propuesta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_plprd_pk`: (numero_propuesta, codigo_producto)
- `idx_plprd_created_at`: (created_at)

#### PLGRT
Descripcion: Garantías asociadas a las propuestas de crédito.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_propuesta | VARCHAR | 30 | SI | SI | PLPCR.numero_propuesta |
| secuencia | INT | - | SI | NO | - |
| fecha_propuesta | DATE | - | NO | NO | - |
| monto_solicitado | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| tasa_propuesta | DECIMAL | 18,2 | NO | NO | - |
| dictamen_credito | VARCHAR | 120 | NO | NO | - |
| estado_propuesta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_plgrt_pk`: (numero_propuesta, secuencia)
- `idx_plgrt_created_at`: (created_at)

#### DPMST
Descripcion: Cabecera de la Declaración Patrimonial de Personas Naturales.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_cliente | VARCHAR | 30 | SI | NO | - |
| secuencia | INT | - | SI | NO | - |
| fecha_propuesta | DATE | - | NO | NO | - |
| monto_solicitado | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| tasa_propuesta | DECIMAL | 18,2 | NO | NO | - |
| dictamen_credito | VARCHAR | 120 | NO | NO | - |
| estado_propuesta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_dpmst_pk`: (id_cliente, secuencia)
- `idx_dpmst_created_at`: (created_at)

#### DPDTL
Descripcion: Detalle de la Declaración Patrimonial de Personas Naturales.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_cliente | VARCHAR | 30 | SI | SI | DPMST.id_cliente |
| secuencia | INT | - | SI | NO | - |
| tipo_registro | VARCHAR | 20 | SI | NO | - |
| fecha_propuesta | DATE | - | NO | NO | - |
| monto_solicitado | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| tasa_propuesta | DECIMAL | 18,2 | NO | NO | - |
| dictamen_credito | VARCHAR | 120 | NO | NO | - |
| estado_propuesta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_dpdtl_pk`: (id_cliente, secuencia)
- `idx_dpdtl_created_at`: (created_at)

#### IFMST
Descripcion: Cabecera de Declaración Patrimonial de Personas Jurídicas.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_cliente | VARCHAR | 30 | SI | NO | - |
| anio | INT | - | SI | NO | - |
| mes | INT | - | SI | NO | - |
| formato_balance | VARCHAR | 50 | SI | NO | - |
| fecha_propuesta | DATE | - | NO | NO | - |
| monto_solicitado | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| tasa_propuesta | DECIMAL | 18,2 | NO | NO | - |
| dictamen_credito | VARCHAR | 120 | NO | NO | - |
| estado_propuesta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ifmst_pk`: (id_cliente, anio)
- `idx_ifmst_created_at`: (created_at)

#### IFDTL
Descripcion: Detalle de Declaración Patrimonial de Personas Jurídicas.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_cliente | VARCHAR | 30 | SI | SI | IFMST.id_cliente |
| anio | INT | - | SI | NO | - |
| mes | INT | - | SI | NO | - |
| formato_balance | VARCHAR | 50 | SI | NO | - |
| codigo_linea | VARCHAR | 20 | SI | NO | - |
| codigo_cuenta | VARCHAR | 20 | SI | NO | - |
| fecha_propuesta | DATE | - | NO | NO | - |
| monto_solicitado | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| tasa_propuesta | DECIMAL | 18,2 | NO | NO | - |
| dictamen_credito | VARCHAR | 120 | NO | NO | - |
| estado_propuesta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ifdtl_pk`: (id_cliente, anio)
- `idx_ifdtl_created_at`: (created_at)

#### DPGLN
Descripcion: Plan de Cuentas de nuestros Clientes.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| tipo_balance | VARCHAR | 20 | SI | NO | - |
| codigo_cuenta | VARCHAR | 20 | SI | NO | - |
| fecha_propuesta | DATE | - | NO | NO | - |
| monto_solicitado | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| tasa_propuesta | DECIMAL | 18,2 | NO | NO | - |
| dictamen_credito | VARCHAR | 120 | NO | NO | - |
| estado_propuesta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_dpgln_pk`: (tipo_balance, codigo_cuenta)
- `idx_dpgln_created_at`: (created_at)

#### LIMST
Descripcion: Cabecera de Declaración Legal de Personas Jurídicas.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_cliente | VARCHAR | 30 | SI | NO | - |
| fecha_propuesta | DATE | - | NO | NO | - |
| monto_solicitado | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| tasa_propuesta | DECIMAL | 18,2 | NO | NO | - |
| dictamen_credito | VARCHAR | 120 | NO | NO | - |
| estado_propuesta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_limst_pk`: (id_cliente)
- `idx_limst_created_at`: (created_at)
