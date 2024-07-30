# Web Scraping XYZ Corp

Web Scraping XYZ Corp es una aplicación web desarrollada en Flask que extrae citas, autores y etiquetas desde [Quotes to Scrape](http://quotes.toscrape.com/) y las almacena en una base de datos PostgreSQL. La aplicación muestra citas con sus autores y etiquetas, y proporciona información detallada sobre cada autor.


## Tabla de Contenidos
- [Descripción](#descripción)
- [Requisitos](#requisitos)
- [Instalación](#instalación)
- [Uso](#uso)
- [Características](#características)
- [Tecnologías](#tecnologías)
- [Pruebas](#pruebas)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)

## Descripción
Este proyecto está diseñado para extraer datos de un sitio web, almacenarlos en una base de datos y mostrarlos en una aplicación web. Los usuarios pueden ver citas, buscar citas por etiquetas y ver información detallada sobre los autores.

![Captura de Pantalla](images/screenshot.png)

## Requisitos
- Python 3.8+
- PostgreSQL
- Flask
- SQLAlchemy
- BeautifulSoup
- Requests

## Instalación
1. **Clonar el repositorio:**
    ```sh
    git clone https://github.com/yourusername/web-scraping-xyz-corp.git
    cd web-scraping-xyz-corp
    ```

2. **Crear y activar un entorno virtual:**
    ```sh
    python -m venv venv
    source venv/bin/activate  # En Windows usa `venv\Scripts\activate`
    ```

3. **Instalar las dependencias requeridas:**
    ```sh
    pip install -r requirements.txt
    ```

4. **Configurar la base de datos PostgreSQL:**
    - Crear una base de datos PostgreSQL llamada `quotes`.
    - Actualizar el archivo `.env` con las credenciales de la base de datos.

5. **Aplicar las migraciones de la base de datos:**
    ```sh
    flask db init
    flask db migrate
    flask db upgrade
    ```

6. **Ejecutar el scraper para poblar la base de datos:**
    ```sh
    python scraper.py
    ```

## Uso
1. **Ejecutar la aplicación Flask:**
    ```sh
    python app.py
    ```

2. **Acceder a la aplicación:**
    Abre tu navegador web y ve a `http://127.0.0.1:5000`.

## Características
- **Extraer Citas:** Extrae citas, autores y etiquetas del sitio web objetivo.
- **Almacenar Datos:** Guarda los datos extraídos en una base de datos PostgreSQL.
- **Ver Citas:** Muestra citas con sus autores y etiquetas.
- **Detalles del Autor:** Muestra información detallada sobre cada autor, incluyendo una breve biografía.
- **Buscar por Etiquetas:** Busca citas por etiquetas.

## Tecnologías
- **Flask:** Framework web utilizado para construir la aplicación.
- **SQLAlchemy:** ORM para interacciones con la base de datos.
- **BeautifulSoup:** Biblioteca para scraping web.
- **Requests:** Biblioteca para hacer solicitudes HTTP.
- **PostgreSQL:** Sistema de base de datos para almacenar los datos extraídos.

## Pruebas
Se incluyen pruebas unitarias para garantizar la fiabilidad del scraper y de la aplicación web.

1. **Crear una base de datos de prueba y ejecutar las pruebas:**
    ```sh
    pytest
    ```

## Contribuciones
¡Las contribuciones son bienvenidas! Por favor, sigue estos pasos para contribuir:
1. Haz un fork del repositorio.
2. Crea una nueva rama para tu funcionalidad o corrección de errores.
3. Haz commit de tus cambios.
4. Haz push de tu rama y crea un pull request.

## Licencia
Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.
