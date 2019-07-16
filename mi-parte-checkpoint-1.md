# Análisis del QA y QC en la organización
En Softcode, todos los equipos están compuestos por desarrolladores y testers, en una proporción de un tester cada dos desarrolladores. El rol de los testers es muy amplio. Hay algunos testers que tienen una formación más técnica y hay otros que tienen un rol más bien híbrido, con algunas responsabilidades de un analista funcional; y hacen también tests de aceptación: verifican que tenga sentido lo que se desarrolló y lo comparan contra la especificación funcional. Hay poquísimos tests automáticos, con lo cual el papel híbrido orientado al negocio de los testers resulta ser una característica muy importante. También es importante tener en cuenta que el sistema desarrollado tiene pocas reglas de domínio, y estas suelen ser más bien sencillas. Si bien esto último lleva a los desarrolladores a valorar poco los tests automáticos, también vuelve muy caro realizar pruebas de regresión.

Por otro lado, el aseguramiento de la calidad es desigual entre los equipos. Si bien la empresa certifica normas ISO, por diversos motivos el proceso de mejora de la calidad no alcanza a todos los equipos con la misma "intensidad". Los equipos más pequeños o con gente más experimentada siguen el proceso de desarrollo de la empresa casi al pié de la letra. Los más grandes y con menor expertise respetan mucho menos el proceso, y además la empresa hace un esfuerzo menor para que lo sigan más. Este esfuerzo "dispar" respecto del QA por parte de la organización se debe, por un lado, a la diferencia en términos de esfuerzo que implica mejorar el proceso de trabajo de un equipo grande y poco experimentado. También se debe a cuestiones políticas entre los que conforman los líderes de proyecto y el sector de calidad de la empresa.

El resultado de esta situación es que algunos equipos generan entregables de una calidad muy alta, y otros entregan siempre fuera de plazo y tienen mucho retrabajo y ajustes luego de las entregas, con mucho descontento y hostilidad por parte del cliente.
# Análisis de los atributos de calidad del producto

## Revisión
### Mantenibilidad, flexibilidad y testability
Softcode vende muchas horas de mantenimiento y soporte, con lo cual el software que desarrolla está pensado para ser mantenible y modificable. El uso de un lenguaje de programación fuertemente tipado es muy importante para lograrlo, ya que asegura cierto nivel de confiabilidad, coherencia interna y cierta "autodocumentación". Esto "protege" al código de programadores inexpertos, lo cual es muy común en Softcode. Además, trabajar sobre código antíguo sin documentación no sería viable si el lenguaje de programación no fuera fuertemente tipado.

Es importante notar al respecto de esto la falta de tests automatizados. Además es importante aclarar que la calidad del código es muy mala, con muchísimos "smells" muy grandes.

## Transición
### Portability e Interoperability
La decisión tomada respecto de las tecnologías utilizadas es muy buena en este sentido, resolviendo completamente los que respecta a portabilidad. Respecto de la interoperabilidad, la tecnología también es muy buena: a partir de los tipos, se genera automáticamente una interfaz que consumen los servícios externos. Lo mismo se utiliza para los servícios que consume el sistema.
### Reusabilidad
Esto está directamente relacionado a la calidad del código, que es muy mala. Por ejemplo, se escribió el código que hace de interfaz para un servício externo 3 veces, en vez de reusar el código existente (ya que esto era imposible).

## Operación
### Usabilidad
Varía mucho debido a la historia de los proyectos: algo que pasa en muchos es que, debido a que el crecimiento se da de formas inesperadas, la interfaz debe cumplir requisitos que el equipo de UX no había previsto, con lo cual se pierde consistencia y la calidad de la experiencia de usuario.
### Correctness
La correctitud respecto de los requerimientos formalizados suele ser buena, aunque los clientes suelen mostrarse disconformes.
### Confiabilidad y eficiencia
Estos aspectos son más relativos a la arquitectura y a la tecnología utilizada. Estas son decisiones que toma poca gente que tiene muchos conocimientos, con lo cual es totalmente acertada.

