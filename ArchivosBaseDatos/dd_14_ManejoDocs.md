### 14. MANEJO DE DOCUMENTOS

#### DIMST
Descripcion: Maestro de Inventario de Documentos

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| tipo_cuenta | VARCHAR | 20 | SI | NO | - |
| numero_tabla | VARCHAR | 30 | SI | SI | DITBL.numero_tabla |
| secuencia | INT | - | SI | NO | - |
| tipo_documento | VARCHAR | 20 | NO | NO | - |
| descripcion_documento | VARCHAR | 120 | NO | NO | - |
| obligatorio | BOOLEAN | - | NO | NO | - |
| fecha_recepcion | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_dimst_pk`: (tipo_cuenta, numero_tabla)
- `idx_dimst_created_at`: (created_at)

#### DITBL
Descripcion: Tablas de Tipos de Documentos.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_tabla | VARCHAR | 30 | SI | NO | - |
| secuencia | INT | - | SI | NO | - |
| tipo_documento | VARCHAR | 20 | NO | NO | - |
| descripcion_documento | VARCHAR | 120 | NO | NO | - |
| obligatorio | BOOLEAN | - | NO | NO | - |
| fecha_recepcion | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ditbl_pk`: (numero_tabla, secuencia)
- `idx_ditbl_created_at`: (created_at)
