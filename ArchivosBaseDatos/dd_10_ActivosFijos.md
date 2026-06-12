### 10. ACTIVOS FIJOS

#### FIXMS
Descripcion: Maestro de Activos Fijos

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_activo | VARCHAR | 30 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| fecha_adquisicion | DATE | - | NO | NO | - |
| valor_adquisicion | DECIMAL | 18,2 | NO | NO | - |
| vida_util_meses | INT | - | NO | NO | - |
| depreciacion_acumulada | DECIMAL | 18,2 | NO | NO | - |
| estado_activo | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_fixms_pk`: (numero_activo)
- `idx_fixms_created_at`: (created_at)

#### CLSMS
Descripcion: Maestro de Clases de Amortizaciones de Activos Fijos

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_clase | VARCHAR | 20 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| fecha_adquisicion | DATE | - | NO | NO | - |
| valor_adquisicion | DECIMAL | 18,2 | NO | NO | - |
| vida_util_meses | INT | - | NO | NO | - |
| depreciacion_acumulada | DECIMAL | 18,2 | NO | NO | - |
| estado_activo | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_clsms_pk`: (codigo_clase)
- `idx_clsms_created_at`: (created_at)

#### LOCMS
Descripcion: Maestro de Localizaciones de Activos Fijos

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_localizacion | VARCHAR | 30 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| fecha_adquisicion | DATE | - | NO | NO | - |
| valor_adquisicion | DECIMAL | 18,2 | NO | NO | - |
| vida_util_meses | INT | - | NO | NO | - |
| depreciacion_acumulada | DECIMAL | 18,2 | NO | NO | - |
| estado_activo | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_locms_pk`: (numero_localizacion)
- `idx_locms_created_at`: (created_at)

#### CNTRLFIX
Descripcion: Archivo de Control de Activos Fijos.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| fecha_adquisicion | DATE | - | NO | NO | - |
| valor_adquisicion | DECIMAL | 18,2 | NO | NO | - |
| vida_util_meses | INT | - | NO | NO | - |
| depreciacion_acumulada | DECIMAL | 18,2 | NO | NO | - |
| estado_activo | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrlfix_pk`: (codigo_banco)
- `idx_cntrlfix_created_at`: (created_at)
