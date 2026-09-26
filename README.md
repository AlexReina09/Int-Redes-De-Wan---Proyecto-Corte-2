# NetForge

Kit de ingeniería de redes en un solo archivo HTML: subnetting IPv4/IPv6, constructor de topología, generador de configuraciones multi-fabricante y lineamientos de ciberdefensa.

**No requiere backend, build ni dependencias.** Es un archivo `index.html` autocontenido que corre en cualquier navegador moderno, incluido GitHub Pages.

## Características

- **Subnetting IPv4**: red, broadcast, rango de host, wildcard, clase, tipo (pública/privada), y división en subredes por número de redes o por hosts requeridos, con exportación a CSV.
- **Subnetting IPv6**: aritmética completa de 128 bits (usando `BigInt`), expansión/compresión de direcciones y generación de subredes por prefijo.
- **Constructor de topología**: lienzo interactivo (SVG) para colocar routers, switches, firewalls, servidores y hosts, conectarlos, editar su inventario y exportar/importar la topología como JSON.
- **Generador de configuraciones**: plantillas para **Cisco IOS**, **Huawei VRP**, **Fortinet FortiOS** y **MikroTik RouterOS** — hostname base, VLAN + interfaz de acceso, interfaz enrutada, ruta estática, OSPF básico y ACL/política de firewall.
- **Ciberdefensa**: checklist de defensa en profundidad (alineado conceptualmente a NIST CSF / CIS Controls) y generador de un baseline de hardening por fabricante (gestión cifrada, AAA, ACLs de mínimo privilegio, logging centralizado, etc.).
- **Control de versiones**: pestaña "Versión y changelog" dentro de la propia app, más `CHANGELOG.md` y `VERSION` en el repositorio, siguiendo [Versionado Semántico](https://semver.org/lang/es/).

## Uso rápido

1. Descarga o clona este repositorio.
2. Abre `index.html` directamente en tu navegador, **o**
3. Publícalo con GitHub Pages: `Settings → Pages → Deploy from branch → main / (root)`.

No hay pasos de instalación ni dependencias externas de npm — solo se cargan fuentes tipográficas (Google Fonts) vía CDN; si no hay conexión a internet, la app sigue funcionando con las fuentes del sistema.

## Estructura del repositorio

```
netforge/
├── index.html       # Aplicación completa (HTML + CSS + JS)
├── README.md        # Este archivo
├── CHANGELOG.md      # Historial de versiones (SemVer)
├── VERSION           # Versión actual en texto plano
├── LICENSE            # Licencia MIT
└── .gitignore
```

## Cómo subirlo a GitHub

```bash
git init
git add .
git commit -m "v0.1.0: lanzamiento inicial de NetForge"
git branch -M main
git remote add origin https://github.com/<tu-usuario>/netforge.git
git push -u origin main
```

Para nuevas versiones, actualiza `VERSION`, `CHANGELOG.md` y el badge de versión dentro de `index.html` (`window.NF.version` y el arreglo `CHANGELOG`), y crea un tag:

```bash
git tag -a v0.2.0 -m "Descripción de la versión"
git push origin v0.2.0
```

## Advertencias importantes

- **Ningún software es infalible.** Las plantillas de configuración y hardening son puntos de partida generales; siempre deben revisarse contra el diseño real de tu red y las políticas de cambio de tu organización antes de aplicarse en producción.
- El módulo de ciberdefensa es **puramente defensivo**: checklist de buenas prácticas y comandos de endurecimiento (hardening). No incluye, ni incluirá, técnicas de explotación, escaneo agresivo o intrusión.
- El constructor de topología guarda el estado únicamente en memoria del navegador durante la sesión; usa "Exportar JSON" para conservar tu trabajo.

## Licencia

MIT — ver [`LICENSE`](./LICENSE).
