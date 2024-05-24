# What is a Software Version Number: 

- A software version number is a unique set of numbers that identifies different releases and updates of a software program, file, firmware, device driver, or hardware. 

- Version numbers are usually made up of two to four numbers separated by periods, and they increase in value as new developments are made to the software. 



# Let's Understand Different Parts of a Software Version Number: 

* Most commonly software version numbers have `3 Numbers seperated by periods` 

* But here's the break down of all the 4 numbers of a software version number: 

```
    * In version 1.9.2.5 : 

        1: Major Version/Revision (new UI, lots of new features, conceptual change, etc.) 

        9: Minor Version/Revision (maybe a change to a search box, 1 feature added, collection of bug fixes) 

        2: Patch Version aka Bug fix release (This number tracks patches or bug fixes). It may also be called a "point release" or "subminor version" 

        5: Build number (if used) - that's why you see the .NET framework using something like 2.0.4.2709 
``` 

> You won't find a lot of apps going down to four levels, 3 is usually sufficient. 


![Software Version Number Breakdown](<12_Software Version Number Breakdown.jpg>)


<br>


# What is a Package: 

- When developing software, it is common to use external libraries or modules written by other developers to avoid writing code from scratch. 
- These external libraries or modules are called packages. 


<br> 


# Understanding Symbols with Software Version Numbers of Packages: 

- Whenever we install any node package from npm, that package gets an entry in `package.json` file as a key-value pair 
- And when you see these packages with their software version numbers ("react": "^18.3.1"), you can notice different types of symbols with these version numbers, and the symbols look like these ones (*, ^, ~) 

> These above mentioned 3 symbols are the symbols written with version number of packages which indicate changes to different parts of the version (What does this really means?? Let's understand ahead) 



# What does these 3 symbols mean exactly with the software version numbers of the packages: 

1. Caret Symbol (^): 
    - Means "compatible with version". For example, ^3.4.1 allows any version between 3.4.1 and 4.0.0, but not 4.0.0. 
    - So, basically if caret symbol is present with a package's software version number, then it simply means whenever the developer wants to update all the packages of this application generally, then the package manager is only allowed to update the minor and patch version, and the build number if it is present in the version number 
    - The major version of this package cannot be updated blindly, because it can cause compatibility issues if you always update a package to its newest version blindly.
    - In major version updates there can be significant changes in the package, and if your application isn't compatible with the newest version of this package then your application will crash without having any change in the code base and this is not a good behaviour to have in your application
    - If the developer wants to upgrade the major version of this package which has a caret symbol, they should read the release notes of the new major version first and update the package to the newest major version explicitly if there are no conflicts with the code base, and if any thing has become out dated in the codebase or has been changed in the newest version of the package, then the developer should update the code base and modernize it as per the newest version of the package if they have chosen to update the package to its newest major version 

2. Tilde Symbol (~): 
    - Means "approximate version". For example, ~2.3.3 allows values between 2.3.3 and 2.4, but not 2.4.  
    - This symbol basically means only the patch version and the version number components after the patch version are allowed to get automatic updates within the same minor version.  
    - But the minor and major version will get fixed to whatever they are and they will never get updated automatically for this package which has tilde symbol with it in the dependency file like "package.json" 

3. Asterisk Symbol (*): 
    - Means "wildcard" and allows any version of a dependency.  
    - For example, "axios": "*" allows npm to install the latest version of Axios. 
    - However, this can cause compatibility issues if a new major version is released.

4. No Symbol: 
    - When no symbol is used, it usually means an exact version match is required. 
    - For example, if you have a package dependency listed as 1.2.3, it means that only version 1.2.3 of the package is allowed, there can be no automatic updates imposed on this package by the package manager if the developer launches a general update command, to make this package updatable, the developer have to add a suitable symbol in front of the package's version number in the package.json file. 


<br> 


# Note: 

> These symbols are also called "Package Versioning Symbols" 


<br> 


# References Cited: 

* __StackOverflow__ (What do the numbers in a version typically represent (i.e. v1.9.0.1)?)__:__  
https://stackoverflow.com/questions/65718/what-do-the-numbers-in-a-version-typically-represent-i-e-v1-9-0-1 

* __Medium__ (Package Versioning Symbols: ^, ~, and No Symbol Explained)__:__ 
https://javascript.plainenglish.io/package-versioning-symbols-and-no-symbol-explained-54f29f64d9b6 