# IA1 - Los Banqueros - Predicción_aprobación_de_préstamo
Este proyecto busca simular el criterio de aceptación de créditos de una entidad bancaria mediante aprendizaje supervisado, no supervisado y profundo.

## Dataset usado

El dataset "Loan Approval Dataset" es un dataset sintético, creado mediante un proceso de generación de datos con el objetivo de reflejar las distribuciones de variables encontradas en datasets financieros reales, sin divulgar información personal.

Fuente:
https://www.kaggle.com/datasets/amineipad/loan-approval-dataset

Estructura:
- Dataset de 1000 entradas con 10 columnas (1000, 10)
- 6 variables discretas (género, estado marital, no. dependientes, créditos vigentes, estado laboral y loan_approved[target])
- 4 variables continuas (edad, ingresos anuales, monto de crédito y credit score)
- 2 clases: loan_approved == 1 (aprobado), ó 0 (rechazado)

## Archivos usados

El único archivo utilizado en el proyecto (sin contar librerías y qué no) es el archivo .CSV "loanapproval.csv". Sin embargo, debido a problemas encontrados durante el proceso de subirlo, se le tuvo que alterar el título a "loan_approval.csv", lo cual puede causar problemas si no se tiene cuidado con el nombre.

## Usar/conseguir archivos

En los notebooks, se accede al dataset mediante pd.read_csv(), con dirección de ruta

https://raw.githubusercontent.com/Khyii/ia1-los_banqueros-prediccion_aprobacion_de_prestamo/refs/heads/main/loan_approval.csv

y separación por coma (",") y, dado que el repositorio es público, debería funcionar sin importar quién lo hace.

Sin embargo, si esto no funciona o, por cualquier motivo, se desea trabajar con el archivo original de Kaggle, el proceso sería el siguiente:

1. Descargar el archivo de https://www.kaggle.com/datasets/amineipad/loan-approval-dataset/data

2. Cargarlo a los archivos locales del ambiente de computación (directamente o mediante google drive)

3. Encontrar la celda en el notebook con pd.read_csv() y reemplazar la dirección de ruta detallada al inicio del segmento con la ruta del archivo local.

## Objetivo

El proyecto se propuso como el primer paso en una cadena de proyectos cuya escala, francamente, excede la materia vista.

Se busca crear un programa capaz de simular el comportamiento de una entidad bancaria en base a su historial aceptando/rechazando préstamos. Subsecuentemente, se busca crear un ambiente simulado donde múltiples individuos de distintas demográficas y necesidades pidan créditos al banco y, al ser aceptados, o logran pagar sus deudas a tiempo, o necesitan extensiones.

Al final de la simulación, se estima qué tan lucrativo fue el banco, y qué porcentaje de sus deudores quedaron 'enganchados' en algún momento por haber tomado créditos que, después, no fueron capaces de repagar. Finalmente, se deben correr pruebas con distintas alteraciones a la ia para, idealmente, mantener sostenibilidad financiera y minimizar la proporción de deudores eternamente endeudados.

Dada la naturaleza sintética de los datos, tiene poca utilidad inmediata. Sin embargo, el proceso de su creación dice tener distribuciones y variedad que reflejan al mundo real, por lo que puede ser un inicio más "limpio" y sencillo que si se trabaja con datos reales desde el inicio.
