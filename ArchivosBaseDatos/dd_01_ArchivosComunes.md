#### CNOFT
Descripcion: Archivo Maestro de Tablas de Datos Comunes.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_tabla | VARCHAR | 20 | SI | NO | - |
| idioma | VARCHAR | 20 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cnoft_pk`: (codigo_tabla, idioma)
- `idx_cnoft_created_at`: (created_at)

#### CNOFC
Descripcion: Archivo de Referencias del Sistema o de Datos Comunes.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_tabla | VARCHAR | 20 | SI | NO | - |
| codigo_registro | VARCHAR | 20 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cnofc_pk`: (codigo_tabla, codigo_registro)
- `idx_cnofc_created_at`: (created_at)

#### MLNCT
Descripcion: Archivo de patrones/formatos de Notificaciones a Clientes (Usos)

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_de_notificacion | VARCHAR | 20 | SI | NO | - |
| nivel | INT | - | SI | NO | - |
| idioma | VARCHAR | 20 | SI | NO | - |
| secuencia | INT | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_mlnct_pk`: (codigo_banco, codigo_de_notificacion)
- `idx_mlnct_created_at`: (created_at)

#### MLNOT
Descripcion: Archivo que contiene los datos a imprimir en la notificación (Usos)

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| fecha_proceso | DATE | - | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | NO | - |
| codigo_de_notificacion | VARCHAR | 20 | SI | NO | - |
| nivel | INT | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_mlnot_pk`: (codigo_banco, fecha_proceso)
- `idx_mlnot_fecha`: (fecha_proceso)

#### HSNOT
Descripcion: Histórico de Datos impresos en las Notificaciones

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| fecha_proceso | DATE | - | SI | NO | - |
| numero_cuenta | VARCHAR | 24 | SI | NO | - |
| codigo_de_notificacion | VARCHAR | 20 | SI | NO | - |
| nivel | INT | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_hsnot_pk`: (codigo_banco, fecha_proceso)
- `idx_hsnot_fecha`: (fecha_proceso)

#### HEAD
Descripcion: Archivo títulos de reportes

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| nombre_printer_file | VARCHAR | 50 | SI | NO | - |
| secuencia | INT | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_head_pk`: (nombre_printer_file, secuencia)
- `idx_head_created_at`: (created_at)

#### MSSGS
Descripcion: Archivo mensajes de Errores.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_mssgs_pk`: (id)
- `idx_mssgs_created_at`: (created_at)

#### HOLYD
Descripcion: Archivo de Feriados.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| fecha | DATE | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_holyd_pk`: (codigo_moneda, fecha)
- `idx_holyd_fecha`: (fecha)

#### APCLS
Descripcion: Archivo Maestro de Productos.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_de_producto | VARCHAR | 20 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_apcls_pk`: (codigo_banco, codigo_de_producto)
- `idx_apcls_created_at`: (created_at)

#### RATES
Descripcion: Archivos de Tasas de Cambio (Posición / Contra Valor)

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_rates_pk`: (codigo_banco, codigo_moneda)
- `idx_rates_created_at`: (created_at)

#### RTRNS
Descripcion: Historia de Tasas de Cambio.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| fecha | DATE | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_rtrns_pk`: (codigo_banco, codigo_moneda)
- `idx_rtrns_fecha`: (fecha)

#### HLHIS
Descripcion: Archivo histórico de Cambios en Retenciones.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_hlhis_pk`: (id)
- `idx_hlhis_created_at`: (created_at)

#### PRENA
Descripcion: Archivo de Descripciones de Programas en Inglés.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| nombre_programa | VARCHAR | 50 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_prena_pk`: (nombre_programa)
- `idx_prena_created_at`: (created_at)

#### PRENS
Descripcion: Archivo de Descripciones de Programas en Español.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| nombre_programa | VARCHAR | 50 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_prens_pk`: (nombre_programa)
- `idx_prens_created_at`: (created_at)

