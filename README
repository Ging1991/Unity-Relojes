# Ging1991 Unity Relojes

Librería para Unity que facilita ejecutar acciones dependientes del tiempo.

---

## Conceptos principales

- **Reloj**: objeto global que gestiona ticks de décimas, segundos y minutos.  
- **IEjecutable**: interfaz que define `Ejecutar()`, para acciones que se ejecutan con el tiempo.  
- **AccionPausable**: wrapper para pausar/reanudar una acción sin tocar el reloj.  
- **Repeticion**: ejecuta una acción un número fijo de veces.  
- **Temporizador**: ejecuta una acción una vez o repetidamente después de N ticks.  
- **ContadorDeIteraciones**: notifica a un observador del avance o retroceso de un contador.

---

## Ejemplos

### Contador de segundos
Muestra cómo avanza un contador cada segundo:
```csharp
ContadorDeIteraciones contador = new ContadorDeIteraciones(this, 0, false);
Reloj.GetInstanciaGlobal().segundos.Suscribir(contador);
```
### Temporizador

Muestra un texto después de 5 segundos:
```csharp
Reloj.GetInstanciaGlobal().segundos.Suscribir(new Temporizador(5, this));
```
### Cambio de color gradual

Cambia un objeto de color usando ticks de décimas:
```csharp
Reloj.GetInstanciaGlobal().decimas.Suscribir(this);
```
### Contador pausable

Muestra un contador que se puede pausar con la tecla espacio:
```csharp
accionPausable = new AccionPausable(contador);
Reloj.GetInstanciaGlobal().segundos.Suscribir(accionPausable);
```
## Uso

- Agregar el script Reloj a un GameObject en la escena, o utlizar el Prefab (en cuyo caso debe asegurase de mo cambiarle el nombre.)

- Crear scripts que implementen IEjecutable o IContadorDeIteraciones.

- Suscribir las acciones al reloj global, a uno propio, para que se ejecuten con el tiempo.