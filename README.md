U-Prove Crypto SDK V1.1.3 (C# Edition)
======================================

The U-Prove Crypto SDK V1.1 (C# Edition) implements the U-Prove Cryptographic
Specification V1.1 Revision 3 [UPCS]. This SDK was developed by Microsoft to
support experimentation with the foundational features of the U-Prove technology.
It is made available under the Apache 2.0 open-source license, with patent
rights granted under the Open Specification Promise.

For more information about U-Prove, visit http://www.microsoft.com/u-prove.

## Rebex Labs
https://labs.rebex.net/CryptoRT

Rebex Cryptography for Windows Store Apps and Windows Phone 8.1
Porting cryptographic applications from classic .NET to target Windows Store Apps or Windows Phone 8.1 is difficult. The new platforms lack the good old System.Security.Cryptography namespace. Instead, they offer a new cryptographic API in Windows.Security.Cryptography namespace (based on Windows Runtime API), but it's completely different and lacks many previously-available features.

CONTENTS:
---------

 - LICENSE: The license and patent grant under which this package is distributed
 - ThirdParty\: Bouncy Castle library files
 - UProveCrypto.sln: Visual Studio solution file
 - UProveCrypto\: SDK project
 - UProveParams\: Recommended parameters generation project (not included in
                  solution by default)
 - UProveSample\: Sample project
 - UProveTestVectors\: Test vectors generation project (not included in
                       solution by default)
 - UProveUnitTest\: Unit test project


BUILDING THE SDK:
-----------------

Open the solution file (UProveCrypto.sln) in Visual Studio 2012 (or a more recent
version) and select "Build Solution" from the "Build" menu.


GENERATING RECOMMENDED PARAMETERS AND TEST VECTORS
--------------------------------------------------

Recommended parameters [UPRP] and test vectors [UPTV] used by the U-Prove SDK 
can be re-generated for validation purposes by loading and running the UProveParams
and UProveTestVectors projects, respectively. The projects depend on the full
BouncyCastle library, and are therefore not included in the UProveCrypto.sln file
by default. BouncyCastle must be obtained from 
http://www.bouncycastle.org/csharp/, the compiled DLL must be placed under
"ThirdParty\BouncyCastle\bc\BouncyCastle.dll", and the two projects must be added
to the solution before compiling it.

USING THE UNIT TESTS:
---------------------

In the "Test" menu of Visual Studio, select the "All Tests"
from the "Run" submenu item. Note that a complete test run takes some
time to complete.


USING THE SDK:
--------------

Add the UProveCrypto assembly to the set of References for a project.

NOTES:
------

This code was formerly hosted on CodePlex (https://uprovecsharp.codeplex.com).
The following changes have been made to the original code:
 - The solution has been updated to Visual Studio 2017.
 - The Bouncy Castle patch (https://uprovecsharp.codeplex.com/SourceControl/list/patches)
   has been applied, improving efficiency of math operations.

REFERENCES:
-----------

[UPCS]    Christian Paquin, Greg Zaverucha. U-Prove Cryptographic Specification V1.1.
          Microsoft Corporation, December 2013. http://www.microsoft.com/u-prove.

[UPTV]	  U-Prove Cryptographic Test Vectors V1.1 (Revision 3)
          http://research.microsoft.com/apps/pubs/default.aspx?id=166983

[UPRP]    U-Prove Recommended Parameters Profile V1.1 (Revision 2)
          http://research.microsoft.com/apps/pubs/default.aspx?id=166972