#### UT500
Descripcion: Agenda Personalizada

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_usuario | VARCHAR | 20 | SI | NO | - |
| fecha | DATE | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ut500_pk`: (codigo_usuario, fecha)
- `idx_ut500_fecha`: (fecha)

#### UT510
Descripcion: Mensajes de Usuarios.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_usuario | VARCHAR | 20 | SI | NO | - |
| fecha | DATE | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ut510_pk`: (codigo_usuario, fecha)
- `idx_ut510_fecha`: (fecha)

#### MICRF
Descripcion: Archivo que contiene los reportes salvados en Microficha.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| tipo_formulario | VARCHAR | 50 | SI | NO | - |
| nombre_reporte | VARCHAR | 50 | SI | NO | - |
| secuencia | INT | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_micrf_pk`: (tipo_formulario, nombre_reporte)
- `idx_micrf_created_at`: (created_at)

#### IBSDD
Descripcion: Diccionario de Datos del IBS

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ibsdd_pk`: (id)
- `idx_ibsdd_created_at`: (created_at)

#### IBTBL
Descripcion: Archivo de Referencias Cruzadas para manejo de Intersucursales.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ibtbl_pk`: (id)
- `idx_ibtbl_created_at`: (created_at)

#### TRANS
Descripcion: Archivo histórico de transacciones

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_transaccion | BIGINT | - | SI | NO | - |
| numero_registro_relativo | VARCHAR | 30 | NO | NO | - |
| codigo_banco | VARCHAR | 20 | NO | NO | - |
| codigo_sucursal | VARCHAR | 20 | NO | NO | - |
| codigo_moneda | VARCHAR | 20 | NO | NO | - |
| cuenta_contable | VARCHAR | 24 | NO | SI | GLMST.cuenta_contable |
| numero_cuenta | VARCHAR | 24 | NO | SI | ACMST.numero_cuenta |
| id_cliente | VARCHAR | 30 | NO | SI | CUMST.id_cliente |
| fecha_operacion | DATE | - | NO | NO | - |
| fecha_valor | DATE | - | NO | NO | - |
| hora_operacion | TIME | - | NO | NO | - |
| tipo_movimiento | VARCHAR | 20 | NO | NO | - |
| debito_credito | CHAR | 1 | NO | NO | - |
| monto | DECIMAL | 18,2 | NO | NO | - |
| saldo_anterior | DECIMAL | 18,2 | NO | NO | - |
| saldo_posterior | DECIMAL | 18,2 | NO | NO | - |
| canal_origen | VARCHAR | 20 | NO | NO | - |
| terminal_origen | VARCHAR | 30 | NO | NO | - |
| referencia_externa | VARCHAR | 40 | NO | NO | - |
| estado_transaccion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_trans_pk`: (id_transaccion)
- `idx_trans_reg_rel`: (numero_registro_relativo)
- `idx_trans_cuenta_fecha`: (numero_cuenta, fecha_operacion)
- `idx_trans_contable_fecha`: (cuenta_contable, fecha_operacion)
- `idx_trans_cliente_fecha`: (id_cliente, fecha_operacion)
- `idx_trans_created_at`: (created_at)

