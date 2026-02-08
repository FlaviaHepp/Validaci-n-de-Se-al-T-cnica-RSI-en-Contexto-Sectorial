# ☑️Validación de Señal Técnica (RSI) en Contexto Sectorial

RSI Individual vs. Fuerza del Sector

## 📌Descripción general

Este proyecto analiza la efectividad de la señal técnica RSI (>70) evaluando si su capacidad predictiva mejora o empeora según el contexto sectorial en el que ocurre.

La hipótesis central es simple pero poderosa:
- Una señal técnica no vive en el vacío: su fiabilidad depende del régimen del mercado y del sector.

Para comprobarlo, se compara el rendimiento futuro de una acción con RSI elevado bajo dos escenarios:
- 📈 Sector fuerte (RSI promedio sectorial alto)
- 📉 Sector débil (RSI promedio sectorial bajo)

## 🎯Objetivo del análisis

Responder a la pregunta:

**¿La señal RSI > 70 es más efectiva cuando el sector acompaña la tendencia o cuando va en contra?**

Esto permite:
- Validar señales técnicas en contexto (no aisladas)
- Evitar falsas señales en sectores débiles
- Mejorar reglas de entrada/salida para trading sistemático

## 🧠Insight clave

- Una señal de sobrecompra puede indicar continuación en sectores fuertes, pero reversión en sectores débiles.

Este proyecto cuantifica esa diferencia de forma objetiva.

## 🧩Metodología

1. RSI promedio sectorial
- Se calcula el RSI promedio diario por sector, usando todos los tickers disponibles.

2. Señal individual

Se identifican acciones con:
- RSI individual elevado
- Precio de cierre en la fecha de la señal
- Precio de cierre 5 días después (rendimiento futuro)

3. Clasificación del escenario

Cada observación se clasifica en uno de tres escenarios:
- Escenario	Condición
- RSI Alto y Sector Fuerte	RSI > 70 y RSI sectorial > 60
- RSI Alto y Sector Débil	RSI > 70 y RSI sectorial < 40
- Otros	Resto de combinaciones

4. Métrica clave

- Rendimiento porcentual a 5 días, posterior a la señal.

## 📈Output principal

El resultado final muestra, para cada ticker y fecha:
- RSI individual
- RSI promedio del sector
- Rendimiento futuro a 5 días
- Escenario de mercado contextual

Esto permite comparar directamente:
- Continuación vs. reversión
- Señales fuertes vs. señales ruidosas

## 💼Valor de negocio

Este análisis es especialmente útil para:

- 📊 Trading cuantitativo: filtrar señales según contexto

- 🧠 Gestión de riesgo: evitar sobrecompra en sectores débiles

- 🏦 Desk institucional: confirmar si el momentum es sistémico o aislado

- 🤖 Modelos algorítmicos: feature engineering basado en régimen sectorial

## 🛠️Requisitos de datos

El proyecto utiliza las siguientes tablas:
- tickers — clasificación sectorial
- precios_diarios — precios OHLC
- indicadores_tecnicos — RSI calculado por ticker y fecha

## 🚀Posibles extensiones

- Comparar horizontes (3d, 10d, 20d)
- Incluir ADX o volatilidad como filtro adicional
- Backtest por sector
- Aplicar el mismo enfoque a señales de sobreventa (RSI < 30)

## 🧠Conclusión

Este proyecto demuestra que:
- La calidad de una señal técnica depende más del contexto que del indicador en sí.
- El RSI funciona mejor cuando el sector acompaña… y se vuelve peligroso cuando va en contra.
- Una validación cuantitativa de algo que muchos traders intuyen, pero pocos miden.

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.
