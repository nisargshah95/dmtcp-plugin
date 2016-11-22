Dependencies -

- MySQL
- MySQL client library

Compiling -

1. Configure the shell variable DMTCP_ROOT to point to the DMTCP installation

2. Compiling the plugin
gcc -g -shared -fPIC -I$DMTCP_ROOT/include plugin.c -o plugin.so -std=c99 `mysql_config --cflags --libs`

3. Compile example code
gcc examples/c_mysql3.c -o c_mysql3 -std=c99 `mysql_config --cflags –libs`

Launching test application -
$DMTCP_ROOT/bin/dmtcp_launch --with-plugin plugin.so ./c_mysql3 [args]