# Entrega final – Ecosistema de automatización con IA: control de seguros de mala praxis de médicos externos

Proyecto integrador (Coderhouse, IA Automation). Detecta médicos externos con seguro vencido o documentación pendiente, redacta con IA un borrador de aviso, lo aprueba una persona y recién ahí lo envía. Todos los datos son ficticios.

## Stack
- **Orquestador:** Make (2 escenarios)
- **Base de datos:** Airtable (casos, médicos, compañías, base de conocimiento RAG, log de errores)
- **IA:** Claude Sonnet (Anthropic)
- **Salida:** Gmail

## Contenido
| Archivo | Qué es |
|---|---|
| `Entrega8_Ecosistema_Automatizacion_IA.pdf` | Diagrama de arquitectura, manual de datos con esquemas JSON, matriz de costos, seguridad y resiliencia, pruebas de estrés y evidencias |
| `E8-Escenario-1-Procesar-con-IA.json` | Blueprint de Make: procesa con IA (con ruta de error) |
| `E8-Escenario-2-Enviar-si-Aprobado.json` | Blueprint de Make: envía solo si aprobó una persona |
| `capturas/` | Capturas de las pruebas (datos personales tapados) |

## Enlaces
- Dashboard (solo lectura): LINK_DASHBOARD
- Base de Airtable (solo lectura): LINK_AIRTABLE

## Pruebas de estrés
1. Caso normal. 2. Camino Infeliz (datos incompletos). 3. Falla de la API. 4. Aprobación inválida. 5. Aprobación correcta y envío.

## Nota de seguridad
Los blueprints no incluyen claves ni credenciales: las conexiones viven en Make. Los datos son ficticios.

