# finalysisappUP

Análisis financiero por sector y volatilidad implícita. Proyecto final de Ingeniería Financiera (8º semestre, Universidad Panamericana).

## Qué hace

- Descarga datos por sector e índice desde FinViz Elite (Overview, Valuation, Financial, Ownership, Performance, Technical)
- Análisis técnico: Bandas de Bollinger, SMA, MACD
- Volatilidad implícita y modelos de regresión lineal

## Cómo correr

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Configuración

Los tokens de la API de FinViz van en `.streamlit/secrets.toml` (no se sube al repo):

```toml
token1 = "..."
token2 = "..."
```

> Nota: la app lee los tokens con `st.secrets`. Si Streamlit no los encuentra, verifica que el archivo esté en `.streamlit/secrets.toml` y no en la raíz del proyecto.

## Ramas

El código vive en `master`. La rama `main` solo contiene el commit inicial.
