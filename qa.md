## QA Evaluation

- Describe que es ser QA para tí
  Es ser responsable de que los sistemas se encuentren funcionando de acuerdo a los requerimientos y especificaciones del cliente.
- En una empresa de IT recién creada desde que momento se necesita un QA y por qué
  Desde el principio, para ir planeadndo las actividades y creando documentación, después ir probando lo que se va liberando y terminar   automatizando lo que ya está estable.
- Cuales tipos de test hay y explica cada uno de ellos
  Unitarios - prueba de código y funcional, Integración - que todo se integre adecuadamente, Sistema - pruebas en base a requerimientos, Sanidad - validar si pruebas más complejas valen la pena, Humo - validar que no hayan problemas mayores, Regresión - pruebas completas, UAT - pruebas de aceptación por el usuario. Entre otras.
- Como decides cuando no debes usar un test automatizado y por que.
  Pues si la tecnología no lo permite o son pruebas qus solo un humano las podría realizar.
- Si encuentras un bug en producción y el dev team lo arregla como te aseguras que no volverá a pasar
  Agregando casos de uso en las suites de regression y marcándolo como prioritario.
- Explica la diferencia entre Load y stress testing
  Load Testing prueba bajo condiciones esperadas y Stress Testing prueba bajo condiciones extremas para ver cuanto soporta el sistema.
- Explica la  diferencia entre White box and Black box testing
  White Box ser'ia probar código con pruebas unitarias y Black Box es probar la funcionalidad del sistema.
- Explica la diferencia entre entre funcional y no funcional testing
  Funcional testing es probar todo lo que esta descrito en los requerimientos y no funcional son pruebas adicionales como configuración, carga, estrés, escalabilidad entre otros.
- Que herramientas usas para hacer testing en API's y como las usas.
  Para pruebas funcionales usaría Postman y si se rreuiere un esfuerzo continuo y o automatizado dependiendo de la tecnología usaría Rest     Assured o Soap UI.
- Si tenemos que migrar un proyecto de un proveedor(AWS) a otro (Azure), que estrategia usarías para asegurarte de que el sitio web funciona bien antes y después de la migración.
  Verificar la compatibilidad del código existente, tener el espacio en la nuve ya configurado, hacer la migración, hacer pruebas, redirigir una parte del tráfico y migrar compleetamente.
- Explica que este TDD y como se debe de usar
  Es un ciclo de desarrollo corto que incluye crear una prueba de código que se desea implementar, la cual va a fallar, crear esa función con el minimo código requerido y luego refactorizar esa función en base a los estándares establecidos.
- Explica que este BDD y como se debe de usar
  Es escribir las puebas en el lenguaje común. YU se aplica creando Historias de usuario concretas, cada uno debe ser un esceneario de usuario valido, entender el rol-requerimiento- razón, y el dado que- cuando y escibir la especificación del comportamiento de la clase.
