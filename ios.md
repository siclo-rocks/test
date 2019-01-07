
# Evaluación



##### 1.-  Considerando  el siguiente `UITableViewCell` constructor: 
```
- (id)initWithStyle:(UITableViewCellStyle)style reuseIdentifier:(NSString *)reuseIdentifier
```
Responde cual es el propósito del `reuseIdentifier`

Reulitlizar celdas de la misma clase. Tal y como dice la documentación: `A string used to identify a cell that is reusable.`

___
##### 2.-  Explica las diferencias entre propiedades sintetizadas, atómicas y no atómicas.

**Sintetizadas**

Crea setters y getters para la propiedad.

**Atómicas**

Asegura la integridad de la propiedad cuando es leida o escrita desde multiples hilos.

**No atómicas**

No asegura la integridad de la propiedad cuando es leida o escrita desde multiples hilos.

___
##### 3.-  Que es URLSession

Es una clase que propociona un API de networking.

___
##### 4.-  Cuales son las diferentes formas en que tu puedes especificar el layout de elementos en una  `UIView`

Autolayout y autoresizing.
___
##### 5.-  Cuales son las diferencias entre WKWebView y UIWebView

API y comportamiento. UIWebView es parte de UIKit, mientras que WKWebView es parte de Webkit. Se puede decir mucho de estas dos clases ya que ambas heredan de UIView pero WKWebView hereda de NSView en MACOS. En fin. La mejor manera de ver las diferencias es hacer un diff de la interfaz.

___
##### 6.-  Considerando el siguiente código
```
#import "TTAppDelegate.h"
@interface TTParent : NSObject
@property (atomic) NSMutableArray *children;
@end

@implementation TTParent
@end

@interface TTChild : NSObject
@property (atomic) TTParent *parent;
@end

@implementation TTChild
@end

@implementation TTAppDelegate

- (BOOL)application:(UIApplication *)application
  didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
    TTParent *parent = [[TTParent alloc] init];
    parent.children = [[NSMutableArray alloc] init];
    for (int i = 0; i < 10; i++) {
        TTChild *child = [[TTChild alloc] init];
        child.parent = parent;
        [parent.children addObject:child];
    }
    return YES;
}
@end
```
Podrías indicar cual es el bug, sus consecuencias  y como arreglarlo?

0. Parent puede ser no-atómico ya que ningun otro thread lo esta llamando. Sólo hace más lento el programa
1. El app delegate no implementa a UIApplicationDelegate. Entonces no se manda a llamar el código.

___
##### 7.-  Que son los blocks y como son usados?

Es un es el conjunto de tipos que representan funciones. Para más info sobre como son utilizados: http://fuckingblocksyntax.com

___
##### 8.-  Cual es la diferencia entre app ID y bundle ID

El App ID contiene al team ID y al bundle ID. El bundle ID identifica a la app en la AppStore y es unico para cada aplicación.

___
##### 9.-  Que mecanismos provee iOS para soportar multi-threading**

Grand Central Dispatch
NSOperation

___
##### 10.-  Explica los diferentes tipos de estado de una aplicacion iOS.

Son los que soporta el Appdelegate.

___
##### 11.-  Por que los patrones de diseño son importantes?

Por que establecen disciplina entre devs y resuelven problemas comunes.

___
##### 12.-  Nombre algunos patrones de diseño y explica en que consiste cada uno de ellos

Bridge:

Se tienen abstracciones e implementaciones intercambiables. Así se reduce la complejidad de escribir N * M implementaciones a N + M

Strategy: 

Es hacer una interfaz y programar hacia ella. Haciendo la implementación intercambiable.

Observable:

Cambiar un objeto y notificar a todos lo que lo observan en una relación uno a muchos.

Notificación, Delegate, Singleton,... y más..

___
##### 13.-  Explica que son los generics en Swift

Paso de tipos dinamicos en clases, estructuras y funciones.

___
##### 15.-  Explica que es la arquitectura VIPER

Es un patron de diseño que divide archivos en las distintas categorias:

View, Contiene elementos visuales
Interactor, Contiene lógica de negocio
Presenter, Contiene la lógica de como se presenta la vista
Entity, Modelos
Router, Contiene la ruta de navegación de la app
___
##### 16.-  Explica como funciona el **Responder Chain** o Cadena de respuesta

Es un composite pattern de vistas y abstracciones de la App para hacer el handling de eventos. Por ejemplo:

Si un botón no hace el handling de un toque, pasa el evento al siguiente elemento de la cadena de respuestas y así sucesivamente hace que se llega al app delegate.

___
##### 15.-  ¿Cuál es la diferencia entre usar un delegate y una notification?

Un delegate es una interfaz.

Notificación es un patrón que la comunicación de eventos muchos a muchos. 

___
##### 17.-  En tus propias palabras explica por que elegiste ser desarrollador de iOS y como hacer para mantenerte actualizado de las ultimas novedades en iOS

Por que me gusta programar. En realidad no me preocupa manternerme actualizado en lo ultimo de iOS. Me preocupa mantenerme actualizado en las herramientas y tecnicas de dessarrollo de software, sin importar el sistema operativo.

