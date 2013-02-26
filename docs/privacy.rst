隐私级别
==============

Read the Docs supports 3 different privacy levels on 2 different objects;
Public, Protected, Private on Projects and Versions.

Understanding the Privacy Levels
--------------------------------

+------------+------------+-----------+-----------+
| Level      | Detail     | Listing   | Search    |
+============+============+===========+===========+
| Private    | No         | No        | No        |
+------------+------------+-----------+-----------+
| Protected  | Yes        | No        | No        |
+------------+------------+-----------+-----------+
| Public     | Yes        | Yes       | Yes       |
+------------+------------+-----------+-----------+

公共
~~~~~~

This is the easiest and most obvious. It is also the default.
It means that everything is available to be seen by everyone.

保护
~~~~~~~~~

Protected means that your object won't show up in Listing Pages,
but Detail pages still work. For example, a Project that is Protected will
not show on the homepage Recently Updated list, however,
if you link directly to the project, you will get a 200 and the page will display.

Protected Versions are similar, they won't show up in your version listings,
but will be available once linked to.


隐私
~~~~~~~

Private objects are available only to people who have permissions so see them.
They will not display on any list view, and will 404 when you link them to others.

项目对象
----------------

详细视图
~~~~~~~~~~~~

    * Project Detail (/projects/<slug>)
    * API Detail (/api/v1/project/<slug>/)

列表视图
~~~~~~~~~~

    * Home Page
    * All Projects Page
    * User Profile Page (/profiles/<user>/)
    * Search 


版本对象
----------------

列表视图
~~~~~~~~~~

    * Project Detail (/projects/<slug>)
    * Version Selector on Home page
    * Version Selector on Documentation page
    * Search 
