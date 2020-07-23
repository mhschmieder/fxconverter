# FxConverterToolkit
FxConverterToolkit is a toolkit for converting JavaFX based graphics and GUI elements to various vector graphics output formats such as EPS, SVG and PDF, via intermediary transcoding to AWT using the excellent JFXConverter library by Hervé Girod, which allows one to connect legacy AWT-based Java libraries to JavaFX application elements.

Although the JFXConverter library has its own drivers and extensions for the supported file formats, I needed to switch to better libraries for each vector graphics target and to have this code all available in a coordinated release with my other libraries. It is possible that this library may go away later on if Hervé likewise switches his source libraries for EPS and SVG (the latter currently uses Batik, which is very old and hard to maintain integration compatibility) and adds PDF support (this is my most important output format overall, and is meant to eventually supplant the need for EPS).

Eclipse and NetBeans related support files are included as they are generic and are agnostic to the OS or to the user's system details and file system structure, so it seems helpful to post them in order to accelerate the integration of this library into a user's normal IDE project workflow and build cycle.

The Javadocs are 100% compliant and complete, but I am still learning how to publish those at the hosting site that I think is part of Maven Central, as it is a bad idea to bloat a GitHub project with such files and to complicate repository changes (just as with binary files and archices). Hopefully later tonight!

This projects depends on my GraphicsToolkit and EpsToolkit libraries, as well as depending on Object Refinery's JFreeSVG and Orson PDF libraries, along with the JFXConverter library, and is marked as such in the Maven POM file.

Please note that for now my forks must be used for both external dependencies, as I had to modify the POM in order to specify Java 1.8 vs. Java 11 (JFreeSVG) andr Java 1.6 (OrsonPDF), and switch to a compatible Maven plug-in version in a couple of items in the POM, as well as correct some inconsistencies in the Group ID and Artifact ID.

Those changes aren't likely to get merged, as Java 11 is Object Refinery's current target and they have rebranded OrsonPDF as the more consistent name of JFreePDF going forward, thus I do not think they have an interest in posting OrsonPDF as a Java 1.8 compatible library. I may check with them directly though. Some vendors offer multiple forks for different Java compliance levels; COntrolsFX comes to mind as they have to maintain Java 1.8 until they are 100% migrated to Java 13+.
