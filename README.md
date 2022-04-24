# XOperaExamples
XOpera and Tosca Examples
## First Example
In FirstExample.yaml there is a simple **Compute** 
node ,called *db_server*, in which are declared some host properties that are built into this node definition.

## Second Example

In Second Example a **MySql** node template is installed over the aforementioned 
db_server. This simulates the installation of Mysql over this server.

By assigning localhost as the values of the *db_server* node template's attributes private_address and public_address , **MySql** is hosted on the same workstation from which opera is running.