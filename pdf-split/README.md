`split-pdf` corta en fragmentos un archivo PDF con `pdftk`, a partir de un archivo de texto llamado `list.txt` con una lista de nombres y páginas.

#### Instalación:

copiar el script a /usr/bin ó ~/bin


#### Dependencias:

Instalar `pdftk`:

(como root)

    apt-get install pdftk

#### Ayuda

**Uso:**

    split-pdf  <archivo.pdf> [test]

**Opciones:**

`test`: no ejecuta pdftk, sólo muestra el comando.

**Lista a procesar:**

Archivo de texto plano llamado `list.txt` en la misma carpeta donde se esta ejecutando el comando.

Formato:

    Nombre A B
    Nombre A B
    ...
    <una linea vacía al final>

Donde:

 - `Nombre`: el nombre del fragmento (sin espacios).
 - `A`: página donde inicia el recorte.
 - `B`: página donde finaliza el recorte (opcional*).
 - Debe haber una línea vacía al final para que el último ítem sea procesado.

(*) Si no se ingresa `B`, se tomará el valor anterior a la página de inicio del item siguiente.

Lineas vacías, comenzadas con `#` y con `#` después de `B`,  se ignoran.

Ver un ejemplo de `list.txt` [aquí](https://github.com/d-a-l/diybookscanner-derechoaleer/blob/master/pdf-split/list_examples/list.txt)
