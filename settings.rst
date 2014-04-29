.. include:: definitions.inc

.. _settings:

Settings
========

Settings can be accessed via the *Preferences > Package Settings > Javatar* from menu bar or via command palette by type ``Preference Javatar``.

Default settings should not be modified. However, you can copy the relevant settings into |J|'s user settings file.

Some settings contain macro for special value such as Source Folder or Project Directory. The followings are all macro supported by |J|...

 * Available anywhere
    * ``$project_dir``
       * Project Directory
    * ``$source_folder``
       * Source folder
    * ``$packages_path``
       * |st|'s packages path
    * ``$sep``
       * Path separator. Such as "/" on Unix and "\\" on Windows
 * Available when open a file
    * ``$full_class_path``
       * Full class path. Such as "package.subpackage.classname"
    * ``$package``
       * Current package. Such as "package.subpackage"
    * ``$class_name``
       * Current class name. Such as "classname"
 * Available when open a file on specific context (such as build or run)
    * ``$file``
       * Full path to file. Such as "/Users/home/File.java"
    * ``$file_parent``
       * Full path of parent directory. Such as "/Users/home/"
    * ``$file_name``
       * File name. Such as "File.java"
    * ``$sourcepath``
       * Source path flag for build command (-sourcepath)
    * ``$classpath``
       * Class path flag for build and run command (-classpath)
    * ``$d``
       * Output path flag for build command (-d)

.. note:: Make sure you are quoted all path specific value to escape spaces.