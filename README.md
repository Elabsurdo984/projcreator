# CliPyth

CliPyth es una herramienta de línea de comandos (CLI) que facilita la creación de proyectos Python con diferentes plantillas predefinidas. Simplifica el proceso de iniciar nuevos proyectos con una estructura básica pero funcional.

## Instalación

### Requisitos previos
- Python 3.8 o superior

### Instalación desde PyPI
```bash
pip install CliPyth
```

### Instalación desde el código fuente
```bash
git clone <url-del-repositorio>
cd CliPyth
pip install -e .
```

## Uso

### Comandos básicos

```bash
# Crear un nuevo proyecto de aplicación de consola
CliPyth new console [nombre-del-proyecto]
```

Si no especificas un nombre de proyecto, se utilizará "my-project" por defecto.

### Plantillas disponibles

#### Consola (`console`)
Crea una aplicación de consola básica con la siguiente estructura:

```
nombre-del-proyecto/
├── main.py           # Punto de entrada de la aplicación
├── requirements.txt  # Archivo para listar dependencias
└── README.md         # Documentación básica del proyecto
```

El archivo `main.py` incluye una función `main()` simple que imprime un mensaje de bienvenida.

## Ejemplos de uso

### Crear una aplicación de consola

```bash
CliPyth new console mi-aplicacion
```

Este comando creará un directorio llamado "mi-aplicacion" en el directorio actual con todos los archivos necesarios para una aplicación de consola básica.

### Estructura del proyecto creado

```
mi-aplicacion/
├── main.py           # Contiene la función principal
├── requirements.txt  # Archivo para gestionar dependencias
└── README.md         # Documentación básica
```

### Ejecutar la aplicación creada

```bash
cd mi-aplicacion
python main.py
```

## Desarrollo

### Estructura del proyecto CliPyth

```
CliPyth/
├── CliPyth/
│   ├── __init__.py   # Implementación principal del CLI
│   └── __main__.py   # Punto de entrada para ejecutar como módulo
├── setup.py          # Configuración de instalación
├── README.md         # Documentación
├── Changelog.md      # Registro de cambios
└── LICENSE           # Licencia (MIT)
```

### Añadir nuevas plantillas

Para añadir nuevas plantillas, debes:

1. Crear una nueva función en `__init__.py` (similar a `create_console_app`)
2. Añadir la nueva plantilla a las opciones del argumento `template` en el parser
3. Actualizar la lógica de selección en la función `main()`

## Compatibilidad

CliPyth es compatible con:
- Python 3.8
- Python 3.9
- Python 3.10
- Python 3.11
- Python 3.12
- Python 3.13

## Contribuir

Las contribuciones son bienvenidas. Para contribuir:

1. Haz un fork del repositorio
2. Crea una rama para tu funcionalidad (`git checkout -b nueva-funcionalidad`)
3. Realiza tus cambios y haz commit (`git commit -am 'Añadir nueva funcionalidad'`)
4. Sube los cambios a tu fork (`git push origin nueva-funcionalidad`)
5. Crea un Pull Request


## Licencia

Este proyecto está licenciado bajo la Licencia MIT - ver el archivo LICENSE para más detalles.

## Autor

- **Elabsurdo984** - [matiassfernandez00@gmail.com]

## Agradecimientos

- Inspirado en herramientas como `create-react-app`, `vue-cli` y otras CLI para iniciar proyectos