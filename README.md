# Mandala-Libs-And-Examples
A collection of Mandala code to be used as standard and system libraries when developing for the [Sanskrit platform](https://github.com/tawaren/Sanskrit). Further it contains an example use case.  
This is part of my PhD thesis at the University of Zurich.

## License

Copyright (C) 2024 Markus Knecht, System Communication Group, University of Zurich.

This project is licensed under the GNU General Public License v3.0. You can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.

## Status

**Research Grade Software**

This software is currently in a research-grade state and is not production-ready. It has been developed for testing and evaluation purposes. 

**Use at Your Own Risk**

Use of this software is at your own risk. The developers and contributors are not responsible for any damage or loss that may result from using this software. It is provided "as-is" without any warranties or guarantees.

## What is contained
The main part is the Mandala standard library in std. It also contains the system library under std/core/sys.
All three folders (std, std/core, std/core/sys) are valid workspaces for the [Samaya](https://github.com/tawaren/Samaya) build tool. They are structured as sub-workspaces of each other, meaning that building std will build the other two workspaces as well. 

The standard and system library provides the following:
 - Primitive data types and operations on them:
	 - A Boolean
	 - Signed and unsigned integers with 8, 16, 32, 64, and 128 bits
	 - Byte container (Data) to hold 1,2,4,8,12,16,20,24,28,32 raw bytes
 - Cryptographic functions:
	 - A Hash function
	 - A EdDSA signature verification function
 - Identifier types (used as basis for many other features)
 - Types used to interact with the Blockchain
	 - A Context (containing: block number, transaction hash, section number, and transaction index)
	 - An unique identifier generator
	 - A Entry to store values in the Blockchain state under an identifier
 - Classes and corresponding implementations
	 - Arith: For arithmetic operation on values
	 - BitOps: For bitewise operations on values
	 - Hash: For hashing of values
	 - Equal: To compare values for equality
	 - Compare: To compare ordered values
 - Virtual Cryptography (using private & public identifiers to simulate assymetric cryptography):
	 - Signing and Verifying
	 - Sealing and Unsealing (similar to encrypt and decrypt)
 - Usefull general data types
	 - Tuple
	 - Either
	 - Option
 - Types and functions for Access controll
	 - Capabilities
	 - Permissions
	 - Subjects
	 - Authenticator using EdDSA
 - Token and Asset related functionality
	 - Fungible class
	 - Token data type
	 - Asset data type
	 - Purse data type (for token storing)
	 - Market data type (for trading)
	 - A Lock type to assign Ownership to values

For more details about the contained types and functions consult the PhD thesis (the link follows after publication)

In addition to the standard and system library the example folder contains an example on how to use the library, especially the ones assosiated with token and assets. The example folder is a valid [Samaya](https://github.com/tawaren/Samaya) workspace. The folder commands contains text files that show transactions using the the example.

The folder pkg contains aprecompiled versions of the standard and system library and the example as Samaya archives.

Finally the measure folder contains measurement data recorded when executing the example use case and are their for transparency (they are used in the PhD thesis).