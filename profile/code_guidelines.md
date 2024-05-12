# Code Guidelines 📖

El propósito de este documento es normalizar el desarrollo del equipo. De esta manera se realiza un trabajo consistente y que sigue los standares y buenas prácticas de la industria.

### Indice 

* [Python](https://github.com/trabajo-profesional-fiuba/.github/blob/main/profile/code_guidelines.md#python)
* [REST API](https://github.com/trabajo-profesional-fiuba/.github/blob/main/profile/code_guidelines.md#rest-api-)
* [Github](https://github.com/trabajo-profesional-fiuba/.github/blob/main/profile/code_guidelines.md#github)

## Python

Se seguirá un standard [PEP8](https://peps.python.org/pep-0008/) para el desarrollo en python. Este convencion posee algunas caracteristicas, por ejemplo:

```python
# Correct:

# Aligned with opening delimiter.
foo = long_function_name(var_one, var_two,
                         var_three, var_four)

# Add 4 spaces (an extra level of indentation) to distinguish arguments from the rest.
def long_function_name(
        var_one, var_two, var_three,
        var_four):
    print(var_one)

# Hanging indents should add a level.
foo = long_function_name(
    var_one, var_two,
    var_three, var_four)

# Wrong:

# Arguments on first line forbidden when not using vertical alignment.
foo = long_function_name(var_one, var_two,
    var_three, var_four)

# Further indentation required as indentation is not distinguishable.
def long_function_name(
    var_one, var_two, var_three,
    var_four):
    print(var_one)
```

Para cumplir con **pep8** cada repositorio tendrá un linter [flake8](https://flake8.pycqa.org/en/latest/user/index.html#) de manera que cada desarrollador se evite el tedioso trabajo de formatear el documento a mano.

Para la correccion automatica se utilizara [Black](https://pypi.org/project/black/).

### Variables & Clases

Se utilizará para las variables y funciones `snake_case` 🐍

```python
def my_function() 👌

def myFunction() ❌

def MyFunction() ❌
```

Se utilizará para las clases `PascalCase`

```python
class MyClass 👌
```

### Espacios y Tabs

Entra cada funcion se espera 1 espacio y se utilizaran como identacion un tab

## Rest API 📚

Se espera para el desarrollo de la API las siguientes buenas prácticas

### Requests

| Método | Descripción                                                 |
| ------ | ----------------------------------------------------------- |
| GET    | Se utiliza para recuperar una representación de un recurso. |
| POST   | Se utiliza para crear nuevos recursos y subrecursos.        |
| PUT    | Se utiliza para actualizar recursos existentes.             |
| PATCH  | Se utiliza para actualizar recursos existentes.             |
| DELETE | Se utiliza para eliminar recursos existentes.               |

### Responses 📣

| Código de Estado          | Descripción                                                                                                                                                 |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400 Bad Request           | Esto significa que la entrada del cliente no supera la validación.                                                                                          |
| 401 Unauthorized          | Esto significa que el usuario no está autorizado para acceder a un recurso. Generalmente se devuelve cuando el usuario no está autenticado.                 |
| 403 Forbidden             | Esto significa que el usuario está autenticado, pero no tiene permitido acceder a un recurso.                                                               |
| 404 Not Found             | Esto indica que no se encontró un recurso.                                                                                                                  |
| 500 Internal Server Error | Este es un error genérico del servidor. Probablemente no debería ser lanzado explícitamente.                                                                |
| 502 Bad Gateway           | Esto indica una respuesta no válida de un servidor ascendente.                                                                                              |
| 503 Service Unavailable   | Esto indica que ocurrió algo inesperado en el servidor (puede ser cualquier cosa, como sobrecarga del servidor, falla de algunas partes del sistema, etc.). |

### Versionado 🔢

Deberíamos tener diferentes versiones de la API si realizamos cambios en ellas que puedan romper la compatibilidad con los clientes. La versión se puede hacer de acuerdo con la versión semántica (por ejemplo, 2.0.6 para indicar la versión principal 2 y el sexto parche), como hacen la mayoría de las aplicaciones en la actualidad.

Ejemplo de endpoint `GET /v1/people`

### Middleware y seguridad 🔒

Se recomienda un buen uso consciente de middleware al igual que definir que endpoints necesitan hacer uso de `authentication & authorization`

## Github

A continuacion se describen algunos guidelines para poder trabajar en conjunto consistentemente

- Para los commits se utilizarán [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/)
- Cada ticket tiene su feature branch donde luego al commitear a master se hara un `squash and merge` para que la historia quede limpia
- Se recomienda que cada feature branch debe llamarse `feat/repo-numero`, por ejemplo `feat/assigment-2`
- Cada PR tiene que tener al menos un Approve y debe tener los builds en verde para que se mergee a `main`
- POR FAVOR NO USAR `--force` en los rebase sino `--force-with-lease` 
