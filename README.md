haxe-hardware
=============

Simple OpenFL extension for accessing android device hardware methods.

Currently implements methods to use the android vibrator and access screen
dimensions.

Install Lime via `haxelib install lime`

Install via `haxelib git haxe-hardware https://github.com/ktravis/haxe-hardware`

Add to `project.xml`:

    <haxelib name="openfl" />
    <haxelib name="haxe-hardware" if="android" />

And import into your project (haxe) with:
  
    import Hardware;

Exposed methods are currently:

    public static function vibrate(int duration):Void;
    public static function getScreenWidth():Int;
    public static function getScreenHeight():Int;
    public static function wakeUp():Void;

More can be simply added in the java source file, replicating the function and
corresponding `JNI.createStaticMethod(...)` call in `Hardware.hx`.
  
### Contributions

Thank you to [alagator](https://github.com/alagatar) for contributing `wakeUp()`!
