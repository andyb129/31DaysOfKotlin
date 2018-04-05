# 31 Days Of Kotlin 

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/android_tools.png" height="100">&nbsp;&nbsp;&nbsp;&nbsp;
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/kotlin_logo.png" width="375" height="95" alt="kotlin logo"/>
</p>

A summary of all the kotlin tips from Google's [Android Developer Twitter account](https://twitter.com/AndroidDev)

A Twitter Moment summary of all the tweets are here -> [https://twitter.com/i/moments/980488782406303744](https://twitter.com/i/moments/980488782406303744) 

### TODO

1. Add code samples in this repo for all 31 days 
2. Create an app for quick reference 
3. Create ref app in the Play Store

### Contents

##### [Day 1 - let, apply, with and run](#day1)
##### [Day 2 - KTX view padding](#day2)
##### [Day 3 - Parcelable](#day3)
##### [Day 4 - Spans](#day4)
##### [Day 5 - Lambdas](#day5)
##### [Day 6 - Bundles](#day6)
##### [Day 7 - Type safe builders](#day7)
##### [Day 8 - KTX Content Values](#day8)
##### [Day 9 - KTX iterators for ViewGroup & SparseArray](#day9)
##### [Day 10 - Basic syntax](#day10)
##### [Day 11 - Operator overload](#day11)
##### [Day 12 - Sequence](#day12)
##### [Day 13 - KTX Graphics](#day13)
##### [Day 14 - Extension functions](#day14)
##### [Day 15 - By](#day15)
##### [Day 16 - KTX reified](#day16)
##### [Day 17 - @JvmName](#day17)
##### [Day 18 - inline](#day18)
##### [Day 19 - require](#day19)
##### [Day 20 - latinit](#day20)
##### [Day 21 - lazy](#day21)
##### [Day 22 - sealed classes](#day22)
##### [Day 23 - default parameters](#day23)
##### [Day 24 - access modifiers](#day24)
##### [Day 25 - data classes](#day25)
##### [Day 26 - properties](#day26)
##### [Day 27 - ranges](#day27)
##### [Day 28 - when statement](#day28)
##### [Day 29 - KTX destructuring](#day29)
##### [Day 30 - string templates](#day30)
##### [Day 31 - elvis operator](#day31)

----

<a name="day1"></a>

#### Day 1 - let, apply, with and run

Let’s run with some standard Kotlin functions! Short and powerful, `let`, `apply`, `with` and `run` all have a receiver (this), may have an argument (it) and may have a return value. See the differences

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day1a.png" width="512" height="287" alt="day1a"/>
<br>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day1b.png" width="512" height="287" alt="day1b"/>
<br>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day1c.png" width="512" height="287" alt="day1c"/>
<br>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day1d.png" width="512" height="287" alt="day1d"/>
</p>

<a name="day2"></a>

#### Day 2 - KTX view padding

Extending existing APIs with default arguments usually makes everyone happy. Android KTX lets you set the padding on one side of a view using default parameters. 

A one line function that saves so much code!

Code: [https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/view/View.kt#L117](https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/view/View.kt#L117)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day2.png" width="512" height="287" alt="day2"/>
</p>

<a name="day3"></a>

#### Day 3 - Parcelable

Love the speed of Parcelable, but don’t like writing all that code? Say hello to Parcelize

Spec: [https://github.com/Kotlin/KEEP/blob/master/proposals/extensions/android-parcelable.md](https://github.com/Kotlin/KEEP/blob/master/proposals/extensions/android-parcelable.md)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day3.png" width="512" height="287" alt="day3"/>
</p>

<a name="day4"></a>

#### Day 4 - Spans

Powerful but hard to use - that’s how the text styling Spans API feels. 
Android KTX adds extension functions for some of the most common spans and makes the API easier to use

Android KTX: [https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/text/SpannableStringBuilder.kt](https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/text/SpannableStringBuilder.kt)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day4.png" width="512" height="287" alt="day4"/>
</p>

<a name="day5"></a>

#### Day 5 - Lambdas

Lambdas are sweet. With last parameter call syntax, you can cleanup callbacks, Callable, and Runnable.

For example, Android KTX sweetens `postDelayed` with a small wrapper.

Docs: [https://kotlinlang.org/docs/reference/lambdas.html](https://kotlinlang.org/docs/reference/lambdas.html)
Android KTX: [https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/os/Handler.kt#L38](https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/os/Handler.kt#L38)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day5.png" width="512" height="287" alt="day5"/>
</p>

<a name="day6"></a>

#### Day 6 - Bundles

Bundle up, and get ready for the concise bundle creator in Android KTX. No more calls to `putString`, `putInt`, or any of their 20 friends.

One call will make you a new bundle, and it’ll even handle Arrays!

Code: [https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/os/Bundle.kt#L27](https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/os/Bundle.kt#L27)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day6.png" width="512" height="287" alt="day6"/>
</p>

<a name="day7"></a>

#### Day 7 - Type safe builders

[1/4] Specifically terrific? Domain specific languages can be made by using type safe builders. They make for clean APIs; and you can build them yourself too.

Extension Lambdas: https://kotlinlang.org/docs/reference/lambdas.html#function-literals-with-receiver
Type Safe Builders: https://kotlinlang.org/docs/reference/type-safe-builders.html

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day7.png" width="512" height="287" alt="day7"/>
</p>

<a name="day8"></a>

#### Day 8 - KTX Content Values

Combine the power of Content Values with the brevity of Kotlin. Use the Android KTX Content Values creator and just pass a Pair<StringKey, Value>.

Android KTX: [https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/content/ContentValues.kt#L21](https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/content/ContentValues.kt#L21)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day8.png" width="512" height="287" alt="day8"/>
</p>

<a name="day9"></a>

#### Day 9 - KTX iterators for ViewGroup & SparseArray

Iterators in interesting places? Android KTX adds iterators to ViewGroup and SparseArray

To define iterator extensions use the `operator` keyword. Foreach loops will use the extensions!

Docs: [https://kotlinlang.org/docs/reference/control-flow.html#for-loops](https://kotlinlang.org/docs/reference/control-flow.html#for-loops)
Android KTX: [https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/view/ViewGroup.kt#L66](https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/view/ViewGroup.kt#L66)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day9.png" width="512" height="287" alt="day9"/>
</p>

<a name="day10"></a>

#### Day 10 - Basic syntax

[1/2] Utility methods for a class? Add them to the top level of the source file. In Java, they are compiled as static methods of that class. 

Doc: [https://kotlinlang.org/docs/reference/basic-syntax.html](https://kotlinlang.org/docs/reference/basic-syntax.html)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day10.png" width="512" height="287" alt="day10"/>
</p>

<a name="day11"></a>

#### Day 11 - Operator overload

Write Kotlin (time * 2) faster with operator overloading. Objects like Path, Range or SpannableStrings naturally allow for operations like addition or subtraction. With Kotlin, you can implement your own operators

[https://goo.gl/EGipGz](https://goo.gl/EGipGz)
[https://goo.gl/iy8tZ9](https://goo.gl/iy8tZ9) 

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day11.png" width="512" height="287" alt="day11"/>
</p>

<a name="day12"></a>

#### Day 12 - Sequence

[1/2] Sequences are lists that never existed. A Sequence is a cousin of Iterator, lazily generating one value at a time. This matters when using map and filter - they’ll create Sequences instead of copying the list for every step!

Docs: [https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/index.html](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.sequences/index.html)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day12.png" width="512" height="287" alt="day12"/>
</p>

<a name="day13"></a>

#### Day 13 - KTX Graphics

If you ever converted a Drawable to a Bitmap then you know how much boilerplate you need. 

Android KTX has a great set of functions to make your code more concise when working with classes from the graphics package:

[https://github.com/android/android-ktx/tree/master/src/main/java/androidx/core/graphics/drawable](https://github.com/android/android-ktx/tree/master/src/main/java/androidx/core/graphics/drawable)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day13.png" width="512" height="287" alt="day13"/>
</p>

<a name="day14"></a>

#### Day 14 - Extension functions

[1/2] No more Util classes! Extend the functionality of a class by using `extension functions`. Put the name of the class you’re extending before the name of the method you’re adding.

Doc: [https://kotlinlang.org/docs/reference/extensions.html#extension-functions](https://kotlinlang.org/docs/reference/extensions.html#extension-functions)

Example: [https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/net/Uri.kt#L28](https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/net/Uri.kt#L28)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day14.png" width="512" height="287" alt="day14"/>
</p>

<a name="day15"></a>

#### Day 15 - By

Delegate your work to another class with `by`. Favor composition over inheritance with class delegation and reuse property accessor logic with delegator properties.

Delegation: [https://kotlinlang.org/docs/reference/delegation.html](https://kotlinlang.org/docs/reference/delegation.html)

Delegated properties: [http://kotlinlang.org/docs/reference/delegated-properties.html](http://kotlinlang.org/docs/reference/delegated-properties.html)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day15.png" width="512" height="287" alt="day15"/>
</p>

<a name="day16"></a>

#### Day 16 - KTX reified

To make the concept of reified concrete an example is in order: `Context.systemService()` in Android KTX uses reified to pass a "real" type via generics. No more passing classes to getSystemService! [https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/content/Context.kt#L37](https://github.com/android/android-ktx/blob/master/src/main/java/androidx/core/content/Context.kt#L37)

Docs: [https://kotlinlang.org/docs/reference/inline-functions.html#reified-type-parameters](https://kotlinlang.org/docs/reference/inline-functions.html#reified-type-parameters)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day16.png" width="512" height="287" alt="day16"/>
</p>

<a name="day17"></a>

#### Day 17 - @JvmName

Using Kotlin and Java in the same project? Do you have classes with top-level functions or properties? 

By default, the compiler generates the class name as “YourFileKt”. Change it by annotating the file with `@file:JvmName(“...“)`.

Doc: [https://kotlinlang.org/docs/reference/java-to-kotlin-interop.html#package-level-functions](https://kotlinlang.org/docs/reference/java-to-kotlin-interop.html#package-level-functions)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day17a.png" width="512" height="287" alt="day17a"/>
<br>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day17b.png" width="512" height="287" alt="day17b"/>
</p>

<a name="day18"></a>

#### Day 18 - inline

Can’t wait to use lambdas to make new APIs? 

Get in line. 

Kotlin lets you specify a function as `inline` - which means calls will be replaced with the function body. Breathe and make lambda-based APIs with zero overhead.

Docs: [https://kotlinlang.org/docs/reference/inline-functions.html](https://kotlinlang.org/docs/reference/inline-functions.html)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day18.png" width="512" height="287" alt="day18"/>
</p>

<a name="day19"></a>

#### Day 19 - require

[1/2] Are your function arguments valid? Check before using them, with `require`. If they’re not valid an IllegalArgumentException is thrown.

Doc: [https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/require.html](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/require.html)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day19.png" width="512" height="287" alt="day19"/>
</p>

<a name="day20"></a>

#### Day 20 - latinit

In Android, onCreate or other callbacks initialize objects. In Kotlin non-null vals must be initialized. What to do?

Enter `lateinit`. It's a promise: initialize me later! Use it to pinky-swear it will "eventually" be null safe

Docs: [https://kotlinlang.org/docs/reference/properties.html#late-initialized-properties-and-variables](https://kotlinlang.org/docs/reference/properties.html#late-initialized-properties-and-variables) 

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day20.png" width="512" height="287" alt="day20"/>
</p>

<a name="day21"></a>

#### Day 21 - lazy

It’s good to be lazy! Defer the cost of expensive property initialization until they’re actually needed, by using `lazy`. The computed value is then saved and used for any future calls. 

Lazy: [https://kotlinlang.org/docs/reference/delegated-properties.html#lazy](https://kotlinlang.org/docs/reference/delegated-properties.html#lazy)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day21.png" width="512" height="287" alt="day21"/>
</p>

<a name="day22"></a>

#### Day 22 - sealed classes

[1/3] Kotlin sealed classes let you easily handle error data. When combined with LiveData you can use one LiveData to represent both the success path and the error path. Way better than using two variables. 

Docs: [https://kotlinlang.org/docs/reference/sealed-classes.html](https://kotlinlang.org/docs/reference/sealed-classes.html)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day22.png" width="512" height="287" alt="day22"/>
</p>

<a name="day23"></a>

#### Day 23 - default parameters

Is the number of method overloads getting out of hand? Specify default parameter values in functions.  

Make the code even more readable with named parameters.

Doc:  [https://kotlinlang.org/docs/reference/functions.html#default-arguments](https://kotlinlang.org/docs/reference/functions.html#default-arguments)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day23.png" width="512" height="287" alt="day23"/>
</p>

<a name="day24"></a>

#### Day 24 - access modifiers

In Kotlin, everything is public by default! Well, almost. Kotlin has a rich set of visibility modifiers you can use as well: private, protected, internal. Each of them reduces the visibility in a different way. 

Docs: [https://kotlinlang.org/docs/reference/visibility-modifiers.html](https://kotlinlang.org/docs/reference/visibility-modifiers.html)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day24.png" width="512" height="287" alt="day24"/>
</p>

<a name="day25"></a>

#### Day 25 - data classes

Creating classes with one role: to hold data? Mark them as “data” classes. The default implementation of equals() is generated (so are hashCode(), toString(), and copy()) and checks for structural equality.

Docs: 
[https://kotlinlang.org/docs/reference/data-classes.html#data-classes](https://kotlinlang.org/docs/reference/data-classes.html#data-classes)
[https://kotlinlang.org/docs/reference/equality.html](https://kotlinlang.org/docs/reference/equality.html)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day25.png" width="512" height="287" alt="day25"/>
</p>

<a name="day26"></a>

#### Day 26 - properties

In Kotlin, classes can have mutable and read-only properties, with getters and setters generated by default. You can also implement custom ones if required.

Docs: [https://kotlinlang.org/docs/reference/properties.html](https://kotlinlang.org/docs/reference/properties.html)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day26.png" width="512" height="287" alt="day26"/>
</p>

<a name="day27"></a>

#### Day 27 - ranges

For loops get superpowers when used with two other Kotlin features: range expressions and destructuring. 

Ranges: [https://kotlinlang.org/docs/reference/ranges.html](https://kotlinlang.org/docs/reference/ranges.html)

Destructuring: [https://kotlinlang.org/docs/reference/multi-declarations.html#destructuring-declarations](https://kotlinlang.org/docs/reference/multi-declarations.html#destructuring-declarations)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day27.png" width="512" height="287" alt="day27"/>
</p>

<a name="day28"></a>

#### Day 28 - when statement

A switch statement with superpowers? Kotlin’s `when` expression can match on just about anything. Literal values, enums, ranges of numbers. You can even call arbitrary functions!
 
Docs: [https://kotlinlang.org/docs/reference/control-flow.html#when-expression](https://kotlinlang.org/docs/reference/control-flow.html#when-expression)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day28.png" width="512" height="287" alt="day28"/>
</p>

<a name="day29"></a>

#### Day 29 - KTX destructuring

Now with prisms? Android KTX uses destructuring to assign the component values of a color. You can use destructuring in your classes, or extend existing classes to add destructuring. 

Docs: [https://kotlinlang.org/docs/reference/multi-declarations.html](https://kotlinlang.org/docs/reference/multi-declarations.html)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day29.png" width="512" height="287" alt="day29"/>
</p>

<a name="day30"></a>

#### Day 30 - string templates

Formatting Strings? Refer to variables and expressions in string literals by putting `$` in front of the variable name. Evaluate expressions using `${expression}`.

Docs: [https://kotlinlang.org/docs/reference/basic-types.html#string-templates](https://kotlinlang.org/docs/reference/basic-types.html#string-templates)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day30.png" width="512" height="287" alt="day30"/>
</p>

<a name="day31"></a>

#### Day 31 - elvis operator

Handling nulls in style? Check out the elvis operator `?:`, to cut your “null-erplate”. It’s just a small bit of syntax sugar to replace nulls with a default value or even return! 

Docs: [https://kotlinlang.org/docs/reference/null-safety.html#elvis-operator](https://kotlinlang.org/docs/reference/null-safety.html#elvis-operator)

<p>
<img src="https://github.com/andyb129/31DaysOfKotlin/blob/master/app/src/main/res/drawable/day31.png" width="512" height="287" alt="day31"/>
</p>


### Thanks

Thanks to the Google Android Developer team for putting together this cool series of Kotlin info! :smile:


