# MobX_Notes

## CH2

### Observable
Observable objects only track the properties provided in the initial value given to observable() or observable.object(). This means if you add new properties later, they will not become observable automatically. This is an important characteristic to remember about observable object.

If you do need dynamic tracking of properties, you should consider using observable maps.

The observable() function automatically converts an object, an array, or a map into an observable entity. This automatic conversion is not applied for other types of data—such as JavaScript primitives (number, string, boolean, null, undefined), functions, or for class- instances (objects with prototypes). So, if you call observable(20), it will fail with an error.
