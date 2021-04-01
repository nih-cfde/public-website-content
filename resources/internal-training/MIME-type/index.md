A MIME type or media type is a form of identification for file formats and contents transmitted over the internet. It is useful to specify the data identification label of a file to allow software to properly interpret and render the data. This is especially important for Common Fund (CF) programs who may undertake data transfers over the internet and thus, have to ensure the data integrity along with data formats for a successful transfer. In this tutorial, we will describe how to determine MIME type for single and multiple files, and create custom MIME types specific to the file format.

Est. Time | Lesson name | Description
--- | --- | ---
5 mins | [Introduction](https://www.nih-cfde.org/resource/intro-mime-type) | What is a MIME type ?
15 mins | [Example Data](https://www.nih-cfde.org/resource/example-data-files) | Obtain general or CF specific data files
5 mins | [file](https://www.nih-cfde.org/resource/file) | MIME type using file
10 mins | [mimetype](https://www.nih-cfde.org/resource/mimetype) | MIME type using mimetype
10 mins | [xdg-utils](https://www.nih-cfde.org/resource/xdg-utils) | MIME type using xdg-utils
15 mins | [Siegfried](https://www.nih-cfde.org/resource/siegfried) | MIME type using Siegfried
5 mins  | [Multi File MIME type ](https://www.nih-cfde.org/resource/multiple-file-mime) | MIME type for multiple files
10 mins | [Unexpected Behavior](https://www.nih-cfde.org/resource/unexpected-behavior) | Understand and validate MIME type

> #### Learning Objectives
> In this tutorial you will learn:
>
> - how to determine MIME type for single and multiple files
> - about different utilities for MIME type identification
> - how to create custom MIME types
> - how to validate MIME types for unknown file formats

#### Prerequisites
This tutorial is written for a Unix/Linux compute environment (e.g. HPC, binder, cloud platforms like AWS, XSEDE etc). **The code included in the tutorial will not work on MacOS/X.** Some of the commands require super user privileges or permissions to use `sudo`.
