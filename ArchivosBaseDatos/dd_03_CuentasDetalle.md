
### 3. CUENTAS DE DETALLE/CHEQUERAS

#### ACMST
Descripcion: Archivo Maestro de Cuentas de Detalle

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_acmst_pk`: (id)
- `idx_acmst_created_at`: (created_at)

#### STPMT
Descripcion: Ordenes de No Pago de Cheques

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| cuenta_contable | VARCHAR | 24 | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | SI | ACMST.numero_cuenta |
| secuencia | INT | - | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_stpmt_pk`: (codigo_banco, codigo_sucursal)
- `idx_stpmt_created_at`: (created_at)

#### UNCOL
Descripcion: Maestro de Retenciones

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_uncol_pk`: (codigo_banco, codigo_sucursal)
- `idx_uncol_created_at`: (created_at)

#### PBTRN
Descripcion: Transacciones de Libretas de Ahorro

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_cuenta | VARCHAR | 24 | SI | SI | ACMST.numero_cuenta |
| fecha | DATE | - | SI | NO | - |
| hora | TIME | - | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_pbtrn_pk`: (numero_cuenta, fecha)
- `idx_pbtrn_fecha`: (fecha)

#### OFMST
Descripcion: Maestro de Cheques Certificados y Cheques de Gerencia.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| numero_cheque | VARCHAR | 30 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ofmst_pk`: (codigo_banco, codigo_sucursal)
- `idx_ofmst_created_at`: (created_at)

#### RCLNB
Descripcion: Transacciones de Cuentas Reconciliables

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| cuenta_contable | VARCHAR | 24 | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | SI | ACMST.numero_cuenta |
| fecha | DATE | - | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_rclnb_pk`: (codigo_banco, codigo_sucursal)
- `idx_rclnb_fecha`: (fecha)

#### TLMST
Descripcion: Maestro de Cajeros

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_de_cajero | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_tlmst_pk`: (codigo_de_cajero, codigo_moneda)
- `idx_tlmst_created_at`: (created_at)

#### TDRCR
Descripcion: Maestro de Transacciones de Cajero

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_de_transaccion | VARCHAR | 20 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_tdrcr_pk`: (codigo_de_transaccion)
- `idx_tdrcr_created_at`: (created_at)

#### AUDIT
Descripcion: Detalle diario de transacciones de caja.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| codigo_cajero | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| referencia | VARCHAR | 50 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_audit_pk`: (codigo_banco, codigo_sucursal)
- `idx_audit_created_at`: (created_at)

#### CHMST
Descripcion: Maestro de Chequeras.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | SI | ACMST.numero_cuenta |
| cheque_inicial | VARCHAR | 50 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_chmst_pk`: (codigo_banco, codigo_sucursal)
- `idx_chmst_created_at`: (created_at)

#### CHPER
Descripcion: Personalizacion de Chequeras.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | SI | CHMST.numero_cuenta |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_chper_pk`: (codigo_banco, codigo_sucursal)
- `idx_chper_created_at`: (created_at)

#### CHSTS
Descripcion: Maestro de cambio de estatus a cuentas de detalle.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| cuenta_contable | VARCHAR | 24 | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_chsts_pk`: (codigo_banco, codigo_sucursal)
- `idx_chsts_created_at`: (created_at)

#### DEVOL
Descripcion: Detalle de Cheques devueltos.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_cuenta | VARCHAR | 24 | SI | NO | - |
| numero_cheque | VARCHAR | 30 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_devol_pk`: (numero_cuenta, numero_cheque)
- `idx_devol_created_at`: (created_at)

#### CMRIN
Descripcion: Detalle de Cámara Entrante.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| sucursal_moneda | VARCHAR | 50 | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | SI | ACMST.numero_cuenta |
| monto | DECIMAL | 18,2 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cmrin_pk`: (codigo_banco, sucursal_moneda)
- `idx_cmrin_created_at`: (created_at)

#### OVDRF
Descripcion: Archivo diario de Sobregiros.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ovdrf_pk`: (id)
- `idx_ovdrf_created_at`: (created_at)

#### CNTRLMSG
Descripcion: Mensajes a ser impresos en estados de cuenta.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrlmsg_pk`: (codigo_banco)
- `idx_cntrlmsg_created_at`: (created_at)

#### CNTRLRTE
Descripcion: Tabla de Tasas y Cargos por Servicio en Cuentas de Detalle.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| tipo_producto | VARCHAR | 20 | SI | NO | - |
| codigo_tabla | VARCHAR | 20 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrlrte_pk`: (codigo_banco, tipo_producto)
- `idx_cntrlrte_created_at`: (created_at)

#### CNTRLDEV
Descripcion: Definición de las Causales de Devolución de Cheques.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_causal | VARCHAR | 20 | SI | NO | - |
| fecha_apertura | DATE | - | NO | NO | - |
| fecha_ultima_transaccion | DATE | - | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| saldo_disponible | DECIMAL | 18,2 | NO | NO | - |
| limite_sobregiro | DECIMAL | 18,2 | NO | NO | - |
| estado_cuenta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrldev_pk`: (codigo_causal)
- `idx_cntrldev_created_at`: (created_at)
