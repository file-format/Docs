{
  "date" : "2021-09-23", 
  "keywords" : [ "NUT", "file", "extension", "file format", "NUT рrоgrаmming lаnguаge", "Programming Guide", "NUT example", "NUT file format", "squirrel language", ".nut extension file", "NUT files" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "NUT - Squirrel Language File",
  "description":"Learn about NUT file format and APIs that can create and open NUT files.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-09-23"
}

## What is a NUT file?

The NUT file format belongs to the programming language which is known as Squirrel. It is an object-oriented, high level and imperative programming language which is used mostly in embedded systems and video games. 

The squirrel language is considered a lightweight scripting language that can be easily adjusted according to size and bandwidth. It involves the advantage of automatic reference counting and the management of garbage in memory.

The syntax of the squirrel language attracts the developers as it is C-like and involves the feature of scripting language. But still, it has quite fewer advantages as compared to other more popular programming languages for this purpose.  



## Brief History ##

It was designed by Alberto Demichelis in 2003. However, a stable version of this language was released in 2016. It was designed under the license of zlib/ libpng. In 2010 the license was changed and transferred to MIT. This language is considered as an inspired version of [LUA](/programming/lua/) (Programming language). There is a list of suggestions for the former language on the website designed by Alberto to make it more advantageous.


## Technical Specification  ##

The feature and specifications of the squirrel language are multiple. It provides the facility of Dynamic typing, property of delegation, several uses of classes and interfaces. The syntax of this language has a similarity with the syntax of the C language. Applications such as Enduro/X (a cluster application server) use this language. As Squirrel is used for video games too, some of those are OpenTTD, GTA IV, etc.

The stable release of the language is 3.0.7. A toolkit known as MirthKit uses Squirrel programming language to provide an open-source and cross-platform for two-dimensional games. The nature of this language is dynamic and most of the features similar to [Python](/programming/py/), LUA, etc. It also involves the implementation of register-based VM. The performance of Squirrel is slower as compared to LUA.

There is also another ".nut" extension file type which is why you should look at the size of the file to find out which NUT file do you have. Squirrel script NUT files are mostly smaller than 1 MB whereas video NUT files are usually bigger than 1 MB in size.


## NUT File Format Example ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
    }
    else {
      return x * factorial(x-1);
    }
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
      }
    }
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
    }
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
    }
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## Reference ##

* [NUT - by Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))


