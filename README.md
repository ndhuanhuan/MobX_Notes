# MobX_Notes

## CH2

### Observable
Observable objects only track the properties provided in the initial value given to observable() or observable.object(). This means if you add new properties later, they will not become observable automatically. This is an important characteristic to remember about observable object.

If you do need dynamic tracking of properties, you should consider using observable maps.

The observable() function automatically converts an object, an array, or a map into an observable entity. This automatic conversion is not applied for other types of data—such as JavaScript primitives (number, string, boolean, null, undefined), functions, or for class- instances (objects with prototypes). So, if you call observable(20), it will fail with an error.

We have to use the more specialized observable.box() to convert primitive values into an observable. Observables that wrap primitives, functions, or class-instances are called boxed observables.

objects	observable.object({ })
arrays	observable.array([ ])
maps	observable.map(value)
primitives, functions, class-instances	observable.box(value)


Observable maps are great for tracking dynamic changes to the keys and values. This is in stark contrast to observable objects, which do not track properties that are added after creation.

#### The computed observable(Computed properties, also known as derivations)
We can define a computed description property by simply adding a get-property to the cart observable. It will derive its value from items.length. 
