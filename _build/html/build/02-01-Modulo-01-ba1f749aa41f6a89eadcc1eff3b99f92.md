# Modelo operacional de procesos

## Modelo de entradas y salidas

```{figure} images/02-01-entradas-salidas.png
:label:02-01-entradas-salidas
:width: 40%
:align: center
```

Desde el punto de vista del sistema operativo, un proceso tiene entradas y salidas asignadas al momento de su creación (ver {numref}`Figura %s <02-01-entradas-salidas>`). La entrada de un proceso se llama Entrada Estándar `stdin`. Las salidas que tiene asociado un proceso son dos: a) Salida Estándar `stdout` y b) Salida de errores `stderr`. 

```{figure} images/02-01-files-proc.png
:label:02-01-files-proc
:width: 100%
:align: center
```
## Códigos de término de ejecución

Al terminar (esto es, al llegar a una llamada `exit()`), el proceso informa al sistema operativo el código de terminación. Finalmente, antes de ser creado y cuando es invocado a través, por ejemplo, de una Interfaz de Comandos o  {abbr}`CLI (Command Line Interface)` es posible pasarlas argumentos al proceso.

Los códigos de términación más utilizadas se muestran en la {numref}`Figura %s <02-01-exit-codes>`)

```{figure} images/02-01-exit-codes.png
:label:02-01-exit-codes
:width: 60%
:align: center
```

## Argumentos

Desde el punto de vista del sistema operativo, el código de un proceso tiene un punto de entrada que se debe acceder para se pueda ejecutar. Este punto de entrada es la función main() del código y puede recibir los argumentos que fueron ingresados desde la {abbr}`CLI (Command Line Interface)`.

```
int main(int argc, char* argv[]) {
    // arg0 = argv[0] ...
    ...

    exit(EXIT_SUCCESS);
}
```


## Modelo de funcionamiento general

## Modelo de funcionamiento en Linux

## Creación de procesos


