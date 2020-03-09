# MobX_Notes

## CH2
Observable objects only track the properties provided in the initial value given to observable() or observable.object(). This means if you add new properties later, they will not become observable automatically. This is an important characteristic to remember about observable object.
