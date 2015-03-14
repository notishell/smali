# Prerequisites #

This is possibly an incomplete list. If you encounter something that is missing, feel free to leave a comment and I'll add it on

  * jdk (1.5 or 1.6 should be fine)
  * git

Everything else should be downloaded by gradle/gradlew

# Build Procedure #

```
git clone https://code.google.com/p/smali/
cd smali
./gradlew build
```

(on windows, use `gradlew.bat` instead of `./gradlew`)

The jar files should be at

`smali/build/libs/smali-<version>.jar`

and

`baksmali/build/libs/baksmali-<version>.jar`

Alternately, you can do

```
./gradlew proguard
```

And you'll also get smaller, proguarded versions of the libraries

`smali/build/libs/smali-<version>-small.jar`

and

`baksmali/build/libs/baksmali-<version>-small.jar`