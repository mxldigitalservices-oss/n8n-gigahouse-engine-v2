# 🎛️ Centro de Control de Prompts — n8n

Este repositorio es el **centro de control de prompts** utilizado por los flujos de automatización en **n8n** para dos marcas:

- 📰 **Farol al Día** — Medio de noticias locales.
- 🍌 **Banana Tech** — Marca de contenido educativo sobre IA y automatización.

## 📂 Estructura del repositorio

```
.
├── README.md
├── .gitignore
└── prompts/
    ├── farol_aldia.txt      # System prompt: Editor de noticias locales
    └── banana_tech.txt      # System prompt: Experto en IA / carruseles educativos
```

## 🎯 Propósito

Los flujos de n8n consumen estos archivos `.txt` como **system prompts** para los nodos de IA (por ejemplo, nodos de OpenAI/Claude/HTTP Request), centralizando así la edición de tono, estilo y estructura de cada marca en un solo lugar versionado con Git.

## 🔄 Flujo de trabajo recomendado

1. Edita el archivo de prompt correspondiente dentro de `prompts/`.
2. Guarda los cambios.
3. Haz `git add`, `git commit` y `git push`.
4. El nodo de n8n que lee el prompt (vía HTTP Request al raw de GitHub, o mediante sincronización local) tomará automáticamente la versión más reciente.

## 🏷️ Marcas

| Marca | Archivo | Enfoque |
|---|---|---|
| Farol al Día | `prompts/farol_aldia.txt` | Noticias locales, tono cercano y profesional |
| Banana Tech | `prompts/banana_tech.txt` | Carruseles educativos de IA, gancho + explicación + CTA |

---
*Mantenido por Josué — Automatizaciones n8n.*
