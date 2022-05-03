# How to write a generator using ceps

- Install ceps (https://github.com/cepsdev/machines4ceps)
- Clone this repo. Assumption: repo ends up in the same directory which also contains ceps, machines4ceps, log4ceps.
- If necessary edit build_all.sh/rebuild_all.sh, i.e. set the values of CEPSCORE, MACHINES4CEPS, LOG4CEPS according to your configuration.
- $ cd repo
- $ ./rebuild_all.sh && ./run_test.sh test/simple_test.ceps
- Your terminal output should look like (modulo compiler version etc.):

```
-- The C compiler identification is GNU 9.3.0
-- The CXX compiler identification is GNU 9.3.0
-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++
-- Check for working CXX compiler: /usr/bin/c++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done
-- Generating done
-- Build files have been written to: /home/tomas/dev/tutorial_write_a_generator/bin
Scanning dependencies of target generator-plugin
[ 50%] Building CXX object CMakeFiles/generator-plugin.dir/src/plugin-entrypoint.cpp.o
[100%] Linking CXX shared library libgenerator-plugin.so
[100%] Built target generator-plugin

Executing test/simple_test.ceps
==============================================================


generator::plugin_entrypoint:
        (INT 123  )
        "abc" 
        (STRUCT "uint32" (ID "ThisIsAnIdentifier" ))
        (INT 2  )


result = 42
```
