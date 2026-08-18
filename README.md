# finalysisappUP

[![Ver la app](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://finalysisappup.streamlit.app/)

**➡️ [Abrir la app](https://finalysisappup.streamlit.app/)** — no necesitas instalar nada.

Análisis financiero por sector y volatilidad implícita. Proyecto final de Ingeniería Financiera (8º semestre, Universidad Panamericana).

## Qué hace

| Sección | Contenido |
|---|---|
| **Company Overview** | Ficha de cualquier empresa listada: precio en vivo, fundamentales, márgenes y estados financieros |
| **Sector Dashboard** | Datos por sector e índice desde FinViz Elite (Overview, Valuation, Financial, Ownership, Performance, Technical) |
| **Implied Volatility** | Volatilidad implícita de 103 empresas, IV Rank, IV Percentile, VIX y regresión contra el VIX |
| **News** | Noticias por ticker |

Análisis técnico incluido: Bandas de Bollinger, SMA 20/50/200 y MACD.

## Correr localmente

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Configuración

Los tokens de la API de FinViz Elite van en `.streamlit/secrets.toml`, que **no** se sube al repo:

```toml
token1 = "..."
token2 = "..."
```

En Streamlit Cloud se configuran desde el panel de la app (Settings → Secrets), no en el código.

> Si Streamlit no encuentra los tokens, verifica que el archivo esté en `.streamlit/secrets.toml` y no en la raíz del proyecto.

## Fuentes de datos

- **Yahoo Finance** (vía `yfinance`) — precios, fundamentales y VIX
- **FinViz Elite** — datos por sector, requiere token
- **TastyLive** — histórico de volatilidad implícita