#### TRDSC
Descripcion: Descripciones Adicionales a las Transacciones (TRANS).

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| numero_registro_relativo | VARCHAR | 30 | SI | SI | TRANS.numero_registro_relativo |
| secuencia | INT | - | SI | NO | - |
| tipo_descripcion | VARCHAR | 20 | NO | NO | - |
| texto_descripcion | VARCHAR | 200 | NO | NO | - |
| codigo_idioma | VARCHAR | 5 | NO | NO | - |
| formato_salida | VARCHAR | 20 | NO | NO | - |
| obligatorio | BOOLEAN | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_trdsc_pk`: (numero_registro_relativo, secuencia)
- `idx_trdsc_tipo`: (tipo_descripcion)
- `idx_trdsc_created_at`: (created_at)

#### TTRAN
Descripcion: Archivo Maestro de Transacciones del día.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id_transaccion_dia | BIGINT | - | SI | NO | - |
| numero_registro_relativo | VARCHAR | 30 | NO | SI | TRANS.numero_registro_relativo |
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| codigo_moneda | VARCHAR | 20 | SI | NO | - |
| cuenta_contable | VARCHAR | 24 | SI | SI | GLMST.cuenta_contable |
| numero_cuenta | VARCHAR | 24 | SI | SI | ACMST.numero_cuenta |
| id_cliente | VARCHAR | 30 | NO | SI | CUMST.id_cliente |
| fecha | DATE | - | SI | NO | - |
| fecha_valor | DATE | - | NO | NO | - |
| hora_operacion | TIME | - | NO | NO | - |
| tipo_movimiento | VARCHAR | 20 | NO | NO | - |
| debito_credito | CHAR | 1 | NO | NO | - |
| monto | DECIMAL | 18,2 | NO | NO | - |
| saldo_anterior | DECIMAL | 18,2 | NO | NO | - |
| saldo_posterior | DECIMAL | 18,2 | NO | NO | - |
| canal_origen | VARCHAR | 20 | NO | NO | - |
| terminal_origen | VARCHAR | 30 | NO | NO | - |
| referencia_externa | VARCHAR | 40 | NO | NO | - |
| estado_transaccion | VARCHAR | 20 | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_ttran_pk`: (id_transaccion_dia, codigo_banco)
- `idx_ttran_reg_rel`: (numero_registro_relativo)
- `idx_ttran_cuenta_fecha`: (numero_cuenta, fecha)
- `idx_ttran_contable_fecha`: (cuenta_contable, fecha)
- `idx_ttran_cliente_fecha`: (id_cliente, fecha)
- `idx_ttran_fecha`: (fecha)

#### CIFXF
Descripcion: Relación de operaciones con clientes.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| id | BIGINT | - | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cifxf_pk`: (id)
- `idx_cifxf_created_at`: (created_at)

#### CNTRLCNT
Descripcion: Parámetros Generales del Sistema

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrlcnt_pk`: (codigo_banco)
- `idx_cntrlcnt_created_at`: (created_at)

#### CNTRLBRN
Descripcion: Archivo de Sucursales

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_sucursal | VARCHAR | 20 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrlbrn_pk`: (codigo_banco, codigo_sucursal)
- `idx_cntrlbrn_created_at`: (created_at)

#### CNTRLNUM
Descripcion: Control de Numeración Automática de Operaciones.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_aplicacion | VARCHAR | 20 | SI | NO | - |
| tipo_cuenta | VARCHAR | 20 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrlnum_pk`: (codigo_aplicacion, tipo_cuenta)
- `idx_cntrlnum_created_at`: (created_at)

#### CNTRLTAX
Descripcion: Definiciones para el manejo de cobro de impuestos.

| Campo | Tipo | Tamaño | PK | FK | Referencia |
|---|---|---:|:---:|:---:|---|
| codigo_banco | VARCHAR | 20 | SI | NO | - |
| codigo_impuesto | VARCHAR | 20 | SI | NO | - |
| descripcion | VARCHAR | 120 | NO | NO | - |
| valor_texto | VARCHAR | 50 | NO | NO | - |
| valor_numerico | DECIMAL | 18,2 | NO | NO | - |
| vigencia_desde | DATE | - | NO | NO | - |
| vigencia_hasta | DATE | - | NO | NO | - |
| orden_visualizacion | INT | - | NO | NO | - |
| usuario_creacion | VARCHAR | 30 | NO | NO | - |
| usuario_actualizacion | VARCHAR | 30 | NO | NO | - |
| version_registro | INT | - | NO | NO | - |
| observaciones | VARCHAR | 120 | NO | NO | - |
| estado_registro | CHAR | 1 | NO | NO | - |
| created_at | TIMESTAMP | - | NO | NO | - |
| updated_at | TIMESTAMP | - | NO | NO | - |

Indices sugeridos:
- `idx_cntrltax_pk`: (codigo_banco, codigo_impuesto)
- `idx_cntrltax_created_at`: (created_at)