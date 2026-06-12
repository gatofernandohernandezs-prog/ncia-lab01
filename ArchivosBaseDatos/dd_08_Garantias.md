
### 8. GARANTÍAS

#### ROCOL
Descripcion: Maestro de Garantías

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| id_cliente | VARCHAR | 30 | SI | SI | CUMST.id_cliente |
| numero_garantia | VARCHAR | 30 | SI | NO | - |
| tipo_garantia | VARCHAR | 20 | NO | NO | - |
| valor_garantia | DECIMAL | 18,2 | NO | NO | - |
| fecha_avaluo | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| estado_garantia | VARCHAR | 20 | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_rocol_pk`: (codigo_banco, id_cliente)
- `idx_rocol_created_at`: (created_at)

#### RCOLL
Descripcion: Relaciones entre Garantías

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| cuenta_a_garantizar | VARCHAR | 50 | SI | NO | - |
| cuenta_que_garantiza | VARCHAR | 50 | SI | NO | - |
| tipo_garantia | VARCHAR | 20 | NO | NO | - |
| valor_garantia | DECIMAL | 18,2 | NO | NO | - |
| fecha_avaluo | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| estado_garantia | VARCHAR | 20 | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_rcoll_pk`: (codigo_banco, cuenta_a_garantizar)
- `idx_rcoll_created_at`: (created_at)
