### 9. LINEAS DE CRÉDITO

#### LNECR
Descripcion: Maestro de Lineas de Crédito

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_cliente | VARCHAR | 30 | SI | SI | CUMST.id_cliente |
| numero_linea | VARCHAR | 30 | SI | NO | - |
| fecha_aprobacion | DATE | - | NO | NO | - |
| fecha_vencimiento | DATE | - | NO | NO | - |
| monto_aprobado | DECIMAL | 18,2 | NO | NO | - |
| monto_utilizado | DECIMAL | 18,2 | NO | NO | - |
| monto_disponible | DECIMAL | 18,2 | NO | NO | - |
| estado_linea | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_lnecr_pk`: (id_cliente, numero_linea)
- `idx_lnecr_created_at`: (created_at)
