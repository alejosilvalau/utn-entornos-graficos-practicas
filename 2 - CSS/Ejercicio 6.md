# Ejercicio 6

Dado los códigos de los documentos `principal.html` y `estilo2.css`, realizar las modificaciones necesarias en el documento HTML para reemplazar la hoja de estilo interna por la externa `estilo2.css` (sin modificarla) y obtener la misma salida en el navegador.

El documento HTML, con sus respectivas modificaciones para reemplazar la hoja de estilo interna por la externa, quedaría de la siguiente manera:

```html
<!DOCTYPE HTML
  PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3c.org/TR/1999/REC-html401-19991224/loose.dtd">
<HTML lang=es xmlns="http://www.w3.org/1999/xhtml">

<HEAD>
  <TITLE>Página Principal</TITLE>
  <META http-equiv=Content-Type content="text/html; charset=iso-8859-1">
  </META>
  <link rel="stylesheet" href="estilos2.css">
</HEAD>

<BODY>
  <DIV id=encabezado>
    <H1>ASIGNATURA ELECTIVA</H1>
  </DIV>
  <DIV id=contenido>
    <H2>Contenido</H2>
    <p>En esta asignatura ...........................<BR></p>
    <P>El objetivo fundamental ..................</P>
    <P>etc., etc., ...........................................</P>
    <P>etc., etc., ...........................................</P>
    <P>Adem&aacute;s, ...........................................</P>
    <P>etc., etc., ...........................................</P>
    <P class="resaltado">Pero, lo más importante es ..............................</P>
    <P class="resaltado">etc., etc., ...........................................</P>
    <P>Y, entonces, podemos continuar con ..................</P>
    <P>etc., etc., ...........................................</P>
    <P>&nbsp;</P>
  </DIV>
  <DIV id=menu class=navBar>
    <H3>Enlaces</H3>
    <UL>
      <LI><A href="http://www.e-style.com.ar/moodle" target=_blank>Curso Actual</A></LI>
      <LI><A href="http://www.e-style.com.ar/logica" target=_blank>Curso anterior</A></LI>
      <LI><A href="http://www.e-style.com.ar/ntedu/consultas.htm" target=_blank>Contacto</A></LI>
    </UL>
  </DIV>
  <DIV id=pie class="estilopie">Ingeniería en Sistemas de Información - Universidad Tecnológica Nacional Rosario</DIV>
  <p>&nbsp;</p>
</BODY>

</HTML>