
### 4. CONTRATOS/CERTIFICADOS/GIROS/VALORES AL COBRO

#### DEALS
Descripcion: Maestro de Préstamos, Certificados, Giros, Valores al Cobro, Inversiones.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| fecha_desembolso | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| tasa_interes | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| dias_mora | INT | - | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_deals_pk`: (id)
- `idx_deals_created_at`: (created_at)

#### DLPMT
Descripcion: Plan de Pagos

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| numero_prestamo | VARCHAR | 30 | SI | SI | DEALS.numero_prestamo |
| fecha | DATE | - | SI | NO | - |
| tipo_registro | VARCHAR | 20 | SI | NO | - |
| fecha_desembolso | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| tasa_interes | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| dias_mora | INT | - | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_dlpmt_pk`: (codigo_banco, codigo_sucursal)
- `idx_dlpmt_fecha`: (fecha)

#### DLDRF
Descripcion: Detalle de Giros y Valores al Cobro.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| numero_prestamo | VARCHAR | 30 | SI | SI | DEALS.numero_prestamo |
| identificacion | VARCHAR | 50 | SI | NO | - |
| numero_documento | VARCHAR | 30 | SI | NO | - |
| fecha_desembolso | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| tasa_interes | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| dias_mora | INT | - | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_dldrf_pk`: (codigo_banco, codigo_sucursal)
- `idx_dldrf_created_at`: (created_at)

#### DLSDE
Descripcion: Detalle de Deducciones del Plan de Pagos

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_prestamo | VARCHAR | 30 | SI | SI | DEALS.numero_prestamo |
| fecha | DATE | - | SI | NO | - |
| tipo_registro | VARCHAR | 20 | SI | NO | - |
| secuencia | INT | - | SI | NO | - |
| codigo_deduccion | VARCHAR | 20 | SI | NO | - |
| fecha_desembolso | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| tasa_interes | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| dias_mora | INT | - | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_dlsde_pk`: (numero_prestamo, fecha)
- `idx_dlsde_fecha`: (fecha)

#### DLCLP
Descripcion: Calificación y Previsión de Cartera.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_cliente | VARCHAR | 30 | SI | SI | CUMST.id_cliente |
| numero_cuenta | VARCHAR | 24 | SI | NO | - |
| referencia | VARCHAR | 50 | SI | NO | - |
| fecha_desembolso | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| tasa_interes | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| dias_mora | INT | - | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_dlclp_pk`: (id_cliente, numero_cuenta)
- `idx_dlclp_created_at`: (created_at)

#### DDCPN
Descripcion: Transacciones pendientes de Cobro.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_prestamo | VARCHAR | 30 | SI | SI | DEALS.numero_prestamo |
| fecha_desembolso | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| tasa_interes | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| dias_mora | INT | - | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ddcpn_pk`: (numero_prestamo)
- `idx_ddcpn_created_at`: (created_at)

#### DLITP
Descripcion: Maestro de Deducciones de Préstamos.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_prestamo | VARCHAR | 30 | SI | SI | DEALS.numero_prestamo |
| codigo_deduccion | VARCHAR | 20 | SI | NO | - |
| fecha_desembolso | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| tasa_interes | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| dias_mora | INT | - | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_dlitp_pk`: (numero_prestamo, codigo_deduccion)
- `idx_dlitp_created_at`: (created_at)

#### CDRTE
Descripcion: Tabla de Tasas de Depósitos

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_tabla | VARCHAR | 30 | SI | NO | - |
| fecha | DATE | - | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| fecha_desembolso | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| tasa_interes | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| dias_mora | INT | - | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cdrte_pk`: (numero_tabla, fecha)
- `idx_cdrte_fecha`: (fecha)

#### CNTRLDLS
Descripcion: Tabla de Tasas para control de Préstamos.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| numero_tabla | VARCHAR | 30 | SI | NO | - |
| tipo_producto | VARCHAR | 20 | SI | NO | - |
| fecha_desembolso | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| tasa_interes | DECIMAL | 18,2 | NO | NO | - |
| plazo_meses | INT | - | NO | NO | - |
| dias_mora | INT | - | NO | NO | - |
| estado_operacion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrldls_pk`: (codigo_banco, numero_tabla)
- `idx_cntrldls_created_at`: (created_at)
