# CURSO IA - ML
1-Crear el entorno uv (moderno) - No necesita activar entorno
    1.1. Instalar uv a nivel global: curl -LsSf https://astral.sh/uv/install.sh | sh
        1.1.1. Verificar version: uv --version
    1.2. Crear proyecto uv:
        - Ir al directorio: 
            uv init mi-proyecto
            cd mi-proyecto
    1.3. Instalar librerias numpy y pandas:
        - uv add numpy pandas
        Nota: Para instalar dependencias se usa uv add
            -Numpy (Calculo numerico): Objeto central: array (ndarray) para operar con numeros
            -Pandas (Analisis de datos tabulares): Objeto central: DataFrame para datos en forma de tablas
    1.4. Arrancar uv: uv run
2-Estructura de carpetas Cookiecutter Data Science (CCDS): plantilla estandar para ciencia de datos
    -data/ (Corazón de la organización de datos). Se divide en:
        -raw/ : Fuentes de datos originales e inmutables - NO SE DEBE DE MODIFICAR DIRECTAMENTE
        -interim/ : Datos intermedios que han sido filtrados - es un paso entre raw y processed
        -processed/ : Datos finales procesados, listos para el modelado
        -external/: Datos de terceros APIs etc
    -notebooks/ (Para analisis exploratorio EDA y experimentación interactiva) - Se recomienda: una convención de nombres cronologicos - codigo valioso debe migrarse a src/ para que sea reutilizable y testeable. 
    -src/ o {{ cookiecutter.module_name }} (Código reutilizable y de producción). Se estructura en modulos:
        -dataset.py: Scripts para generar o descargar datos
        -features.py: Logica para crear caracterisitcas features para el modelado
        -train.py/predict.py: Código para entrenar modelos y hacer predicciones
        -plots.py: Funciones para generar visualizaciones
        -config.py: Variables de configuración y parametros
    -models/ (Almacena los modelos entrenados y serializados .pkl y .h5 - asi como predicciones y resumenes - Se recomienda mantener fuera del codigo)
    -reports/ (Para entregables finales - PDF, HTML). Es la carpeta que se comparte con los stakeholders o se incluye en publicaciones. Se puede dividir en:
        -figures/: Para graficos
        -tables/: Para tablas
    -references/ (Material explicativo - Referencias - Manuales, documentación)
    -docs/ (Documentación del proyecto para otros devs - Generada automaticamente por MkDocs o Sphinx)