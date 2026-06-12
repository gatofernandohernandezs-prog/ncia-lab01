### 11. PROVEEDORES Y CUENTAS POR PAGAR

#### BAVEN
Descripcion: Maestro de Proveedores.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_proveedor | VARCHAR | 30 | SI | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_pendiente | DECIMAL | 18,2 | NO | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| estado_cxp | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_baven_pk`: (numero_proveedor)
- `idx_baven_created_at`: (created_at)

#### BAPRC
Descripcion: Maestro de Cuentas por Pagar

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| origen_cuenta | VARCHAR | 20 | SI | NO | - |
| tipo_cuenta | VARCHAR | 20 | SI | NO | - |
| id_cliente | VARCHAR | 30 | SI | SI | CUMST.id_cliente |
| numero_referencia | VARCHAR | 30 | SI | NO | - |
| tipo_registro | VARCHAR | 20 | SI | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_pendiente | DECIMAL | 18,2 | NO | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| estado_cxp | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_baprc_pk`: (codigo_banco, codigo_sucursal)
- `idx_baprc_created_at`: (created_at)

#### BAMOR
Descripcion: Amortizaciones de Cuentas por Pagar

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| origen_cuenta | VARCHAR | 20 | SI | NO | - |
| tipo_cuenta | VARCHAR | 20 | SI | NO | - |
| id_cliente | VARCHAR | 30 | SI | SI | BAPRC.id_cliente |
| numero_referencia | VARCHAR | 30 | SI | NO | - |
| tipo_registro | VARCHAR | 20 | SI | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_pendiente | DECIMAL | 18,2 | NO | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| estado_cxp | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_bamor_pk`: (codigo_banco, codigo_sucursal)
- `idx_bamor_created_at`: (created_at)

#### BAINP
Descripcion: Transacciones Contables Diarias de Cuentas por Pagar

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_batch | VARCHAR | 30 | SI | NO | - |
| secuencia | INT | - | SI | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_pendiente | DECIMAL | 18,2 | NO | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| estado_cxp | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_bainp_pk`: (numero_batch, secuencia)
- `idx_bainp_created_at`: (created_at)

#### BAHIS
Descripcion: Histórico de Cuentas por Pagar

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| origen_cuenta | VARCHAR | 20 | SI | NO | - |
| tipo_cuenta | VARCHAR | 20 | SI | NO | - |
| id_cliente | VARCHAR | 30 | SI | SI | BAPRC.id_cliente |
| numero_referencia | VARCHAR | 30 | SI | NO | - |
| fecha | DATE | - | SI | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_pendiente | DECIMAL | 18,2 | NO | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| estado_cxp | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_bahis_pk`: (codigo_banco, origen_cuenta)
- `idx_bahis_fecha`: (fecha)

#### CNTRLBAF
Descripcion: Archivo de Control de Cuentas por Pagar (Sección Comisiones).

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_pendiente | DECIMAL | 18,2 | NO | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| estado_cxp | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrlbaf_pk`: (codigo_banco, codigo_moneda)
- `idx_cntrlbaf_created_at`: (created_at)

#### CNTRLBAP
Descripcion: Archivo de Control de Cuentas por Pagar (Otros Parámetros).

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| numero_identificacion | VARCHAR | 30 | NO | NO | - |
| razon_social | VARCHAR | 80 | NO | NO | - |
| email | VARCHAR | 80 | NO | NO | - |
| telefono | VARCHAR | 80 | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_pendiente | DECIMAL | 18,2 | NO | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| estado_cxp | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrlbap_pk`: (codigo_banco, codigo_moneda)
- `idx_cntrlbap_created_at`: (created_at)
