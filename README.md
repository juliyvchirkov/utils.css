# helpers.css

ambry w/ a couple of useful css helper sets

## helper.indent.css

the goal of this helper set is to provide the fast & simple way to align an item in html layout thru its outer / inner indentation

each class in this helper can be safely combined w/ any number of other classes of the set, classes can be applied to an item in any order

one nominal indentation step has been designed to equal **10px**, the naming in the set is unified on this basis, so it shouldn’t be a rocket science to keep the class names in mind for anyone

varying the combinations of helper classes one can quickly align an item w/ **4** outer & **4** inner directions at once (outer ``margin-top`` ``margin-bottom`` ``margin-left`` & ``margin-right``, inner ``padding-top`` ``padding-bottom`` ``padding-left`` & ``padding-right``). the indentation on each direction can be tuned from **2px** up to **100px** w/ the scale containing all commonly used milestones like 5px, 10px, 15px, 20px, 25px, 30px, 40px, 50px et cetera

besides the numerical values the helper also consists of 14 additional classes covering the cases w/ ``auto`` & ``zero`` indentation for almost<sup name="a1">[1](#f1)</sup> every direction mentioned above

### an example

markup for some ``div`` auto centered horizontally, w/ **50px** gap above the container & **40px** gap below, w/ inner vertical gaps from top & bottom **15px** each & inner horizontal gaps from left & right **25px** each, will be as simple as 

```

<div class="tind-hg bind-4x lind-a rind-a tindi-lg bindi-lg lindi-xlg rindi-xlg">[…</>…]</div>

```

### filelist

**helper.indent.css** oversized stylesheet, contains a lot of redundant info. published for educational purposes to explore the classes & examine the logic of naming

**helper.indent.compact.css** compact version of helper. recommended for real use (on a par w/ the minified copy below on one’s choice). provides the same functionality as the oversized one above, but contains only the shortest names for clases declaration (since nobody will type ``top-indent-inner-large`` once & again vice ``tindi-lg``)

**helper.indent.compact.min.css** minified copy of the above

<b id="f1">[1]</b> syne the inner auto indentation is not supported & attempt to apply ``auto`` to ``padding`` is treated as malformed rule & ignored, classes ``tindi-a`` & ``bindi-a`` for top & bottom inner vertical auto indentation have not been incuded in the set. notwithstanding the foregoing, despite the inability to set ``padding`` as ``auto`` directly, the other pair of classes for horizontal auto indentation ``lindi-a`` & ``rindi-a`` has not been removed & can be safely used for inner horizontal auto indentation either on left / right direction alone or both together ’cause I’ve found the way to achieve this functionality thru workaround [↺](#a1)

## helper.animate.css

the goal of this helper is to expand the tuning flexibility of the world-famous css animation library [animate.css](https://github.com/daneden/animate.css) w/o altering the original vendors’ stylesheet

the [animate.css](http://daneden.github.io/animate.css) library contains bunch of cool & fun cross-browser ready-for-use css animations, which fit for the wide range of usecases. a fly in the ointment is the ``duration`` (full cycle of playing) of these animations: almost all of them are bounded to **1s** limit ’cause this value is hardcoded in special ``.animated`` class of the library, the trigger for animations to start

this helper provides the solution to override this limit & apply an individual time to play for every animation in html

classes in this helper are designed to be applied alone, one single class from the set per animation. although the attempt of mass use of these classes at once can’t spoil anything, it’s senseless syne the last helper class applied to an animation will override the settings of the whole bunch

the original **1s** limit of ``animate.css`` is taken as untuned ``normal speed`` value, the time to play (``duration``) of animation can be tuned in both directions in range from **2000%** slower to **2000%** faster w/ the following set of milestones 

```

∿.05s∿.1s∿.2s∿.25s∿.33s∿.5s∿ untuned 1s value ∿1.5s∿2s∿2.5s∿3s∿4s∿5s∿6s∿7s∿8s∿9s∿10s∿20s∿

```

### an example

markup of ``slideInDown`` animation from ``animate.css`` library in slow-mo awesome for growls (250% slower) will be as simple as 

```

<div class="slideInDown animated adagio-lg">[…</>…]</div>

```

we can lose that guy, the heartbeat is extremely high! 

```

<div class="pulse infinite animated allegro-lg">[…</>…]</div>

```

### filelist

**helper.animate.css** oversized stylesheet, contains some redundant info. published for educational purposes to explore the classes & examine the logic of naming

btw, this helper offers the naming in two alternative ways: the first one utilizes common speed definitions, & the second one is based on two special musical terms ``allegro`` & ``adagio``  

**helper.animate.compact.css** compact version of helper. recommended for real use (on a par w/ the minified copy below on one’s choice). provides the same functionality as the oversized one above, but contains only the shortest names for clases declaration based on musical terms

**helper.animate.compact.min.css** minified copy of the above

**glory to Ukraine!** 🇺🇦

Juliy V. Chirkov,  
[twitter.com/juliychirkov](https://twitter.com/juliychirkov)
