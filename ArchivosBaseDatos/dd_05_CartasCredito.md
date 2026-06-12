### 5. CARTAS DE CRÉDITO

#### LCMST
Descripcion: Maestro de Cartas de Crédito.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| banco_corresponsal | VARCHAR | 80 | NO | NO | - |
| pais_destino | VARCHAR | 80 | NO | NO | - |
| estado_carta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_lcmst_pk`: (id)
- `idx_lcmst_created_at`: (created_at)

#### LCDOC
Descripcion: Documentos de Cartas de Crédito

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_carta_credito | VARCHAR | 30 | SI | SI | LCMST.numero_carta_credito |
| tipo_registro | VARCHAR | 20 | SI | NO | - |
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_documento | VARCHAR | 20 | SI | NO | - |
| numero_linea | VARCHAR | 30 | SI | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| banco_corresponsal | VARCHAR | 80 | NO | NO | - |
| pais_destino | VARCHAR | 80 | NO | NO | - |
| estado_carta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_lcdoc_pk`: (numero_carta_credito, tipo_registro)
- `idx_lcdoc_created_at`: (created_at)

#### LCFIN
Descripcion: Indice de Formatos de Cartas de Crédito

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| nivel | INT | - | SI | NO | - |
| codigo_documento | VARCHAR | 20 | SI | NO | - |
| secuencia_de_texto | VARCHAR | 50 | SI | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| banco_corresponsal | VARCHAR | 80 | NO | NO | - |
| pais_destino | VARCHAR | 80 | NO | NO | - |
| estado_carta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_lcfin_pk`: (nivel, codigo_documento)
- `idx_lcfin_created_at`: (created_at)

#### LCFMT
Descripcion: Formatos de Cartas de Crédito

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_documento | VARCHAR | 20 | SI | NO | - |
| secuencia_de_texto | VARCHAR | 50 | SI | NO | - |
| numero_linea | VARCHAR | 30 | SI | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| banco_corresponsal | VARCHAR | 80 | NO | NO | - |
| pais_destino | VARCHAR | 80 | NO | NO | - |
| estado_carta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_lcfmt_pk`: (codigo_documento, secuencia_de_texto)
- `idx_lcfmt_created_at`: (created_at)

#### LCADM
Descripcion: Enmiendas a Cartas de Crédito

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_carta_credito | VARCHAR | 30 | SI | SI | LCMST.numero_carta_credito |
| numero_enmienda | VARCHAR | 30 | SI | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| banco_corresponsal | VARCHAR | 80 | NO | NO | - |
| pais_destino | VARCHAR | 80 | NO | NO | - |
| estado_carta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_lcadm_pk`: (numero_carta_credito, numero_enmienda)
- `idx_lcadm_created_at`: (created_at)

#### LCCOV
Descripcion: Negociaciones de Cartas de Crédito

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_carta_credito | VARCHAR | 30 | SI | SI | LCMST.numero_carta_credito |
| secuencia | INT | - | SI | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| banco_corresponsal | VARCHAR | 80 | NO | NO | - |
| pais_destino | VARCHAR | 80 | NO | NO | - |
| estado_carta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_lccov_pk`: (numero_carta_credito, secuencia)
- `idx_lccov_created_at`: (created_at)

#### LCDIN
Descripcion: Documentos Recibidos en Cartas de Crédito

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_carta_credito | VARCHAR | 30 | SI | SI | LCMST.numero_carta_credito |
| secuencia | INT | - | SI | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| banco_corresponsal | VARCHAR | 80 | NO | NO | - |
| pais_destino | VARCHAR | 80 | NO | NO | - |
| estado_carta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_lcdin_pk`: (numero_carta_credito, secuencia)
- `idx_lcdin_created_at`: (created_at)

#### LCSTA
Descripcion: Estadística de Aperturas, Enmiendas, Pagos en Cartas de Crédito

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| banco_corresponsal | VARCHAR | 80 | NO | NO | - |
| pais_destino | VARCHAR | 80 | NO | NO | - |
| estado_carta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_lcsta_pk`: (id)
- `idx_lcsta_created_at`: (created_at)

#### CNTRLLCP
Descripcion: Archivo de Control de Cartas de Crédito

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| lcrparm | VARCHAR | 20 | SI | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| banco_corresponsal | VARCHAR | 80 | NO | NO | - |
| pais_destino | VARCHAR | 80 | NO | NO | - |
| estado_carta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrllcp_pk`: (codigo_banco, lcrparm)
- `idx_cntrllcp_created_at`: (created_at)

#### CNTRLRLC
Descripcion: Tabla de Cargos por Servicios o Tarifas de Cartas de Crédito.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| tipo_producto | VARCHAR | 20 | SI | NO | - |
| numero_tabla | VARCHAR | 30 | SI | NO | - |
| fecha_emision | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_original | DECIMAL | 18,2 | NO | NO | - |
| saldo_actual | DECIMAL | 18,2 | NO | NO | - |
| banco_corresponsal | VARCHAR | 80 | NO | NO | - |
| pais_destino | VARCHAR | 80 | NO | NO | - |
| estado_carta | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrlrlc_pk`: (codigo_banco, tipo_producto)
- `idx_cntrlrlc_created_at`: (created_at)
