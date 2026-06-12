
### 15. SEGURIDAD

#### USERS
Descripcion: Archivo de Autorizaciones por menús

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_usuario | VARCHAR | 20 | SI | NO | - |
| menu | VARCHAR | 20 | SI | NO | - |
| opcion | VARCHAR | 20 | SI | NO | - |
| rol | VARCHAR | 20 | NO | NO | - |
| nivel_autorizacion | INT | - | NO | NO | - |
| permite_consulta | BOOLEAN | - | NO | NO | - |
| permite_creacion | BOOLEAN | - | NO | NO | - |
| permite_actualizacion | BOOLEAN | - | NO | NO | - |
| permite_aprobacion | BOOLEAN | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_users_pk`: (codigo_usuario, menu)
- `idx_users_created_at`: (created_at)
