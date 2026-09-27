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