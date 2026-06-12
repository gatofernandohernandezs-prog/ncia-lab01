### 12. PAGOS Y TRANSFERENCIAS

#### FIWRT
Descripcion: Transacciones Históricas de Pagos y Recibos.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| numero_transferencia | VARCHAR | 30 | SI | NO | - |
| fecha_operacion | DATE | - | NO | NO | - |
| monto | DECIMAL | 18,2 | NO | NO | - |
| beneficiario | VARCHAR | 80 | NO | NO | - |
| banco_destino | VARCHAR | 80 | NO | NO | - |
| canal_pago | VARCHAR | 20 | NO | NO | - |
| estado_pago | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_fiwrt_pk`: (codigo_banco, numero_transferencia)
- `idx_fiwrt_created_at`: (created_at)

#### POFED
Descripcion: Ordenes de Pago.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| id_cliente | VARCHAR | 30 | SI | NO | - |
| tipo_registro | VARCHAR | 20 | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | NO | - |
| numero_referencia | VARCHAR | 30 | SI | NO | - |
| fecha_operacion | DATE | - | NO | NO | - |
| monto | DECIMAL | 18,2 | NO | NO | - |
| beneficiario | VARCHAR | 80 | NO | NO | - |
| banco_destino | VARCHAR | 80 | NO | NO | - |
| canal_pago | VARCHAR | 20 | NO | NO | - |
| estado_pago | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_pofed_pk`: (codigo_banco, codigo_moneda)
- `idx_pofed_created_at`: (created_at)

#### POSWF
Descripcion: Ordenes de Pago vía Swift.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| id_cliente | VARCHAR | 30 | SI | NO | - |
| tipo_registro | VARCHAR | 20 | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | NO | - |
| numero_referencia | VARCHAR | 30 | SI | NO | - |
| monto | DECIMAL | 18,2 | SI | NO | - |
| fecha_operacion | DATE | - | NO | NO | - |
| beneficiario | VARCHAR | 80 | NO | NO | - |
| banco_destino | VARCHAR | 80 | NO | NO | - |
| canal_pago | VARCHAR | 20 | NO | NO | - |
| estado_pago | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_poswf_pk`: (codigo_banco, codigo_moneda)
- `idx_poswf_created_at`: (created_at)

#### POTLX
Descripcion: Ordenes de Pago vía Télex.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| id_cliente | VARCHAR | 30 | SI | NO | - |
| tipo_registro | VARCHAR | 20 | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | NO | - |
| numero_referencia | VARCHAR | 30 | SI | NO | - |
| fecha_operacion | DATE | - | NO | NO | - |
| monto | DECIMAL | 18,2 | NO | NO | - |
| beneficiario | VARCHAR | 80 | NO | NO | - |
| banco_destino | VARCHAR | 80 | NO | NO | - |
| canal_pago | VARCHAR | 20 | NO | NO | - |
| estado_pago | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_potlx_pk`: (codigo_banco, codigo_moneda)
- `idx_potlx_created_at`: (created_at)

#### SWITF
Descripcion: Histórico de Pagos y Recibidos vía Swift.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| numero_referencia | VARCHAR | 30 | SI | NO | - |
| formato_swift | VARCHAR | 50 | SI | NO | - |
| fecha_operacion | DATE | - | NO | NO | - |
| monto | DECIMAL | 18,2 | NO | NO | - |
| beneficiario | VARCHAR | 80 | NO | NO | - |
| banco_destino | VARCHAR | 80 | NO | NO | - |
| canal_pago | VARCHAR | 20 | NO | NO | - |
| estado_pago | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_switf_pk`: (codigo_banco, numero_referencia)
- `idx_switf_created_at`: (created_at)

#### CNTRLPRF
Descripcion: Archivo de Control de Pagos y Recibos.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| parametro | VARCHAR | 20 | SI | NO | - |
| codigo_tabla | VARCHAR | 20 | SI | NO | - |
| fecha_operacion | DATE | - | NO | NO | - |
| monto | DECIMAL | 18,2 | NO | NO | - |
| beneficiario | VARCHAR | 80 | NO | NO | - |
| banco_destino | VARCHAR | 80 | NO | NO | - |
| canal_pago | VARCHAR | 20 | NO | NO | - |
| estado_pago | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrlprf_pk`: (codigo_banco, parametro)
- `idx_cntrlprf_created_at`: (created_at)
