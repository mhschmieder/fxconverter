# FxConverterToolkit
FxConverterToolkit is a toolkit for converting JavaFX based graphics and GUI elements to various vector graphics output formats such as EPS, SVG and PDF, via intermediary transcoding to AWT using the excellent JFXConverter library by Hervé Girod, which allows one to connect legacy AWT-based Java libraries to JavaFX application elements.

Although the JFXConverter library has its own drivers and extensions for the supported file formats, I needed to switch to better libraries for each vector graphics target and to have this code all available in a coordinated release with my other libraries. It is possible that this library may go away later on if Hervé likewise switched the source libraries for the EPS, SVG and PDF generation.

Maven support will hopefully be added within the next day or two.
