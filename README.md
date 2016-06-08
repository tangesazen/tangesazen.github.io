# tangesazen.github.io

I slightly modified the RedBear Duo (v0.2.9) and Digistump (v1.0.2) json files to work with the [arduino-eclipse-plugin](https://github.com/jantje/arduino-eclipse-plugin).

To add them to Preferences => Arduino => Locations, use:

	https://tangesazen.github.io/package_readbear_index.json  
	https://tangesazen.github.io/package_digistump_index.json

For the RedBear Duo, you also need to set the following in Properties => C/C++ Build => Build Variables:

  A.ARCHIVE\_FILE  		  libcore.a  
  A.RECIPE.AR.PATTERN     "${A.COMPILER.PATH}${A.COMPILER.AR.CMD}" ${A.COMPILER.AR.FLAGS} "${A.OBJECT_FILE}"  
  A.RECIPE.AR.PATTERN.2   && "${A.COMPILER.PATH}${A.COMPILER.AR.CMD}" -dv "${A.BUILD.PATH}/libcore.a" libcore.a
  
