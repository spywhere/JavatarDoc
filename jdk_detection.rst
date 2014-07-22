.. include:: definitions.inc

.. _jdk_detection:

JDK Detections
==============

At startup time, |J| will automatically detect installed JDK on your computer and select the best one.

Here are the steps it takes to select the best JDK for most projects...

 1. Run a checking command to see that Java has been setup as default
 2. Search all JDK directories in installation path (depends on your OS)
 3. If Java is already setup, use the default one. And set all available JDK version to settings (as your JDK settings)
 4. If Java is not setup yet, use the latest version that available
 5. If Java is not setup and there is no Java installed, |J| will notify that you did not install Java yet

If you install Java anywhere else, you can set how |J| search and detect JDK by setting it in |J|'s user preferences.
