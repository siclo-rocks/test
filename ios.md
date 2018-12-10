
# Evaluación



##### 1.-  Considerando  el siguiente `UITableViewCell` constructor: 
```
- (id)initWithStyle:(UITableViewCellStyle)style reuseIdentifier:(NSString *)reuseIdentifier
```
Responde cual es el propósito del `reuseIdentifier`
___
##### 2.-  Explica las diferencias entre propiedades sintetizadas atómicas y no atómicas.
___
##### 3.-  Que es  URLSession
___
#####  4.-Cuales son las  diferentes formas en que tu puedes especificar el layout de elementos en una  `UIView`
___
##### 5.-  Cuales son las diferencias entre WKWebView y UIWebView
___
##### 6.- Considerando el siguiente código
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
___
##### 7.- Que son los blocks y como son usados?

___
##### 8.- Cual es la diferencia entre app ID y bundle ID

___
##### 9.-  Que mecanismos provee iOS para soportar multi-threading**

___
##### 10.-  Explica los diferentes tipos de estado de una aplicacion iOS.

___
##### 11.- Por que los patrones de diseño son importantes?

___
##### 12.- Nombre algunos patrones de diseño y explica en que consiste cada uno de ellos
___
##### 13.- Explica que son los generics en Swift
___
##### 15.- Explica que es la arquitectura VIPER
___
##### 16.- Explica como funciona el **Responder Chain** o Cadena de respuesta
___
##### 15.- ¿Cuál es la diferencia entre usar un delegate y una notification?
___
##### 17.- En tus propias palabras explica por que elegiste ser desarrollador de iOS y como hacer para mantenerte actualizado de las ultimas novedades en iOS
