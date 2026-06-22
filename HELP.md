# Instrucciones y notas
## Dependencias
Para su uso es necesario contar con Python 3.x, Sphinx y Make:

### En derivados de Debian 
``` shell
pip install sphinx
sudo apt install make
```

O tambien: 
``` shell
sudo apt install python3-sphinx make
```
### En windows
Descargar desde:
**[https://www.python.org/downloads/](https://www.python.org/downloads/)**

Luego desde su consola, cmd o PowerShell
``` bash
pip install sphinx
```
Make no viene instalado por defecto en windows pero puede ejecutarse make.bat sin problemas.

## Manual de uso
### Uso en GNU/Linux
Para hacer uso de los formatos de salida ejecutar:
``` shell
make [formato elegido]
```
### Uso en Windows
Ejecutar **`make.bat`** entonces se puede ejecutar
``` PowerShell
make [formato elegido]
```

En caso de querer ejecutar desde Python tambien se puede usar:
``` PowerShell
sphinx-build -b html source _build/html
```

> Todas las salidas se ubicarán en la carpeta `_build`

## Formatos
### Principales
- `html`: Salida HTML estándar
- `singlehtml`: Toda la documentación en un único archivo HTML
- `text`: Salida en texto plano
- `epub`: Formato de libro electrónico (EPUB)
- `latex`: Formato de libro LaTeX (LaTeX) 

### Constructores de integración (IDE / sistemas de ayuda)
- `htmlhelp`: Genera archivos de ayuda HTML de Microsoft (.chm) **(requiere sphinxcontrib-htmlhelp)**
- `qthelp`: Genera documentación para Qt Assistant **(requiere sphinxcontrib-qthelp)**
- `devhelp`: Genera documentación para el visor Devhelp de GNOME **(requiere sphinxcontrib-devhelp)**
- `json`: Salida estructurada en JSON (útil para herramientas y automatización) **(requiere configuraciones adicionales)**
- `doctest`: Ejecuta ejemplos de código incrustados en la documentación **(requiere sphinx.ext.doctest)**

### No recomendables 
- `dirhtml`: HTML con index.html en cada directorio
- `man`: Páginas de manual para Unix/Linux

### No funcionan
- `pickle`: Totalmente obsoleto **(Legacy)**

## Herramientas de calidad y pruebas
- `linkcheck`: Verifica la validez y disponibilidad de enlaces externos
- `changes`: Genera un informe de elementos añadidos, modificados y obsoletos
