# Otras herramientas para el manejo de errores en programación

## Introducción

En programación pueden presentarse errores que afectan el funcionamiento de un programa. Algunos ocurren por datos incorrectos, otros por problemas durante la ejecución y algunos por situaciones que no fueron previstas al desarrollar el código.

Para evitar que estos problemas provoquen que un programa se cierre inesperadamente, existen diferentes herramientas que ayudan a detectar, controlar, registrar y corregir errores.

En este reporte se investigan algunas herramientas de Python que complementan el manejo de errores y excepciones visto en clase.


## 1. Logging (registro de eventos)

`logging` es una herramienta integrada en Python que permite registrar los eventos que ocurren durante la ejecución de un programa. Ayuda a identificar problemas y conocer qué sucedió antes, durante o después de un error.

Tiene diferentes niveles de registro:

- **DEBUG:** muestra información detallada para revisar el funcionamiento del programa.
- **INFO:** informa que el programa está funcionando correctamente.
- **WARNING:** advierte sobre una situación que podría causar un problema.
- **ERROR:** registra un error que impide realizar alguna operación.
- **CRITICAL:** indica un problema grave que puede afectar el funcionamiento del programa.

**Ejemplo en Python:**

```python
import logging

logging.basicConfig(level=logging.INFO)

try:
    resultado = 10 / 0
except ZeroDivisionError:
    logging.error("No se puede dividir entre cero")
```

**Ventaja:** permite guardar registros de los errores y facilita encontrar las causas de los problemas sin tener que revisar todo el programa manualmente.


## 2. Warnings (advertencias)

`warnings` es un módulo integrado en Python que permite mostrar mensajes de advertencia cuando se detectan situaciones que podrían causar problemas en el futuro. A diferencia de las excepciones, las advertencias normalmente no detienen la ejecución del programa.

Se utiliza para informar al programador sobre prácticas que podrían ser incorrectas, funciones que dejarán de utilizarse o situaciones que necesitan atención.

**Ejemplo en Python:**

```python
import warnings

edad = -5

if edad < 0:
    warnings.warn("La edad no puede ser negativa", UserWarning)

print("El programa continúa ejecutándose")
```

**Ventaja:** permite detectar posibles problemas antes de que se conviertan en errores más graves, sin interrumpir necesariamente el programa.


## 3. Assert (comprobación de condiciones)

`assert` es una instrucción de Python que permite verificar si una condición es verdadera. Si la condición no se cumple, el programa genera un error llamado `AssertionError`.

Se utiliza para comprobar que los valores y resultados de un programa sean los esperados durante el desarrollo.

**Ejemplo en Python:**

```python
numero = 10

assert numero > 0, "El número debe ser positivo"

print("La comprobación fue correcta")
```

En este ejemplo, Python verifica que el número sea mayor que cero. Si la condición es falsa, muestra el mensaje indicado.

**Ventaja:** ayuda a encontrar errores en las condiciones y en los resultados del programa durante su desarrollo.

**Nota:** `assert` no debe utilizarse como sustituto de la validación de datos ingresados por los usuarios, porque las comprobaciones pueden desactivarse al ejecutar Python con ciertas opciones.


## 4. Traceback (rastreo de errores)

`traceback` es un módulo integrado en Python que permite obtener información detallada sobre los errores que ocurren durante la ejecución de un programa.

Muestra la secuencia de llamadas a funciones que llevó al error, así como el archivo y la línea donde ocurrió. Esto facilita encontrar y corregir el problema.

**Ejemplo en Python:**

```python
import traceback

try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("Se produjo un error:")
    traceback.print_exc()
```

En este ejemplo, cuando ocurre una división entre cero, `traceback` muestra los detalles del error y ayuda a identificar dónde sucedió.

**Ventaja:** facilita la depuración porque proporciona información sobre el origen del error y las instrucciones que se ejecutaron antes de que ocurriera.


## 5. Excepciones personalizadas

Las excepciones personalizadas son errores creados por el programador para representar situaciones específicas que pueden ocurrir en una aplicación.

En Python se pueden crear mediante clases que heredan de `Exception`. Después, pueden utilizarse con las instrucciones `raise`, `try` y `except` para controlar esos errores.

**Ejemplo en Python:**

```python
class EdadInvalidaError(Exception):
    pass

edad = -3

try:
    if edad < 0:
        raise EdadInvalidaError("La edad no puede ser negativa")

    print("Edad válida")

except EdadInvalidaError as error:
    print("Error:", error)
```

En este ejemplo se crea una excepción llamada `EdadInvalidaError`. Cuando la edad es negativa, el programa genera ese error y lo controla mediante `except`.

**Ventaja:** permite identificar y controlar situaciones particulares de cada programa, haciendo que el código sea más claro y fácil de mantener.


## Conclusión

Existen diferentes herramientas en Python que ayudan a prevenir, identificar y controlar los errores durante la ejecución de un programa. `logging` permite registrar eventos, `warnings` muestra advertencias, `assert` comprueba condiciones, `traceback` facilita localizar el origen de los errores y las excepciones personalizadas permiten controlar situaciones específicas.

Estas herramientas complementan el uso de `try` y `except`, ya que ayudan a desarrollar programas más seguros, organizados y fáciles de mantener. Conocerlas permite detectar problemas con mayor facilidad y mejorar la calidad del código.


## Fuentes de consulta

La información de este reporte se consultó en la documentación oficial de Python:

1. Python Software Foundation. [Logging — Registro de eventos](https://docs.python.org/3/howto/logging.html).
2. Python Software Foundation. [Warnings — Control de advertencias](https://docs.python.org/es/3/library/warnings.html).
3. Python Software Foundation. [Assert — Instrucciones simples](https://docs.python.org/3/reference/simple_stmts.html#the-assert-statement).
4. Python Software Foundation. [Traceback — Rastreo de errores](https://docs.python.org/3/library/traceback.html).
5. Python Software Foundation. [Errors and Exceptions — Errores y excepciones](https://docs.python.org/3/tutorial/errors.html).
