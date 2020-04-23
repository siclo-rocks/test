
# Evaluación



##### 1.- ¿Como describirías Android?
##### 2.- ¿Por que Android y no iOS?
##### 3.- ¿En que lenguajes puedo programar para Android?
##### 4.- Da una explicación breve sobre la arquitectura de Android
##### 5.- ¿Qué es ADB y para qué sirve?
##### 6.- ¿Qué es un Activity  y cuales son los métodos que deben de ser implementados en todas las subclases de una Activity?
##### 7.- ¿Cual es el life-cycle de una Android Activity?
##### 8.- ¿Qué es un Intent y cuales son los diferentes tipos de intents?
##### 9.- ¿Qué es DDMS? Describe algunas de sus características
##### 10.- ¿Qué es un ANR?
##### 11.- ¿Qué medidas tomarías para evitar los ANR?
##### 12.- ¿Qué es AAPT?
##### 13.- ¿Qué es DDMS?
##### 14.- ¿Cuál es la diferencia entre Serializable y Parcelable y cual es el mejor enfoque en Android?
##### 15.- ¿Cuáles son los diferentes estados en los que se basa un proceso?
##### 16.- ¿Cual es la diferencia entre Service y IntentService y como se usa cada uno de ello?
##### 17.- ¿Es posible crear un activity sin UI?
##### 18.- ¿Cuales son los diferentes métodos para guardar información en Android?
##### 19.- Describe como está formada una App de Android (Carpetas, Archivos esenciales, configuraciones, etc)
##### 20.- ¿Cuáles son los componentes básicos de android?
##### 21.- ¿Que es un sticky broadcast? Da un ejemplo
##### 22.- ¿Que es AIDL? Cuales sin los tipos de datos soportados por AIDL ?
##### 23.- De las siguientes, ¿Cuál es la forma correcta de verificar si hay un Compass sensor en tu sistema?, Explica por que
a)
```
PackageManager m = getPackageManager();
if (!m.hasSystemFeature(PackageManager.FEATURE_SENSOR_COMPASS)) {
    // This device does not have a compass, turn off the compass feature
}
```

b)
```
SensorManager m = getSensorManager();
if (!m.hasSystemFeature(SensorManager.FEATURE_SENSOR_COMPASS)) {
    // This device does not have a compass, turn off the compass feature
}
```

c)
```
Sensor s = getSensor();
if (!s.hasSystemFeature(Sensor.FEATURE_SENSOR_COMPASS)) {
    // This device does not have a compass, turn off the compass feature
}
```
##### 24.-  Teniendo el siguiente código:
```
Intent sendIntent = new Intent();
sendIntent.setAction(Intent.ACTION_SEND);
sendIntent.putExtra(Intent.EXTRA_TEXT, textMessage);
sendIntent.setType(HTTP.PLAIN_TEXT_TYPE); // "text/plain" MIME type
startActivity(sendIntent);

```
¿Bajo que condiciones la app podría bloquearse?

¿Que modificarías para evitar ese tipo de problemas?

##### 25.- Explica en que son diferentes Implicit y Explicit Intents.
##### 27.- Que es context?
##### 28.- Por qué no podemos ejecutar bytecode en Android?
##### 29.- Describe el funcionamiento de Job Scheduling
##### 30.- Si tu App se bloquea continuamente como lo evitarías?

Gracias
