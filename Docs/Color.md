Color Convenience
=================

### Components

Getting color information from an instance of `UIColor` is as easy as it could possibly be.

**Component Structure**

The following component structures are provided for convenience.  Each one conforms to `Equatable` and a protocol called `ColorComponents`.

```swift
struct RGBComponents {
    let red: CGFloat
    let green: CGFloat
    let blue: CGFloat
    let alpha: CGFloat
}
```

```swift
struct HSBComponents {
    let hue: CGFloat
    let saturation: CGFloat
    let brightness: CGFloat
    let alpha: CGFloat
}
```

```swift
struct GrayscaleComponents {
    let white: CGFloat
    let alpha: CGFloat
}
```

```swift
struct CMYKComponents {
    let cyan: CGFloat
    let magenta: CGFloat
    let yellow: CGFloat
    let key: CGFloat
    let alpha: CGFloat
}
```


Convert component types with these methods:

 - `RGBComponents.asHSBComponents() -> HSBComponents`
 - `RGBComponents.asGrayscaleComponents() -> GrayscaleComponents`
 - `RGBComponents.asCMYKComponents() -> CMYKComponents`
 - `HSBComponents.asRGBComponents() -> RGBComponents`
 - `HSBComponents.asGrayscaleComponents() -> GrayscaleComponents`
 - `HSBComponents.asCMYKComponents() -> CMYKComponents`
 - `GrayscaleComponents.asRGComponents() -> RGBComponents`
 - `GrayscaleComponents.asHSBComponents() -> HSBComponents`
 - `GrayscaleComponents.asCMYKComponents() -> CMYKComponents`
 - `CMYKComponents.asRGBComponents() -> RGBComponents`
 - `CMYKComponents.asHSBComponents() -> HSBComponents`
 - `CMYKComponents.asGrayscaleComponents() -> GrayscaleComponents`


These component structures can be retrieved from an existing color using the following properties:
 - `var rgbComponents: RGBComponents`
 - `var hsbComponents: HSBComponents`
 - `var grayscaleComponents: GrayscaleComponents`
 - `var cmykComponents: CMYKComponents`

Each component scheme also has a method to produce a color:
 - `func color() -> UIColor`

In addition, `UIColor` has a new convenience initializer for creating colors using CMYK values and a component-value retrieval method to match the system API.
 - `init(cyan: CGFloat, magenta: CGFloat, yellow: CGFloat, key: CGFloat, alpha: CGFloat)`
 - `func getCyan(inout cyan: CGFloat, inout magenta: CGFloat, inout yellow: CGFloat, inout key: CGFloat, inout alpha: CGFloat) -> Bool`


**Component Values**

Want individual component values?  Here they are as properties!
 - `var red: CGFloat`
 - `var green: CGFloat`
 - `var blue: CGFloat`
 - `var alpha: CGFloat`
 - `var hue: CGFloat`
 - `var saturation: CGFloat`
 - `var brightness: CGFloat`
 - `var white: CGFloat`
 - `var cyan: CGFloat`
 - `var magenta: CGFloat`
 - `var yellow: CGFloat`
 - `var key: CGFloat`


### Aliases

Use these constant aliases for all of the preset component value methods on `UIColor`:

 - `let Black` is defined as `UIColor.blackColor()`
 - `let White` is defined as `UIColor.whiteColor()`
 - `let Gray` is defined as `UIColor.grayColor()`
 - `let LightGray` is defined as `UIColor.lightGrayColor()`
 - `let DarkGray` is defined as `UIColor.darkGrayColor()`
 - `let Red` is defined as `UIColor.redColor()`
 - `let Green` is defined as `UIColor.greenColor()`
 - `let Blue` is defined as `UIColor.blueColor()`
 - `let Cyan` is defined as `UIColor.cyanColor()`
 - `let Magenta` is defined as `UIColor.magentaColor()`
 - `let Yellow` is defined as `UIColor.yellowColor()`
 - `let Orange` is defined as `UIColor.orangeColor()`
 - `let Purple` is defined as `UIColor.purpleColor()`
 - `let Brown` is defined as `UIColor.brownColor()`
 - `let Clear` is defined as `UIColor.clearColor()`
