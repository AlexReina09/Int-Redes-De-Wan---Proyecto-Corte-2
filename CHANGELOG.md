# Changelog

Todos los cambios notables de este proyecto se documentan en este archivo.

El formato sigue las convenciones de [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/) y este proyecto usa [Versionado Semántico](https://semver.org/lang/es/).

## [0.1.0] - 2026-09-25

### Añadido
- Lanzamiento inicial de NetForge como aplicación de un solo archivo HTML.
- Calculadora de subnetting IPv4: red, broadcast, rango de host, wildcard, clase, tipo de dirección y división en subredes (por número de subredes o por hosts requeridos), con exportación CSV.
- Calculadora de subnetting IPv6 con aritmética de 128 bits (`BigInt`): expansión, compresión y generación de subredes por prefijo.
- Constructor de topología interactivo basado en SVG, con inventario editable y exportación/importación en JSON.
- Generador de configuraciones para Cisco IOS, Huawei VRP, Fortinet FortiOS y MikroTik RouterOS: base/hostname, VLAN + interfaz, interfaz enrutada, ruta estática, OSPF básico, ACL/política de firewall.
- Módulo de ciberdefensa: checklist de defensa en profundidad y generador de baseline de hardening por fabricante.
- Estructura de repositorio lista para GitHub: README, LICENSE (MIT), VERSION y .gitignore.

### Notas
- Sin dependencias externas de build; solo carga tipografías desde Google Fonts (opcional, con fallback a fuentes de sistema).

[0.1.0]: https://github.com/<tu-usuario>/netforge/releases/tag/v0.1.0
