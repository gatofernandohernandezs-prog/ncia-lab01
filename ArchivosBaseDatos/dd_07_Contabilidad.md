### 7. CONTABILIDAD

#### GLMST
Descripcion: Maestro de Cuentas Contables.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| cuenta_contable | VARCHAR | 24 | SI | NO | - |
| descripcion_cuenta | VARCHAR | 120 | NO | NO | - |
| naturaleza_cuenta | VARCHAR | 20 | NO | NO | - |
| nivel_cuenta | VARCHAR | 50 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| fecha_proceso_sistema | TIMESTAMP | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_glmst_pk`: (codigo_banco, codigo_moneda)
- `idx_glmst_created_at`: (created_at)

#### INPUT
Descripcion: Archivo de Asientos Contables Aprobados (Archivos Derivados).

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_del_lote | VARCHAR | 30 | SI | NO | - |
| secuencia_dentro_del_lote | VARCHAR | 50 | SI | NO | - |
| descripcion_cuenta | VARCHAR | 120 | NO | NO | - |
| naturaleza_cuenta | VARCHAR | 20 | NO | NO | - |
| nivel_cuenta | VARCHAR | 50 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| fecha_proceso_sistema | TIMESTAMP | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_input_pk`: (numero_del_lote, secuencia_dentro_del_lote)
- `idx_input_created_at`: (created_at)

#### GLBLN
Descripcion: Balances Generales

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| cuenta_contable | VARCHAR | 24 | SI | SI | GLMST.cuenta_contable |
| descripcion_cuenta | VARCHAR | 120 | NO | NO | - |
| naturaleza_cuenta | VARCHAR | 20 | NO | NO | - |
| nivel_cuenta | VARCHAR | 50 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| fecha_proceso_sistema | TIMESTAMP | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_glbln_pk`: (codigo_banco, codigo_sucursal)
- `idx_glbln_created_at`: (created_at)

#### GLBSE
Descripcion: Balances Generales Consolidado.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| descripcion_cuenta | VARCHAR | 120 | NO | NO | - |
| naturaleza_cuenta | VARCHAR | 20 | NO | NO | - |
| nivel_cuenta | VARCHAR | 50 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| fecha_proceso_sistema | TIMESTAMP | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_glbse_pk`: (id)
- `idx_glbse_created_at`: (created_at)

#### GLFIN
Descripcion: Estados Financieros por niveles.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| descripcion_cuenta | VARCHAR | 120 | NO | NO | - |
| naturaleza_cuenta | VARCHAR | 20 | NO | NO | - |
| nivel_cuenta | VARCHAR | 50 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| fecha_proceso_sistema | TIMESTAMP | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_glfin_pk`: (id)
- `idx_glfin_created_at`: (created_at)

#### CCDSC
Descripcion: Maestros de Centros de Costos

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| descripcion_cuenta | VARCHAR | 120 | NO | NO | - |
| naturaleza_cuenta | VARCHAR | 20 | NO | NO | - |
| nivel_cuenta | VARCHAR | 50 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| fecha_proceso_sistema | TIMESTAMP | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ccdsc_pk`: (id)
- `idx_ccdsc_created_at`: (created_at)

#### INPT2
Descripcion: Entradas Contables Automáticas generadas en el fin de día.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| descripcion_cuenta | VARCHAR | 120 | NO | NO | - |
| naturaleza_cuenta | VARCHAR | 20 | NO | NO | - |
| nivel_cuenta | VARCHAR | 50 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| fecha_proceso_sistema | TIMESTAMP | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_inpt2_pk`: (id)
- `idx_inpt2_created_at`: (created_at)

#### NXINP
Descripcion: Transacciones Contables del próximo día.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_batch | VARCHAR | 30 | SI | NO | - |
| secuencia | INT | - | SI | NO | - |
| descripcion_cuenta | VARCHAR | 120 | NO | NO | - |
| naturaleza_cuenta | VARCHAR | 20 | NO | NO | - |
| nivel_cuenta | VARCHAR | 50 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| fecha_proceso_sistema | TIMESTAMP | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_nxinp_pk`: (numero_batch, secuencia)
- `idx_nxinp_created_at`: (created_at)

#### BUMST
Descripcion: Maestro de Presupuestos

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| numero_presupuesto | VARCHAR | 30 | SI | NO | - |
| centro_costo | VARCHAR | 50 | SI | NO | - |
| descripcion_cuenta | VARCHAR | 120 | NO | NO | - |
| naturaleza_cuenta | VARCHAR | 20 | NO | NO | - |
| nivel_cuenta | VARCHAR | 50 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| fecha_proceso_sistema | TIMESTAMP | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_bumst_pk`: (codigo_banco, codigo_sucursal)
- `idx_bumst_created_at`: (created_at)
