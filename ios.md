
# Evaluación



##### 1.-  Considerando  el siguiente `UITableViewCell` constructor: 
```
- (id)initWithStyle:(UITableViewCellStyle)style reuseIdentifier:(NSString *)reuseIdentifier
```
Responde cual es el propósito del `reuseIdentifier`

R: Se usa para identificar la celda que se mostrará en la vista a la hora de ejecutarse la app, para eso se hace uso de UITableViewCell, para eso de debe hacer un registro de el en el viewcontroller donde se estará usando, instanciando el UINib de la celda creada en un Xib, o bien hacerlo de una manera más gráfica mediante los Storyboards.

___
##### 2.-  Explica las diferencias entre propiedades sintetizadas atómicas y no atómicas.

R. Estos términos son más comunes escucharlos en Objective-C, atomic garantiza un valor de retorno, aunque esto significa que su rendimiento es menor ya que cuando una propiedad es declarada con atomic a la hora de querer consultar el valor de esta propiedad a partir de otro proceso, este otro debe esperar a que atomic tenga un valor. caso contrario con nonatomic, que es considerado más rápido, sin embargo a la hora de consultar el valor de la propiedad que tenga nonatomic a traves de subprocesos estos valores pueden retornar otras cosas que las deseadas.

___
##### 3.-  Que es  URLSession

R. Es la herramienta que se usa para poder configurar mediante código todo un entorno para el consumo de servicios web.
___
#####  4.-Cuales son las  diferentes formas en que tu puedes especificar el layout de elementos en una  `UIView`

R. ¿?
___
##### 5.-  Cuales son las diferencias entre WKWebView y UIWebView

R. Hacen las mismas funciones de embeber contenido HTML en la app, UIWebView ya es deprecated y pertenece al framework UIKit. WKWebView pertenece ahora a WebKit. 

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

R. ¿?

___
##### 7.- Que son los blocks y como son usados?

R. son estructuras de codigo que tienen la funcion de agregar una action como complemento a un método que ya ha sido ejecutado o en ejecución.
___
##### 8.- Cual es la diferencia entre app ID y bundle ID

R. App ID es asignado en App Store Connect a la hora de que se configura la app para ser publicada en la App Store, Bundle ID es el identificador único de la applicación.

___
##### 9.-  Que mecanismos provee iOS para soportar multi-threading**

R. Grand Central Dispatch, NSOperationQueue, NSThread
___
##### 10.-  Explica los diferentes tipos de estado de una aplicacion iOS.

R. 
- Background: Es cuando la aplicacion se ha pasado a segundo plano una vez que el usuario ha presionado el botón home del dispositivo.
- Foreground: Cuando la aplicación regresa a ser activada a primer plano.
- Finish: cuando la aplicación ha sido terminado su proceso ya sea por el usuario o por el sistema operativo.
- Not Running: La app simplemente no ha sido ejecutada.

___
##### 11.- Por que los patrones de diseño son importantes?

R. Ayudan a estructurar el código y a que no sea tan repetitivo, algunos patrones de diseño ayudan para el unit test, además de que se tiene un código más controlado que ayuda a ser más entendible como escalable.
___
##### 12.- Nombre algunos patrones de diseño y explica en que consiste cada uno de ellos

R.
- Singleton: Es un objeto compartido en toda la ejecución de la app, y solo es instanciado una sola vez.
- Factory: Su principal función es ejecutar acciones o funciones sin tener que instanciar un objeto.
- Observable: sirve para notificar en otra estructura de código la ejecución de alguna acción.
- Delegados: su pricipal función es implementar funciones un objeto a otro.
___
##### 13.- Explica que son los generics en Swift

R. Son tecnicas que se usa en Swift para poder escribir funciones que puedan ser reusables.

___
##### 15.- Explica que es la arquitectura VIPER

- VIPER (View - Interactor - Presenter - Entity - Router)
· View: Tendrá la responsabilidad de iniciar la parte gráfica que se mostrará al usuario asi como iniciar los custom controls, este solo tiene comunicación con el Presenter.
· Presenter: Contiene una serie de instrucciones y es el encargado del modelo de negocio. Este tiene comunicación con el Router sin respuesta, tambien se comunica con el Interactor.
· Interactor: Este es el encargado de las peticiones para obtener datos, ya sea mediante servicios web o de forma local mediante una base de datos (por ejemplo Core Data), a la hora de obtener estos datos son transformados en objetos.
· Router: Su principal funcion es iniciar el todos los features anteriores y relacionarlos entre si. Pero también es ecargado de iniciar la navegacion entre modulos (o pantallas).
· Entity: Representa a un objeto de los datos que son obtenidos en el Interactor, es encargado de realizar serie de operaciones para retornar datos más especificos.
___
##### 16.- Explica como funciona el **Responder Chain** o Cadena de respuesta

R. Consiste en como el UIApplication recibirá eventos a partir de un UIControl de UIKit, y este pasará a UIView que este en el SuperView del ViewController, el evento pasara al UIWindow asi hasta finalizar al UIAplication. Esto permite que la app tenga comunicación con el sistema, por ejemplo el UIResponse que se da cuando es activado un UITextfield para poder mostrar el Teclado.

___
##### 15.- ¿Cuál es la diferencia entre usar un delegate y una notification?

R. Delegate es necesario que el objeto que se le ha implementado ciertas responsabilidades a otro objeto esten ejecutandose al mismo tiempo. Con notification solo se manda la orden de ejecución de la acción sin necesidad de que este ya en memoria.   

___
##### 17.- En tus propias palabras explica por que elegiste ser desarrollador de iOS y como hacer para mantenerte actualizado de las ultimas novedades en iOS

R. Inicie a desarrollar apps en iOS por que tengo un gusto por los dispositivos Apple, al adquirir mi primer iPhone 3G quede sorprendido de la calidad de graficos que se mostraban en las aplicaciones asi como la ayuda que comenzaba a tener esas en la vida real. Fue asi como ahorre e inverti en una MacBook Pro 2011 e inicie a tomar cursos y a leer respecto a los nuevos features de los iPhone y en ese tiempo en como desarrollar con Objective-C. Para mantenerme actualizado, normalmente leo foros respecto a las novedades que tendra tanto dispositivos como en el sistema operativo, en el desarrollo por lo regular veo a veces el codigo de otros desarrolladores intentando aprender nuevas tecnicas para mejorar el codigo, tambien leo algunos articulos relacionados a Swift que tenga que ver con nuevos features con Swift.

