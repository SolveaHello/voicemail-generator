# Voicemail Greeting Generator — Habilidad de Claude Code

> **Otros idiomas:** [English](README.md) · [日本語](README.ja.md) · [Français](README.fr.md)

Genera guiones de saludo de buzón de voz profesionales desde tu terminal con Claude Code y conviértelos a MP3 con una voz de IA natural en [Solvea](https://solvea.cx/tools/voicemail-greeting-generator) — sin equipo de grabación ni repeticiones.

## Características

- 5 tipos de saludo: Empresarial, Personal, Festivo, Fuera de horario, Baja por enfermedad
- 7 plantillas por industria: General, Inmobiliaria, Medspa, Comercio, Dental, Despacho jurídico y más
- Guiones optimizados para ≤ 30 segundos hablados
- Enlace directo al generador de voz IA gratuito de Solvea y exportación a MP3
- Compatible con iPhone, Android, RingCentral, Zoom Phone y la mayoría de servicios VoIP

## Instalación

```bash
claude mcp install voicemail-greeting-generator
```

O añade la habilidad manualmente colocando `skill.md` en el directorio de habilidades de Claude Code.

## Uso

```
/voicemail-greeting [opciones]
```

| Opción | Valores | Predeterminado |
|--------|---------|----------------|
| `--type` | `business` · `personal` · `holiday` · `after-hours` · `out-sick` | `business` |
| `--industry` | `general` · `real-estate` · `medspa` · `retail` · `dental` · `law-firm` · `other` | `general` |
| `--name` | Tu nombre o el de tu empresa | *(se solicita)* |
| `--phone` | Número de devolución de llamada | *(opcional)* |
| `--hours` | Horario comercial, p. ej. `Lun-Vie 9:00-18:00` | *(opcional)* |
| `--custom` | Proporciona tu propio guión y omite la generación | *(opcional)* |

## Ejemplos

```bash
# Saludo profesional para el sector inmobiliario
/voicemail-greeting --type business --industry real-estate --name "Inmobiliaria García"

# Mensaje de cierre festivo para una clínica dental
/voicemail-greeting --type holiday --industry dental --name "Clínica Sonrisa"

# Usa tu propio guión e ir directo a la selección de voz
/voicemail-greeting --custom "Gracias por llamar a Acme Corp..."
```

## Cómo funciona

1. Claude genera un guión a medida (o utiliza tu texto personalizado).
2. Revisas el guión y puedes solicitar una ronda de revisiones.
3. Claude te dirige al [Generador de Saludos de Buzón de Voz de Solvea](https://solvea.cx/tools/voicemail-greeting-generator), donde eliges entre 6 voces de IA, previsualizas y descargas tu MP3.

> Las cuentas gratuitas de Solvea incluyen hasta **13 generaciones** — sin tarjeta de crédito.

## Licencia

MIT © Boyuan Gao
