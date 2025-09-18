# Trabajo 1 – Análisis de Expectativas y Tipo de Cambio en Perú (2015–2025)

Descripción:

Este proyecto analiza la relación entre el tipo de cambio, la tasa de política monetaria (TPM) y las expectativas empresariales en Perú entre 2015 y 2025. Se utilizan datos oficiales del Banco Central de Reserva del Perú (BCRP) y se realiza un análisis exploratorio (EDA) para identificar patrones, relaciones y efectos de shocks como el Covid-19.

Datos:

- **Fuente**: Banco Central de Reserva del Perú (BCRP).  
- **Series utilizadas**:  
  - Tipo de cambio de compra  
  - Tasa de política monetaria (TPM)  
  - Expectativas de economía  
  - Expectativas de demanda  
  - Expectativas de sector  
- **Última actualización**: julio 2025.

Variables principales:

- **Fecha**: Fecha del periodo (mensual). Formato en el dataset: `YYYY-MM-01` (se toma el primer día del mes). Rango del análisis: 2015-01 a 2025-07 (ajustar si se actualiza la fuente).

- **Tipo_Cambio_Compra** (PN01214PM): Tipo de cambio interbancario — *compra* (S/ por US$), fin de periodo. Numérico, mensual. Indica el precio del dólar en soles; valores mayores = depreciación del sol.

- **Tasa_Politica_Monetaria / TPM** (PD04722MM): Tasa de referencia de política monetaria del BCRP (% anual). Numérica, mensual. Instrumento principal de la política monetaria usado para influir inflación, liquidez y tipo de cambio.

- **Expectativas_Economia** (PD37981AM): Índice de expectativas empresariales sobre la economía a 12 meses. Escala indexada (aprox. 0–100); valores >50 indican expectativa positiva / optimismo, <50 indican pesimismo.

- **Venta_Según_Mes_Anterior** (PD38041AM): Índice que refleja la expectativa de ventas respecto al mes anterior. Indexado; útil para medir dinamismo de la demanda a corto plazo.

- **Situacion_Negocio** (PD38044AM): Índice de la situación actual del negocio declarado por encuestados. Indexado; mide percepción presente (condición operativa y ventas actuales).

- **Expectativas_Demanda** (PD39751AM): Índice de expectativas de demanda por sus productos a 12 meses. Indexado; mide la expectativa de mercado para el horizonte anual.

- **Expectativas_Sector** (PD39752AM): Índice de expectativas del sector a 12 meses. Indexado; refleja la visión agregada del sector productivo al que pertenecen los encuestados.

- **Expectativa_Tipo_Cambio** (Encuesta BCRP — archivo Excel): Expectativa reportada del tipo de cambio (p. ej. fin de año o horizonte a 12 meses). Numérica, se utiliza para contrastar expectativas de tipo de cambio con el TC observado.

**Notas:**  
- Todas las series son **mensuales** y provienen del Banco Central de Reserva del Perú (BCRP).  
- Los índices de expectativas suelen interpretarse con el umbral **50**: por encima = optimismo, por debajo = pesimismo.  
- En el CSV final (`dataset_final.csv`) las columnas usan exactamente los nombres anteriores para facilitar la reproducibilidad del notebook.


Instrucciones de ejecución
1. Clonar este repositorio.  
   ```bash
   git clone https://github.com/tu_usuario/Trabajo1_ICD.git
   cd Trabajo1_ICD
