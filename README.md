## Backload
===========
**Backload** is a professional, full featured ASP.NET MVC 4 file upload controller and handler (server side). It has been developed as part of a commercial product for the aero craft industry. 
While Backload out of the  box handles the client side [jQuery File Upload Plugin](https://github.com/blueimp/jQuery-File-Upload) from blueimp, it can be easily customized to work with any client side plugin (e.g. [PlUpload](https://github.com/moxiecode/plupload) from Moxiecode, see [Example 09](https://github.com/blackcity/Backload/wiki/Example-10) or [Example 10](https://github.com/blackcity/Backload/wiki/Example-10).

### Roadmap
#### Extensions
Starting with release 1.8.0 we open up the Backload component for extensions (plugins) using .NET MEF (Managed Extensibility Framework) which is part of the .NET Framework. The extensions are very easy to write and clean up the code drastically. You'll be able to hook into several steps through the entire processing pipeline. Extensions can be added, deleted and renamed within the Extensions folder while the MVC application is running. Use Cases: Manipulate incoming data before it is processed, store incoming files in multiple locations, use a custom cloud storage, perform additional image processing and many more.
#### Cloud storage
Cloud storage will mark our next milestone. We start with giving you the basic means storing data in a cloud storage in the same manner Backload provides for the local file system or databases. Then we will support popular cloud storage providers out of the box. Help is much appreciated! Don't hesitate to show us your code or help develop cloud storage extensions. 

### Highlights

**Backload** is a feature rich server side component which can be fully customized (declaratively) within the web.config file (resp. a linked config file). Complex storage structures are supported and handled by the component without a single line of code, whether the storage location is the file system or a database. If you want to upload different file types (images, pdfs, doc, etc) content type based subfolders can be configured to automatically store different file types in different sub folders (e.g. /images, /pdfs, /movies, etc).

The zero configuration feature allows quick setups, a default MVC controller is ready to handle incoming requests. For more complex scenarios, where you have to run your own business logic, you can derive from the default controller or call the handler method from your code. 

**Backload** supports cropping and resizing of images. The parameters can be set within the web.config file or by an incoming request from the client. Multiple image manipulation features are implemented. Type conversion is also supported.

**Backload** can create unique file names (GUIDs). So files cannot be overwritten or, if this is the purpose of using this feature, cannot be accessed from the web without knowledge of the new name. Mapping of the original file name to the new file name and back is also implemented. This feature can be used to send a friendly name back to the client. 

**Backload** is extensible. Extensions are normal, easy to write classes, implementing a simple interface and decorated with an ExportAttribute. Using extensions is a very cheap process regarding system resources. They are very good testable, scalable, isolate code and can be dynamically added and removed while the MVC app is running. You may want to add a new functionality (e.g. exception logging, change client side plugin, etc.) or perform tests without changing or stopping the application (See examples 08+).

**Backload** has proven its scalability in production with hundreds of thousands uploads a day. Internally it is designed to work asynchronously where possible and it supports and encourages the development of asynchronous extensions.

### Features
* Zero configuration: The defaults set up a fully functional server side file upload controller and handler.
* Declarative configuration: Features will be setup within the web.config or a linked config file.
* Storage context: Supported locations are file system and databases (by the Entity Framework) and cloud (next milestone).
* Object context based locations: Based on the context (e.g. UserX, UserY, ArtistX, ArtistY, HouseA, HouseB) different storage locations can automatically be routed.
* Content type subfolders: Based on the content type files can automatically be stored in an appropriate subfolder. This feature is fully customizable.
* Unique file names: Files can be stored with a unique name and also remapped to their original name.
* Cropping and resizing: This can be setup in the web.config file or in a request from the client.
* Image type conversion: Images can be converted to a different target type.
* Security: Access control with authentication and authorization (roles based).
+ Extensibility (coming release): Dynamically hook in your own extensions. (Multiple extensions for a specific processing step are supported).
+ Scalability by asynchronous internal code and asynchronous support for extensions.

### Setup
[Setup instructions](https://github.com/blackcity/Backload/wiki/Setup)

### Configuration
[Options, settings and enumerations](https://github.com/blackcity/Backload/wiki/Configuration)

### Examples
[Example 01: Zero configuration](https://github.com/blackcity/Backload/wiki/Example-01)<br />
[Example 02: Configuration basics: Using web.config](https://github.com/blackcity/Backload/wiki/Example-02)<br />
[Example 03: Configuration basics: Using an external config file](https://github.com/blackcity/Backload/wiki/Example-03)<br />
[Example 04: Using your own controllers](https://github.com/blackcity/Backload/wiki/Example-04)<br />
[Example 05: Using server side image manipulation features](https://github.com/blackcity/Backload/wiki/Example-05)<br />
[Example 06: Managing subfolders: Using the object context](https://github.com/blackcity/Backload/wiki/Example-06)<br />
[Example 07: Managing subfolders: Using the upload context](https://github.com/blackcity/Backload/wiki/Example-07)<br />
[Example 08: Extensibility: Writing a simple extension](https://github.com/blackcity/Backload/wiki/Example-08)<br />
[Example 09: Extensibility: Handle and extend the PlUpload plugin (Moxiecode)](https://github.com/blackcity/Backload/wiki/Example-09)<br />
[Example 10: Handling exceptions](https://github.com/blackcity/Backload/wiki/Example-10)<br />
[Example 11: Asynchronous operations with async/await, Tasks and Threads](https://github.com/blackcity/Backload/wiki/Example-11)

### Demo: JQuery File Upload Plugin (original demo) with Backload
The original demo shipped with the JQuery File Upload Plugin working with the Backload the server side component can be found [here](https://github.com/blackcity/Backload/tree/master/Examples/Demos_by_bluimp).  

###News, releases, plans and more
Follow us on Twitter (just started) [@Backload_MVC](https://twitter.com/backload_mvc)

### License
[Backload. (Standard version)](https://github.com/blackcity/Backload): Copyright 2013, Steffen Habermehl, License (Standard version): MIT license<br />
Professional and Enterprise (source code) version are available under a commercial license.<br/>
Follow us on Twitter: [@Backload_MVC](https://twitter.com/backload_mvc)

