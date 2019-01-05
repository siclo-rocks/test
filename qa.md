## QA Evaluation

- Describe que es ser QA para tí

  Rol cuya responsabilidad es diseñar, validar e implementar mecanismos que ayuden al aseguramiento de la calidad de los productos en
  diferentes facetas como pueden ser la eficiencia, seguridad, funcionalidad, entre otras.
  Estos mecanismos pueden ser tecnicas, herramientas, lineamientos, metricas o pruebas.
  
- En una empresa de IT recién creada desde que momento se necesita un QA y por qué

  Desde el momento en que se inicia la concepción de un producto o proyecto, dado que se requiere conocer aspectos de requerimientos y diseño para generar el plan de pruebas y los lineamientos entre otros artefactos.

- Cuales tipos de test hay y explica cada uno de ellos
    
  Pruebas de caja blanca: buscan evaluar que las funcionalidades se comporten correctamente, aprovechando el conocimiento completo de los flujos de ejecución y datos de entrada/salida. 
    
  Pruebas de caja negra:  buscan evaluar que las funcionalidades se comporte conforme a lo especificado verificando  sus entradas y salidas. 
    
  Pruebas unitarias: son del tipo caja blanca y buscan evaluar que una unidad de código (clase) funcione correctamente y conforme a lo especificado de forma individual.
  
  Pruebas de integración: son del tipo caja negra y buscan evaluar que las unidades de código (clases) funcionen
  correctamente en conjunto, se centran principalmente en verificar sus interfaces de entrada y salida. 
  
  Pruebas funcionales: son del tipo caja negra y buscan evaluar que las funcionalidades se comporten conforme a lo especificado. Pueden basarse en los casos de uso o las reglas de negocio.
  
  Pruebas de regresión: son del tipo caja negra y buscan evaluar que las funcionalidades no hayan sido afectadas de forma directa o colateral por cambios recientemente integrados. 
  
  Prueba de humo: son del tipo caja negra y buscan evaluar de forma rápida que las funcionalidades primordiales se conporten conforme a lo especificado. Son un subconjunto de las pruebas funcionales.  
  
  Prueba de aceptación: buscan determinar si los criterios de aceptación de un producto se cumplen a fin de que este , sea aceptado o rechazado por parte del cliente.
    
  Pruebas no funcionales: son del tipo caja negra y buscan evaluar aspectos como la eficiencia, la usabilidad, la portabilidad, seguridad, escalabilidad, entre otros.
  
  Pruebas de carga: buscan medir la capacidad del sistema para continuar funcionando bajo diferentes condiciones de carga (usuarios concurrentes, transacciones, entre otros). 
  
  Pruebas de estrés:   buscan medir la capacidad del sistema para continuar funcionando bajo condiciones excepcionales como la ausencia de recursos o el exceso de la demanda. 
  
  Pruebas de seguridad: buscan verificar el acceso correcto por parte de los actores a las funcionalidades conforme a lo especificado.
  
  Pruebas de usabilidad: buscan determinar si la operación del sistema por parte del usuario es complicada, dificil de usar o tiene problemas para la correcta interacción con el usuario.

- Como decides cuando no debes usar un test automatizado y por que.

  Se decide no usar un test automatizado cuando las acciones a automatizar no son repetibles, debido a que el esfuerzo invertido en implementarla no podrá ser recuperado por las multiples ejecuciones automaticas. En estos casos es mejor realizar pruebas manuales.

  
- Si encuentras un bug en producción y el dev team lo arregla como te aseguras que no volverá a pasar
  Se implementa la verificación de la corrección como una prueba automática y se ejecuta como parte de las pruebas de regresión.

- Explica la diferencia entre Load y stress testing
   las pruebas de carga buscan medir la capacidad del sistema para continuar funcionando bajo diferentes condiciones de carga, las pruebas de stress buscan verificar el comportamiento de sistema en condiciones excepcionales como la ausencia de recursos o el exceso de la demanda

- Explica la  diferencia entre White box and Black box testing

  Las pruebas de caja blanca verifican la funcionalidad con conocimiento de los flujos de ejecución y datos de entrada/salida, mientras que las pruebas de caja negra se basan solo en la varificación de las entradas y las salidas.

- Explica la diferencia entre entre funcional y no funcional testing

Las pruebas funcionales verifican que el sistema se comporte conforme a lo especificado en los casos de uso o reglas de negocio. Las pruebas no funcionales verifican las capacidades y debilidades del software, incluyendo la infraestructura sobre la que se ejecutará. 

- Que herramientas usas para hacer testing en API's y como las usas.
Empleo SoapUI para verificar el funcionamiento y tiempo de respuesta esperado de cada uno de los tipos de peticiones. 

- Si tenemos que migrar un proyecto de un proveedor(AWS) a otro (Azure), que estrategia usarías para asegurarte de que el sitio web funciona bien antes y después de la migración.

Implementaria una suite de pruebas funcionales automaticas con Selenium para verificar el funcionamiento del sitio con el proveedor (AWS), la misma suite de pruebas se utilizaría para verificar que el sitio migrado al proveedor (Azure) funcione correctamente.


- Explica que este TDD y como se debe de usar

TDD es una metodologia en la que las pruebas (unitarias) se escriben primero con base en los requerimientos y luego se escribe el código que deberá pasar las pruebas y repitiendo estos pasos se ira generando el codigo de una aplicación que cumple con los requisitos especificados y validados por las pruebas unitarias mismas.


- Explica que este BDD y como se debe de usar

BDD es una metodologia en la que se define un lenguaje común para el negocio y la parte técnica (Gherkin) con el cual se definen las pruebas de aceptación que pueden ejecutarse de forma automática con base en las historia de usuario y sus criterios de aceptación propios de metodologías ágiles. 
