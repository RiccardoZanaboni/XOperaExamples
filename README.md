# XOperaExamples
XOpera + Tosca Examples
## First Example
In FirstExample.yaml there is a simple **Compute** 
node ,called *db_server*, in which are declared some host properties that are built into this node definition.

## Second Example

In Second Example a **DBMS.MySql** node template is installed over the aforementioned 
*db_server*. This simulates the installation of Mysql over this server.

By assigning localhost as the values of the *db_server* node template's attributes private_address and public_address,**MySql** is hosted on the same workstation from which opera is running.

## Third Example

In ThirdExample.yaml a **Database.MySql** node template is added. This represents an actual MySQL database instance managed by a MySQL DBMS.

## Fourth Example

FourthExample.yaml defines a web application stack hosted on the web_server **Compute** node and the database software stack of previous examples.
The example can be well represented with this image:


The web application stack consists of the **wordpress**, the **apache** and the
**web_server** node templates. The wordpress node template represents a custom web application of type
**tosca.nodes.WebApplication.WordPress** which is hosted on an **Apache** web server,which itself is hosted on web_server **Compute** node.

The connection between **wordpress** and **wordpress_db** nodes is established through the database_endpoint
entry in the requirements section of the **wordpress** node.