haxe-hardware
=============

Simple OpenFL extension for accessing android device hardware methods.

Currently implements methods to use the android vibrator and access screen
dimensions.

Install via `haxelib git haxe-hardware https://github.com/ktravis/haxe-hardware`

Add to `project.xml`:

  <haxelib name="openfl" />
  <haxelib name="haxe-hardware" if="android" />

And import into your project (haxe) with:
  
  import Hardware;

Exposed methods are currently:

  public function vibrate(int duration):Void;
  public function getScreenWidth():Int;
  public function getScreenHeight():Int;

More can be simply added in the java source file, replicating the function and
corresponding `JNI.createStaticMethod(...)` call in `Hardware.hx`.
  
