### About ###
smali/baksmali is an assembler/disassembler for the dex format used by dalvik, Android's Java VM implementation. The syntax is loosely based on Jasmin's/dedexer's syntax, and supports the full functionality of the dex format (annotations, debug info, line info, etc.)

The names "smali" and "baksmali" are the Icelandic equivalents of "assembler" and "disassembler" respectively. Why Icelandic you ask? Because dalvik was named for an Icelandic fishing village.

Curious what the smali format looks like? Here's a quick [HelloWorld example](http://code.google.com/p/smali/source/browse/examples/HelloWorld/HelloWorld.smali) to whet your appetite.

<i><h2>Got questions/comments? Need help? Come hang out in <a href='http://webchat.freenode.net/?channels=smali'>#smali</a> on freenode.</h2></i>

### News ###
**2015-01-20** v2.0.5 is out! It fixes a multi-threading issue in baksmali in 2.0.4, and it switches the default for implicit references to no-implicit-references, for better backwards compatibility.

**2015-01-20** The v2.0.4 release is faulty. The download has been removed, and a fixed v2.0.5 will be released shortly.

**2015-01-20** v2.0.4 is out
  * Added optional functionality to add the resource name as a comment to likely resource accesses. See the help for the new -i/--resource-id-files option (credit: Jeff Smith/whydoubt)
  * Added comments for constants that are likely an encoded float/double (credit: Jeff Smith/whydoubt)
  * Added support for implicit method/field references within a class, which allows you to leave off the class name when referencing a field/method within the current class.
  * Changed short option for --check-package-private-access to -k (from -K) (thanks to yyjdelete for noticing/reporting a problem with an interim change related to this)
  * Added the ability to disassemble a file other than classes.dex within an apk (credit: Connor Tumbleson/iBotPeaches)
  * other misc bugfixes, etc.
