## Descripción
Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
## Solución
Revisé los metadatos del archivo y encontré:
```
Creator                         : Word
Producer                        : macOS Version 11.4 (Build 20F71) Quartz PDFContext
Title                           : Microsoft Word - Financial Report for ABC Labs.docx

```
lo que indica que fue escrito en word y que se usó Quartz PDFContext para pasarlo a pdf, pero al ser un programa simple, no tacha la información sensible, si no que oculta con una caja negra encima del texto y al pasar el ratón por encima de esa caja encontré la llave:
```
picoCTF{C4n_Y0u_S33_m3_fully}
```
## Notas
## Referencias
