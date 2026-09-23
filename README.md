# Punto-de-venta---Test

Es un programa que mantiene un registro de ventas e inventario, principalmente enfocado para pequeños negocios.



\[Nombre de tu proyecto]: Punto de venta - Test

\[Qué problema resuelve]: Facilita el control de ventas, registros de inventarios.

\[Para quién]: Negocios que aun usen sus registros de forma manual.





\[Datos que manejará la herramienta]:



\* \*\*Precio de producto / Total de venta:\*\* Tipo Decimal o Entero (centavos). \*Por qué:\* Evita errores de redondeo por coma flotante en transacciones monetarias.

\* \*\*Cantidad en inventario:\*\* Tipo Entero (Int). \*Por qué:\* Representa unidades físicas discretas que no requieren decimales.

\* \*\*Nombre del producto / Código de barras:\*\* Cadena de texto (String). \*Por qué:\* Son caracteres alfanuméricos utilizados para identificación.





\[Datos y estructuras]



=====Dato===== 		 =====Qué guarda===== 		   =====Tipo elegido=====   	     =====Por qué ese y no otro=====

Precio de producto     El costo monetario de un artículo   Decimal (Coma fija)               Evita los errores de redondeo de la coma flotante (float), permitiendo 
                                                                                             operaciones financieras exactas en base 10 sin perder centavos

Inventario             Unidades disponibles en stock       Entero (int)                      Es una cantidad discreta contable; un límite de 32 bits (hasta 2,147,483,647 
                                                                                             previene desbordamiento en el inventario.

Código de barras       Identificador único del producto    Cadena de texto (string)          Son caracteres numéricos/alfanuméricos que no sufren operaciones matemáticas y
                                                                                             pueden contener ceros a la izquierda.

Nombre del producto    Descripción pública del artículo    Cadena de texto (string UTF-8)    Soporta acentos, letras especiales como la 'ñ' y símbolos sin cortar caracteres 
                                                                                             por conteo incorrecto de bytes.

ID de venta            Folio único de cada ticket emitido  Entero grande (int 64-bit / long) Evita problemas de desbordamiento (overflow) cuando el negocio acumule decenas 
                                                                                             de miles de transacciones con el tiempo.