**2014-01-17** v2.0.3 is out
  * More bugs being slaughtered in this release. Notably, smali's memory footprint should now be reduced, although it's still a good idea to use -JXmx512m when using multiple threads.
  * We also managed to sneak in some new features as well. Thanks to [whydoubt](https://github.com/whydoubt), it's now possible to add a comment with the resource name when a resource id is referenced in the bytecode as a constant, using the new -i flag.
  * As a reminder, the googlecode downloads are deprecated and downloads are now hosted at [bitbucket](https://bitbucket.org/JesusFreke/smali/downloads)

**11-10-13** v2.0.2. Bugs are dead. Long live bugs.

**10-10-13** v2.0. 2.0 is finally out of beta and ready for mass consumption. Consume away!

**Administrivia:**
  * The primary download location has been moved to [bitbucket](https://bitbucket.org/JesusFreke/smali/downloads), per the impending deprecation of downloads on googlecode.
  * The dexlib\_redesign branch in the repository has been merged into the master branch, and the dexlib\_redesign branch itself is dead.
  * The old dexlib library is now gone from the repository, in favor of the new dexlib2 library.
  * The old master branch is available as the [v1.4.3 tag](https://code.google.com/p/smali/source/browse/?name=v1.4.3) - there was never an actual 1.4.3 release, but it contains a few changes that occurred on the master branch after the 1.4.2 release.
A big thanks goes out to Izzat "TwoSheds" Bahadirov for significant effort in helping me out with the dexlib2 redesign, and to all the people who helped test and reported bugs for the 2.0 beta.


**9-14-13** v2.0b6. This version has some significant reworking of how instruction rewriting is handled, as well as various other bug fixes. For people using dexlib2 directly, you'll want to take note of the new MethodImplementationBuilder and/or MutableMethodImplementation classes, which should help streamline creating new method implementations, or modifying existing method implementations.

**6-15-13** v2.0b5, now with 34.2% more bug fixes! Downloads: [smali](https://code.google.com/p/smali/downloads/detail?name=smali-2.0b5.jar)/[baksmali](https://code.google.com/p/smali/downloads/detail?name=baksmali-2.0b5.jar)

**5-12-13** v2.0b4, which fixes some new issues introduced in b3.

**5-12-13** A new 2.0b3 release, which adds multithreading for baksmali.

**5-7-13** A minor update to the beta (v2.0b2), that fixes a reported dexodexing issue.

**5-7-13** A beta release (v2.0b1) is available for the next major of smali/baksmali. You can find more info on the [wiki page](https://code.google.com/p/smali/wiki/SmaliBaksmali20). Feel free to grab the beta jars from the downloads page and give it a spin. Something doesn't work? Please file a [bug report](https://code.google.com/p/smali/issues/list)!

**2-14-13** smali/baksmali v1.4.2 is out, with a handful of bugfixes.

**11-19-12** smali/baksmali v1.4.1 is out. This is mostly just a bugfix release, although
it does include support for a minor change in the way odex files are generated in api 17.

**9-16-12** smali/baksmali v1.4.0 is out! The primary feature in this release is that deodexing has been much simplified. This has actually been implemented for a month or two, but I'm just now getting around to doing a release. See the [deodex instructions](http://code.google.com/p/smali/wiki/DeodexInstructions) for additional information. Additionally, for the developers out there, you'll notice that the mvn build has been replaced with a gradle build. The [build instructions](http://code.google.com/p/smali/wiki/BuildProcedure) have been updated accordingly.

**6-20-12** smali/baksmali v1.3.3 is out. cleanup, bugfixes, more cleanup. Did I mention cleanup?

**1-11-12** smali/baksmali v1.3.2 is out. This version has a few misc. bugfixes

**11-20-11** smali/baksmali v1.3.0 is out! This version now supports Honeycomb and Ice Cream Sandwich. More details [here](http://blog.jesusfreke.com/2011/11/smalibaksmali-130.html).<br><font size='3'><b><i>Important</i></b></font> When deodexing pre-ICS odex files, you must use the new --api-level/-a option to specify the api level<br>
<br>
<b>8-22-11</b> smali/baksmali v1.2.8 is out. This fixes a problematic bug that crept into 1.2.7<br>
<br>
<b>8-13-11</b> smali/baksmali v1.2.7 is out. This is a bugfix release, with a small additional feature (helper comments for synthetic access methods)<br>
<br>
<b>12-23-10</b> smali/baksmali v1.2.6 is out, with support for gingerbread odex files<br>
<br>
<b>10-31-10</b> smali/baksmali v1.2.5 is out. This is a minor release with a few small bugfixes<br>
<br>
<b>8-1-10</b> smali/baksmali v1.2.4 is out, with a number of bugfixes <a href='http://jf.andblogs.net/2010/08/01/more-smalibaksmali-bugfixes/'>blog post</a>

<b>6-13-10</b> smali/baksmali v1.2.3, now with frozen yogurt! <a href='http://jf.andblogs.net/2010/06/13/yes-i-would-like-some-frozen-yogurt-with-my-baksmali-please/'>blog post</a>

<b>4-03-10</b> smali/baksmali v1.2.2 is out! This is again mostly a bugfix release, but it also has significant performance improvements as well. More details <a href='http://jf.andblogs.net/2010/04/03/yabbfr/'>here</a>

<b>3-06-10</b> smali/baksmali v1.2.1 is out! This is mostly a bugfix release, with a few performance improvements and enhancements.<br>
<br>
<b>2-22-10</b> smali/baksmali v1.2 is out! As usual, more info on <a href='http://jf.andblogs.net/2010/02/22/smali-baksmali-1-2-released/'>my blog</a>

<b>12-25-09</b> smali/baksmali v1.1 is out. More info on <a href='http://jf.andblogs.net/2009/12/25/have-a-very-smali-christmas/'>my blog</a>

<b>11-08-09</b> smali/baksmali v1.0 is out. More info on <a href='http://jf.andblogs.net/2009/11/08/smalibaksmali-v1-0/'>my blog</a>

<b>9-10-09</b> smali/baksmali v0.96 is out. baksmali now supports deodexing .odex files! For the first time you can turn those pesky .odex files into much-easier-to-use classes.dex files. Here are <a href='http://code.google.com/p/smali/wiki/DeodexInstructions'>instructions</a> on how this magic is performed.<br>
<br>
<b>NOTE</b> deodexerant is just a helper binary that runs on the phone and talks to baksmali. It doesn't do much of anything interesting in and of itself. Unless you want to dump some vtables or something :)<br>
<br>
<b>8-29-09</b> smali/baksmali v0.95 is out. The major change in this version is a re-implemented version of dexlib, as well as changes in smali/baksmali to work with the new dexlib. Also, I've optimized baksmali, so it should run much much quicker now (up to 4x quicker). smali should also be a bit quicker, but nothing you'll probably notice.<br>
<br>
As far as new functionality goes, baksmali will now output registers that are mapped to method parameters using a p<code>&lt;n&gt;</code> syntax, instead of the normal v<code>&lt;n&gt;</code> syntax. i.e. p0 is the first method parameter (or the "this" reference, for non-static methods), p1 is the second method parameter and so on. If you want to disable this functionality, you can use the -p command line arg.<br>
<br>
<br>
<b>7-27-09</b> smali/baksmali v0.94 is available. This is a bugfix release, a few typo fixes here and there, plus it should be compatible with java 5 now (for the Mac users out there)<br>
<br>
<b>7-3-09</b> baksmali v0.93 is available on the download tab. v0.92 had a template issue that prevented it from running.<br>
<br>
<br>
<b>7-2-09</b> smali/baksmali v0.92 has been released. This is a minor bugfix release. Thanks to Stericson and Josef Pfleger for the bug reports!<br>
<br>
<br>
<b>6-23-09</b> The first release of baksmali (v0.91) is out! Also, a new version of smali, also v0.91, with a number of improvements and fixes. Still no documentation.. I'll get there eventually.<br>
<br>
<br>
<b>6-7-09</b> After lots and lots of work, the first release of smali is out finally! You can grab it from the downloads tab. I'll try and get a wiki going with some documentation, as far as usage and syntax goes. For now, you can look at the examples and tests to see the syntax. There are tests for every opcode, so you should be able to find the syntax you need.<br>
<br>
<b>6-3-09</b> I've been whipping smali into shape the past few days. I should be getting close to a release soon! Currently, it should be able to handle all the features supported by the dex format. I still need to spend some time with the error handling, move all the tests from HelloWorld2.smali to the new junit-tests testing framework, and write more examples.<br>
<br>
<br>
<b>5-9-09</b> I've just added support for packed-switch and sparse-switch, and now smali supports the full set of dex opcodes. Woot! There's still a decent amount of work to be done though. I need to implement try blocks, annotations, debug/line info, add better exception handling in the parsing code, write a real front end, etc.<br>
<br>
<br>
<br>
<h3>More</h3>
To see some examples of the syntax, take a look at <a href='http://code.google.com/p/smali/source/browse/#git%2Fexamples'>examples</a>. This contains examples of how various features are implemented in smali.<br>
<br>
The lexer/parser for smali is built with ANTLR v3, and the dex file generation is done by dexlib, a library I have written to read in and write out dex files.<br>
<br>
baksmali uses dexlib to read in dex files, and the StringTemplate library (a companion library to ANTLR) to generate the disassembly.<br>
<br>
<hr />

Developed With: <br>
<a href='http://www.jetbrains.com/idea/'>
<img src='http://www.jetbrains.com/idea/opensource/img/all/banners/idea120x30_blue.gif' alt='The best Java IDE' border='0' /></a>