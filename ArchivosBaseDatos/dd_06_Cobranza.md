### 6. COBRANZAS

#### DCMST
Descripcion: Maestro de Cobranzas Documentarias.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| fecha_recepcion | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_pendiente | DECIMAL | 18,2 | NO | NO | - |
| tipo_documento | VARCHAR | 20 | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_dcmst_pk`: (id)
- `idx_dcmst_created_at`: (created_at)

#### APPRV
Descripcion: Cobranzas pendientes de Aprobación.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_carta_credito | VARCHAR | 30 | SI | SI | LCMST.numero_carta_credito |
| tipo_registro | VARCHAR | 20 | SI | NO | - |
| fecha_recepcion | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_pendiente | DECIMAL | 18,2 | NO | NO | - |
| tipo_documento | VARCHAR | 20 | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_apprv_pk`: (numero_carta_credito, tipo_registro)
- `idx_apprv_created_at`: (created_at)

#### LCFEE
Descripcion: Control de Cobro de Comisiones

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_carta_credito | VARCHAR | 30 | SI | SI | LCMST.numero_carta_credito |
| codigo_de_comision | VARCHAR | 20 | SI | NO | - |
| fecha_recepcion | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_pendiente | DECIMAL | 18,2 | NO | NO | - |
| tipo_documento | VARCHAR | 20 | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_lcfee_pk`: (numero_carta_credito, codigo_de_comision)
- `idx_lcfee_created_at`: (created_at)

#### CNTRLRCO
Descripcion: Tabla de Cargos por Servicios o Tarifas de Cobranzas.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| tipo_producto | VARCHAR | 20 | SI | NO | - |
| numero_tabla | VARCHAR | 30 | SI | NO | - |
| fecha_recepcion | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_pendiente | DECIMAL | 18,2 | NO | NO | - |
| tipo_documento | VARCHAR | 20 | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrlrco_pk`: (codigo_banco, tipo_producto)
- `idx_cntrlrco_created_at`: (created_at)
