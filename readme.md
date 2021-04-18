<head xmlns="http://www.w3.org/1999/xhtml">
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8"/>
<title>Eclipse Project Release Notes 4.19</title>
<!-- Please validate as "xhtml1 strict", at
https://validator.w3.org/check?uri=http%3A%2F%2Fwww.eclipse.org%2Feclipse%2Fdevelopment%2Freadme_eclipse_4.19.html;ss=1
(It must be "on website" to validate.)
-->
</head>
<body xmlns="http://www.w3.org/1999/xhtml">
  <h1>
    <a class="mozTocH1" name="mozTocId299852" id="mozTocId299852">Eclipse Project Release Notes</a>
  </h1>
  <p>
    <a class="mozTocH1" name="mozTocId299852" id="mozTocId299852">Release 4.19</a>
  </p>
  <p>
    <a class="mozTocH1" name="mozTocId299852" id="mozTocId299852">Last revised February 21, 2020</a>
  </p>
  <!-- 
This following link to www.eclipse.org should be commented out
or removed in final version of the 
"web version" of the readme, since it does not make sense to 
have there. But in the "product's readme" it will point people 
to "the latest version" since there _might_ be changes made 
after the release.
  <p>
    The latest version of this document can be found on the web at <a href="https://www.eclipse.org/eclipse/development/readme_eclipse_4.19.php">Eclipse Release Notes 4.19</a>. There may or may
    not be changes made after the product is released. You can tell by checking the "last revised" date near the top of this page.
  </p>
-->

  <p style="text-align: left; font-weight: bold;">
    <a class="mozTocH1" name="mozTocId299852" id="mozTocId299852"> This software is OSI Certified Open Source Software.<br/> OSI Certified is a certification mark of the Open Source Initiative.
    </a>
  </p>
  <h2 id="TargetOperatingEnvironments1">
    <a class="mozTocH2" name="mozTocId438134" id="mozTocId438134"/>
  </h2>
  <ol id="mozToc">
    <!--mozToc h1 1 h2 2 h3 3 h4 4 h5 5 h6 6--><li><a href="#mozTocId299852">Eclipse Project Release Notes</a><ol><li><a href="#mozTocId315234">Target Operating Environments</a></li><li><a href="#mozTocId569479">Compatibility with Previous Releases</a><ol><li><a href="#mozTocId324309">Compatibility of Release 4.19 with 4.18</a></li></ol></li><li><a href="#mozTocId214943">Known Issues</a><ol><li><a href="#mozTocId758150">General problems</a></li><li><a href="#mozTocId559320">General - Startup</a><ol><li><a href="#mozTocId693657">Installation/Configuration issues that can cause Eclipse to fail start</a></li><li><a href="#mozTocId337416"> Invalid characters in install directory prevents Eclipse from starting </a></li><li><a href="#mozTocId639565">Hanging during class loading when out of permanent generation memory</a></li></ol></li><li><a href="#mozTocId148479">General - GCJ</a><ol><li><a href="#mozTocId584602">Problems with classloaders in created threads</a></li><li><a href="#mozTocId403443">Deadlock creating executable extension in Plugin.startup</a></li><li><a href="#mozTocId984286">Potential Problems Converting Plug-in Manifests</a></li><li><a href="#mozTocId993987">Location for Debug Options File on Mac OS</a></li><li><a href="#mozTocId808188">Issues with JNI that use FindClass</a></li></ol></li><li><a href="#mozTocId324774">Platform - Ant</a><ol><li><a href="#mozTocId480194">Custom Ant tasks and Ant types must be separate from plug-in library JARs</a></li><li><a href="#mozTocId912215">XDoclet support from within Eclipse</a></li><li><a href="#mozTocId31051">Ant Editor code completion based on Ant 1.6.x</a></li><li><a href="#mozTocId925603">Setting build loggers not supported when debugging Ant builds</a></li><li><a href="#mozTocId669417">Renaming an External Tool builder set to run during auto-build will cause errors</a></li><li><a href="#mozTocId772119">Slow typing/saving of the Ant editor with imports that define numerous macrodefs</a></li><li><a href="#mozTocId715004">Ant 1.8.x reports missing libraries as build failures</a></li></ol></li><li><a href="#mozTocId876322">Platform - User Assistance</a><ol><li><a href="#mozTocId828477">Welcome page not displayed properly (Linux/Unix)</a></li><li><a href="#mozTocId26110">Help browser tool bar buttons do not work for some documents</a></li><li><a href="#mozTocId324012">Help documents not displayed in a browser or very slow document loading (Windows only)</a></li><li><a href="#mozTocId227368">Working disconnected from the network (Windows only)</a></li><li><a href="#mozTocId121403">Using Internet Explorer in offline mode (Windows only)</a></li></ol></li><li><a href="#mozTocId683637">Platform - UI</a><ol><li><a href="#mozTocId348035">Dirty state not tracked properly for OLE documents (Windows only)</a></li><li><a href="#mozTocId878052">OLE document crashes can cause Eclipse to also crash (Windows only)</a></li><li><a href="#mozTocId452707">Toolbars only containing contributed controls exhibit display errors on Mac/Linux</a></li><li><a href="#mozTocId443682">Allocating enough memory and solving OutOfMemoryError</a></li><li><a href="#mozTocId862142">Capabilities and Activities don't affect the menus and toolbars</a></li></ol></li><li><a href="#mozTocId554478">Platform - SWT</a><ol><li><a href="#mozTocId565691">Support for macOS 11 (Big Sur)</a></li><li><a href="#mozTocId534426">Usage of swt.autoScale and GDK_SCALE flag on GTK platforms</a></li><li><a href="#mozTocId554478">Non-uniform scaling of text vs. icons when using intermediate scaling factors on high-DPI displays</a></li><li><a href="#mozTocId69222">Eclipse plug-in based on the SWT Browser throws exception</a></li><li><a href="#mozTocId238090">Eclipse icon is duplicated in task-bar on Windows</a></li><li><a href="#mozTocId414883">BIDI Segments in Text controls</a></li><li><a href="#mozTocId518357">Block Selection functionality provided by StyledText is not BIDI aware</a></li></ol></li><li><a href="#mozTocId805874">Platform - Install/Update</a><ol><li><a href="#mozTocId914600">Manually installing features and plug-ins on a FAT file system (Windows only)</a></li><li><a href="#mozTocId648565">Connecting to untrusted sites using https</a></li><li><a href="#mozTocId104394">Extension location is lost if the install path changes</a></li></ol></li><li><a href="#mozTocId428861">Java development tools (JDT)</a><ol><li><a href="#mozTocId180305">Multiple regions formatting in a given source snippet</a></li><li><a href="#mozTocId589358">Searching for constant field references</a></li><li><a href="#mozTocId577868">Cut, copy, paste not working for linked resources in views showing Java elements</a></li><li><a href="#mozTocId554543">Java working sets not working correctly for elements from JRE system library container</a></li><li><a href="#mozTocId157019">Breakpoints unreliable running Sun 1.6.0_14</a></li><li><a href="#mozTocId440090">Suspend on uncaught exception overrides exception breakpoint location filters</a></li><li><a href="#mozTocId812347">Running Java programs with non-Latin-1 characters in package or class names</a></li><li><a href="#mozTocId638407">Cannot run or debug class in a project with GB18030 characters in project name</a></li><li><a href="#mozTocId994970">Cannot detect installed JRE with GB18030 characters in path name</a></li><li><a href="#mozTocId324283">Cannot generate Javadoc for packages with GB18030 characters in the name</a></li><li><a href="#mozTocId524553">Unable to debug stack overflows</a></li><li><a href="#mozTocId162517">Evaluation limitation</a></li><li><a href="#mozTocId408387">Missing debug attributes</a></li><li><a href="#mozTocId330034">Using Hot Code Replace</a></li><li><a href="#mozTocId976120">Scrapbook</a></li><li><a href="#mozTocId666507">Debugging over slow connections</a></li><li><a href="#mozTocId207158">Updating of inspected values</a></li><li><a href="#mozTocId821393">Stepping over native methods that perform I/O</a></li><li><a href="#mozTocId606104">Java Annotation Processing</a></li><li><a href="#mozTocId188069">Java indexing encounters problems when a folder is used both as a source and a class folder</a></li></ol></li><li><a href="#mozTocId25456">Plug-in Development Environment (PDE)</a><ol><li><a href="#mozTocId179699">Feature manifest editor does not preserve all comments</a></li><li><a href="#mozTocId243421">PDE will not unzip source zips of some plug-ins</a></li><li><a href="#mozTocId722932">Emacs key bindings do not work in manifest editor fields</a></li><li><a href="#mozTocId828449">Export of plug-in may silently drop classes</a></li><li><a href="#mozTocId89714">Compilation errors when exporting projects not stored outside of the workspace</a></li><li><a href="#mozTocId270371">Headless build needs to be run from a fully qualified path</a></li><li><a href="#mozTocId73293">Importing in Eclipse application fails if plug-in exists in host workspace</a></li><li><a href="#mozTocId914239">Reusing a workspace after changing architectures silently breaks PDE models</a></li><li><a href="#mozTocId624312">Missing @since tag API Tools problems on interface fields containing @noreference tag</a></li></ol></li></ol></li></ol></li><li><a href="#mozTocId19817">Running Eclipse</a><ol><li><a href="#mozTocId60052">Allocating enough memory and solving OutOfMemoryErrors</a></li><li><a href="#mozTocId735187">Selecting a workspace</a></li><li><a href="#mozTocId620725">Specifying the Java virtual machine</a></li><li><a href="#mozTocId928700">Mac OS X</a></li><li><a href="#mozTocId221199">Shared Install</a></li></ol></li><li><a href="#mozTocId575572">Upgrading Workspace from a Previous Release</a><ol><li><a href="#mozTocId401691">Users who don't use "-data"</a></li><li><a href="#mozTocId197750">Users who do use "-data"</a></li><li><a href="#mozTocId839433">Users who use User Libraries or classpath containers that contain JARs referencing other libraries via Class-Path in the MANIFEST.MF</a></li><li><a href="#mozTocId623237">Dropped in bundles may not resolve after upgrade</a></li></ol></li><li><a href="#mozTocId638978">Interoperability with Previous Releases</a><ol><li><a href="#mozTocId759237">Interoperability of Release 4.19 with previous releases</a><ol><li><a href="#mozTocId226004">Sharing projects between heterogeneous Eclipse 4.19 and 4.18</a></li><li><a href="#mozTocId574781">Using Eclipse 4.19 to develop plug-ins that work in Eclipse 4.18</a></li></ol></li></ol></li><li><a href="#mozTocId317294">Appendix: Execution Environment by Bundle</a></li></ol><h2 id="TargetOperatingEnvironments2">
    <a class="mozTocH2" name="mozTocId315234" id="mozTocId315234"/>Target Operating Environments
  </h2>
  <p>In order to remain current, each Eclipse Project release targets reasonably current operating environments.</p>
  <p>Most of the Eclipse SDK is "pure" Java code and has no direct dependence on the underlying operating system. The chief dependence is therefore on the Java Platform itself. Portions are
    targeted to specific classes of operating environments, requiring their source code to only reference facilities available in particular class libraries (e.g. J2ME Foundation 1.1, J2SE 1.4, Java
    5, etc).</p>
  <p>In general, the 4.19 release of the Eclipse Project is developed on Java SE 11 VMs. As such, the Eclipse SDK as a whole is targeted at all modern, desktop Java VMs.</p>
  <p>
    <a href="#appendix">Appendix 1</a> contains a table that indicates the class library level required for each bundle.
  </p>
  <p>
    There are many different implementations of the Java Platform running atop a variety of operating systems. We focus our testing on a handful of popular combinations of operating system and Java
    Platform; these are our <em>reference platforms</em>. Eclipse undoubtedly runs fine in many operating environments beyond the reference platforms we test. However, since we do not systematically
    test them we cannot vouch for them. Problems encountered when running Eclipse on a non-reference platform that cannot be recreated on any reference platform will be given lower priority than
    problems with running Eclipse on a reference platform.
  </p>
  <p>
    Eclipse 4.19 is tested and validated on a number of reference platforms. For the complete list, see <a href="https://www.eclipse.org/projects/project-plan.php?planurl=http://www.eclipse.org/eclipse/development/plans/eclipse_project_plan_4_19.xml#target_environments">Target Environments in the
      4.19 Plan</a>.
  </p>
  <p>
    As stated above, <i>we expect that Eclipse works fine on other current Java VM and OS versions but we cannot flag these as reference platforms without significant community support for testing
      them.</i>
  </p>
  <p>The Eclipse SDK is designed as the basis for internationalized products. The user interface elements provided by the Eclipse SDK components, including dialogs and error messages, are
    externalized. The English strings are provided as the default resource bundles.</p>
  <p>Latin-1, DBCS, and BiDi locales are supported by the Eclipse SDK on all reference platforms.</p>
  <p>The Eclipse SDK supports GB 18030 (level 1), the Chinese code page standard, on Windows, Linux and the Macintosh.</p>
  <p>German and Japanese locales are tested.</p>
  <h2 id="Compatibility">
    <a class="mozTocH2" name="mozTocId569479" id="mozTocId569479">Compatibility with Previous Releases</a>
  </h2>
  <h3>
    <a class="mozTocH3" name="mozTocId324309" id="mozTocId324309">Compatibility of Release 4.19 with 4.18</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId324309" id="mozTocId324309">Eclipse 4.19 is compatible with Eclipse 4.18 (and all earlier 4.x and 3.x versions).</a>
  </p>
  <p>
    <a class="mozTocH3" name="mozTocId324309" id="mozTocId324309"> <strong>API Contract Compatibility:</strong> Eclipse SDK 4.19 is upwards contract-compatible with Eclipse SDK 4.18 except in those areas noted in the
    </a><a href="http://www.eclipse.org/eclipse/development/porting/eclipse_4_19_porting_guide.html"><em>Eclipse 4.19 Plug-in Migration Guide</em></a>. Programs that use affected APIs and extension points
    will need to be ported to Eclipse SDK 4.19 APIs. Downward contract compatibility is not supported. There is no guarantee that compliance with Eclipse SDK 4.19 APIs would ensure compliance with
    Eclipse SDK 4.18 APIs. Refer to <a href="https://wiki.eclipse.org/Evolving_Java-based_APIs"><em>Evolving Java-based APIs</em></a> for a discussion of the kinds of API changes that maintain contract
    compatibility.
  </p>
  <p>
    <strong>Binary (plug-in) Compatibility:</strong> Eclipse SDK 4.19 is upwards binary-compatible with Eclipse SDK 4.18 except in those areas noted in the <a href="http://www.eclipse.org/eclipse/development/porting/eclipse_4_19_porting_guide.html"><em>Eclipse 4.19 Plug-in Migration Guide</em> </a>. Downward plug-in compatibility is not supported.
    Plug-ins for Eclipse SDK 4.19 will not be usable in Eclipse SDK 4.18. Refer to <a href="https://wiki.eclipse.org/Evolving_Java-based_APIs"> <em>Evolving Java-based APIs</em></a> for a discussion of
    the kinds of API changes that maintain binary compatibility.
  </p>
  <p>
    <strong>Source Compatibility:</strong> Eclipse SDK 4.19 is upwards source-compatible with Eclipse SDK 4.18 except in the areas noted in the <a href="http://www.eclipse.org/eclipse/development/porting/eclipse_4_19_porting_guide.html"><em>Eclipse 4.19 Plug-in Migration Guide</em> </a>. This means that source files written to use Eclipse
    SDK 4.19 APIs might successfully compile and run against Eclipse SDK 4.18 APIs, although this is not guaranteed. Downward source compatibility is not supported. If source files use new Eclipse SDK
    APIs, they will not be usable with an earlier version of the Eclipse SDK.
  </p>
  <p>
    <strong>Workspace Compatibility:</strong> Eclipse SDK 4.19 is upwards workspace-compatible with earlier 3.x and 4.x versions of the Eclipse SDK unless noted. This means that workspaces and projects
    created with Eclipse SDK 4.18, 4.17, 4.16, 4.15, 4.14, 4.13, 4.12, 4.11, 4.10, 4.9, 4.8, 4.7, 4.6, 4.5 and 4.4 can be successfully opened by Eclipse SDK 4.19 and upgraded to a 4.19 workspace. This includes both hidden metadata, which is localized to a
    particular workspace, as well as metadata files found within a workspace project (e.g., the .project file), which may propagate between workspaces via file copying or team repositories. Individual
    plug-ins developed for Eclipse SDK 4.19 should provide similar upwards compatibility for their hidden and visible workspace metadata created by earlier versions; 4.19 plug-in developers are
    responsible for ensuring that their plug-ins recognize metadata from earlier versions and process it appropriately. User interface session state may be discarded when a workspace is upgraded.
    Downward workspace compatibility is not supported. A workspace created (or opened) by a product based on Eclipse 4.19 will be unusable with a product based on an earlier version of Eclipse. Visible
    metadata files created (or overwritten) by Eclipse 4.19 will generally be unusable with earlier versions of Eclipse.
  </p>
  <p>
    <strong>Non-compliant usage of API's</strong>: All non-API methods and classes, and certainly everything in a package with "internal" in its name or x-internal in the bundle manifest entry, are
    considered implementation details which may vary between operating environment and are subject to change without notice. Client plug-ins that directly depend on anything other than what is
    specified in the Eclipse SDK API are inherently unsupportable and receive no guarantees about compatibility within a single release much less with earlier releases. Refer to <a href="https://www.eclipse.org/articles/Article-API-Use/index.html"> <em>How to Use the Eclipse API</em></a> for information about how to write compliant plug-ins.
  </p>
  <h2 id="KnownIssues">
    <a class="mozTocH2" name="mozTocId214943" id="mozTocId214943">Known Issues</a>
  </h2>
  <p>
    <a class="mozTocH2" name="mozTocId214943" id="mozTocId214943"> Note: Bug numbers refer to the Eclipse project bug database at </a><a href="http://dev.eclipse.org/bugs/">http://bugs.eclipse.org/bugs/</a>
  </p>
  <h3 id="I-General">
    <a class="mozTocH3" name="mozTocId758150" id="mozTocId758150">General problems</a>
  </h3>
  <h3 id="I-General-Startup">
    <a class="mozTocH3" name="mozTocId559320" id="mozTocId559320">General - Startup</a>
  </h3>
  <h4>
    <a class="mozTocH4" name="mozTocId693657" id="mozTocId693657">Installation/Configuration issues that can cause Eclipse to fail start</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId693657" id="mozTocId693657">Here are some common problems that can cause Eclipse not to start:</a>
  </p><ul><li>Running Eclipse with Java SE 9 and above may require additional configuration. Please refer to <a href="https://wiki.eclipse.org/Configure_Eclipse_for_Java_9">this page</a> for more details.</li><li><a class="mozTocH4" name="mozTocId693657" id="mozTocId693657">As shown </a><a href="#TargetOperatingEnvironments">above</a>, Eclipse 4.19 requires at least a Java SE 11. Perhaps an older version of the VM is being found in your path. To
      explicitly specify which VM to run with, use the Eclipse <code>-vm</code> command-line argument. (See also the <a href="#RunningEclipse">Running Eclipse</a> section below.)</li><li>Running Eclipse on Gentoo Linux may result in the following error message:
      <div style="margin-left: 40px;">
        <code>
          * run-java-tool is not available for sun-jdk-1.6 on i686<br/> * IMPORTANT: some Java tools are not available on some VMs on some architectures
        </code>
      </div> If this occurs, start Eclipse by specifying a -vm argument, either specify the path to a java vm or use: <code>eclipse -vm `java-config</code> --java` (bug <a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=176021">176021</a>)</li><li>Eclipse must be installed to a clean directory and not installed over top of a previous installation. If you have done this then please re-install to a new directory. If your workspace is
      in a child directory of your old installation directory, then see the instructions below on "<a href="#Upgrading">Upgrading Workspace from a Previous Release"</a>.</li><li>Java sometimes has difficulty detecting whether a file system is writable. In particular, the method java.io.File.canWrite() appears to return true in unexpected cases (e.g., using
      Windows drive sharing where the share is a read-only Samba drive). The Eclipse runtime generally needs a writable configuration area and as a result of this problem, may erroneously detect the
      current configuration location as writable. The net result is that Eclipse will fail to start and depending on the circumstances, may fail to write a log file with any details. To work around
      this, we suggest users experiencing this problem set their configuration area explicitly using the <code>-configuration</code> command line argument. (bug <a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=67719">67719</a>)</li></ul><h4>
    <a class="mozTocH4" name="mozTocId337416" id="mozTocId337416"> <b>Invalid characters in install directory prevents Eclipse from starting</b>
    </a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId337416" id="mozTocId337416"> Eclipse will fail to launch if installed in a directory whose path contains certain invalid characters, including :%#&lt;>"!. The workaround is to install Eclipse
      in a directory whose path does not contain invalid characters. (bugs </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=3109">3109</a> and <a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=17281">17281</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId639565" id="mozTocId639565">Hanging during class loading when out of permanent generation memory</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId639565" id="mozTocId639565"> The Oracle JVM may hang indefinitely during class loading if it runs out of permanent generation memory. This will cause CPU usage to stay at 100% until the process is
      ended. See the section </a><a href="#RunningEclipse">Running Eclipse</a> for details on addressing this VM problem.
  </p>
  <h3 id="I-General-GCJ">
    <a class="mozTocH3" name="mozTocId148479" id="mozTocId148479">General - GCJ</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId148479" id="mozTocId148479">GCJ is an effort by the GCC team to provide an open source Java compiler and runtime environment to interpret Java bytecode. Unfortunately, the GCJ runtime environment
      is not an environment that is often tested on by Eclipse developers.</a>
  </p>
  <p>
    <a class="mozTocH3" name="mozTocId148479" id="mozTocId148479">The most common problems surrounding GCJ are:</a>
  </p><ul><li><a class="mozTocH3" name="mozTocId148479" id="mozTocId148479">Eclipse does not start at all</a></li><li><a class="mozTocH3" name="mozTocId148479" id="mozTocId148479">Eclipse throws a 'java.lang.ClassNotFoundException: org.eclipse.core.runtime.Plugin' that can be found in the logs (located in workspace/.metadata/.log)</a></li></ul><p>
    <a class="mozTocH3" name="mozTocId148479" id="mozTocId148479"> The workspace's log file is a good place to check to identify whether GCJ is being used or not. Every Eclipse log session is prepended with information about the
      runtime environment that was used to run Eclipse. The log may include something like the following: <code>java.fullversion=GNU libgcj 4.2.1 (Debian 4.2.1-5)</code>
    </a>
  </p>
  <p>
    <a class="mozTocH3" name="mozTocId148479" id="mozTocId148479"> If Eclipse does start, one can check which runtime environment is being used to run Eclipse by going to <b>Help > About Eclipse SDK > Installation Details
        > Configuration</b>. The <b>About</b> dialog itself can also provide other information, the build identifier can be of particular interest as it is tagged by some distributions. This allows the
      user to identify whether Eclipse was downloaded through the distribution's package management system or directly from the eclipse.org web site. <br/> Such as:<br/> <code>Build id:
        M20070212-1330 (Ubuntu version: 3.2.2-0ubuntu3)</code>
    </a>
  </p>
  <p>
    <a class="mozTocH3" name="mozTocId148479" id="mozTocId148479">The two most common workarounds are:</a>
  </p><ul><li><a class="mozTocH3" name="mozTocId148479" id="mozTocId148479">download the Eclipse binary from eclipse.org directly</a></li><li><a class="mozTocH3" name="mozTocId148479" id="mozTocId148479">run Eclipse using an alternate Java runtime environment</a></li></ul><p>
    <a class="mozTocH3" name="mozTocId148479" id="mozTocId148479">To download Eclipse, try one of the links below:</a>
  </p><ul><li><a href="http://www.eclipse.org/downloads/">http://www.eclipse.org/downloads/</a></li><li><a href="http://download.eclipse.org/eclipse/downloads/">http://download.eclipse.org/eclipse/downloads/</a></li></ul><p>
    It is imperative that 64-bit builds are downloaded and used if a 64-bit Java runtime environment has been installed. Below is a sample tarball names of version 4.19 of the Eclipse SDK packaged
    for 64-bit processors.<br/>
    <code>eclipse-SDK-4.19-linux-gtk-x86_64.tar.gz (64-bit)</code>
  </p>
  <p>
    To run Eclipse with an alternate Java runtime environment, the path to the Java virtual machine's binary must be identified. With an Eclipse installation from the distribution, altering the $PATH
    variable to include the path to the alternate Java runtime environment is often not enough as the Eclipse that Linux distributions package often performs a scan internally to pick up GCJ by itself
    whilst ignoring what's on the $PATH. An example of the terminal's output is shown below:<br/>
    <code>
      searching for compatible vm...<br/> testing /usr/lib/jvm/java-gcj...found
    </code>
  </p>
  <p>
    Once the path to the virtual machine's binary has been identified, try running Eclipse with the following command:<br/>
    <code>./eclipse -vm /path/to/jre/bin/java</code>
  </p>
  <p>
    For an actual example, it might look something like the following:<br/>
    <code>
      ./eclipse -vm /usr/lib/jvm/java-11/bin/java<br/> ./eclipse -vm /opt/jdk-11/bin/java
    </code>
  </p>
  <p>
    If this seems to solve the problem, it is likely that the problem really was related to the use of GCJ as the Java runtime for running Eclipse. The eclipse.ini file located within Eclipse's folder
    can be altered to automatically pass this argument to Eclipse at startup. An example of its content is presented below:<br/>
    <code>
      -showsplash<br/> org.eclipse.platform<br/> -vm<br/> /opt/jdk-11/bin/java<br/> -vmargs<br/> -Xms256m<br/> -Xmx2048m
    </code>
  </p>
  <p>
    Note that every argument must be on its own line. More information about the eclipse.ini file can be found at <a href="http://wiki.eclipse.org/Eclipse.ini">http://wiki.eclipse.org/Eclipse.ini</a>.
  </p>
  <p>
    If problems persists after downloading an installation of Eclipse from eclipse.org and using a supported Java runtime environment (a list of which may be found <a href="#TargetOperatingEnvironments">above</a>), you can seek further assistance through the <a href="https://www.eclipse.org/forums/">forums</a>, the IRC <a href="irc://irc.freenode.net/#eclipse">channel</a>, and/or <a href="https://bugs.eclipse.org/bugs/">bugzilla</a>.
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId584602" id="mozTocId584602">Problems with classloaders in created threads</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId584602" id="mozTocId584602"> There is a known issue with trying to load classes from a newly-created thread using a class loader different from the plug-in class loader. The result will be a <code>ClassNotFoundException</code>
      . As a workaround, do the following:
    </a>
  </p><ol><li><a class="mozTocH4" name="mozTocId584602" id="mozTocId584602">Create a thread in which to run your code.</a></li><li><a class="mozTocH4" name="mozTocId584602" id="mozTocId584602">Send yourThread.setContextClassLoader(yourClassLoader); // you can find your classloader by grabbing a class it loaded (YourPluginClass.class.getClassLoader())</a></li><li><a class="mozTocH4" name="mozTocId584602" id="mozTocId584602">Run your code in the newly created thread.</a></li></ol><p>
    <a class="mozTocH4" name="mozTocId584602" id="mozTocId584602"> If you set the context class loader for the current thread, you are competing with other users of the thread (all of Eclipse), so the results will be unpredictable.
      However, there should be no problem in practice provided you reset the context class loader back to its original value when your use in the current thread is complete. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=8907">8907</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId403443" id="mozTocId403443">Deadlock creating executable extension in Plugin.startup</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId403443" id="mozTocId403443"> If <code>Plugin.startup</code> code is too complex and performs tasks such as creating an executable extension, a deadlock situation can be created. Only simple
      bookkeeping tasks should be performed in <code>Plugin.startup</code> code. (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=5875">5875</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId984286" id="mozTocId984286">Potential Problems Converting Plug-in Manifests</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId984286" id="mozTocId984286"> If your plug-in ships with a plug-in manifest and not an OSGi bundle manifest, is shipped as a JAR file, and contains a nested JAR file then there may be problems in
      the automatic generation of the bundle manifest file. The packages defined in the nested JAR may not be exported correctly in the <code>Export-packages</code> bundle manifest header. To work
      around this you should ship your plug-in with a bundle manifest. (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=97689">97689</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId993987" id="mozTocId993987">Location for Debug Options File on Mac OS</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId993987" id="mozTocId993987"> If you are running in debug mode on Mac OS, the default location for the .options file is inside the application bundle in the Eclipse.app/Contents/MacOS directory
      (like the eclipse.ini). (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=88782">88782</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId808188" id="mozTocId808188">Issues with JNI that use FindClass</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId808188" id="mozTocId808188"> There may be issues when using a JNI implementation that uses FindClass in a function where the JNIEnv pointer is not available, such as in a C callback (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=125250">125250</a>). The reason is that FindClass, in this case, uses the application class loader to find the class. If the desired class is
    in the classpath used for the application classloader (e.g. defined by the VM argument -cp &lt;classpath>), as it would typically be in a stand-alone application, there is no problem. However,
    under Eclipse, the application classloader does not have access to classes contained in plug-ins. Eclipse uses its own class loader to find classes contained in plug-ins.
  </p>
  <p>The proper plug-in class loader is used by FindClass in JNI functions which are passed the JNIEnv pointer, but not when you have to use AttachCurrentThread to get the JNIEnv pointer. In this
    case the application classloader is used.</p>
  <p>For example, the following will fail because AttachCurrentThread is used to get the JNIEnv pointer:</p>
  <pre>static JavaVM* jvm;  // Global variable<br/><br/>void myCallback(void) {<br/>    JNIEnv* env;<br/>    jvm->AttachCurrentThread((void**)&amp;env, NULL);<br/>    // Fails if some/class is not in the application classloader:<br/>    jclass cls = env->FindClass("some/class");<br/>    jmethodID methodID = env->GetMethodID(cls, "methodName",<br/>      "(Ljava/lang/String;)V or whatever signature");<br/>    env->CallVoidMethod(callback, methodID, ...);<br/>    jvm->DetachCurrentThread();<br/>  }<br/>}</pre>
  <p>A solution is to cache the method ID, for example:</p>
  <pre>static jmethodID mid;  // Global variable<br/><br/>JNIEXPORT jint JNICALL JNI_OnLoad(JavaVM *vm, void *reserved) {<br/>...<br/>  // Store the JavaVM pointer<br/>    jvm = vm;<br/><br/>  // Find the class and store the method ID<br/>  // Will use the class loader that loaded the JNI library<br/>    jclass cls = env->FindClass(className"some/class");<br/>    if(!cls) goto ERR;<br/><br/>    mid = env->GetMethodID(cls, "methodName",<br/>      "(Ljava/lang/String;)V or whatever signature");<br/>    if(!mid) goto ERR;<br/>...<br/>}<br/><br/>void myCallback(void) {<br/>    JNIEnv* env;<br/>    jvm->AttachCurrentThread((void**)&amp;env, NULL);<br/>    env->CallVoidMethod(callback, mid, ...);<br/>     // Handle error ...<br/>    jvm->DetachCurrentThread();<br/>  }<br/>}</pre>
  <h3 id="I-Platform-Ant">
    <a class="mozTocH3" name="mozTocId324774" id="mozTocId324774">Platform - Ant</a>
  </h3>
  <h4>
    <a class="mozTocH4" name="mozTocId480194" id="mozTocId480194">Custom Ant tasks and Ant types must be separate from plug-in library JARs</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId480194" id="mozTocId480194"> Including the class files for custom Ant tasks or Ant types in the regular code JAR for your plug-in causes problems. These class files must be provided in a separate
      JAR that is contributed to the <code>org.eclipse.ant.core.antTasks</code> or <code>antTypes</code> extension point (and not declared as a library in the plug-in's manifest). This ensures that
      the Ant tasks and types are loaded by the special Ant class loader and not by a plug-in classloader. (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=34466">34466</a>).
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId912215" id="mozTocId912215">XDoclet support from within Eclipse</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId912215" id="mozTocId912215"> Since there are differences when running Ant from the commandline and within Eclipse, some extra steps may be needed to have XDoclet support function correctly within
      Eclipse. Problems may occur creating XDoclet subtasks. The workarounds and full discussion can be found in bug report. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=37070">37070</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId31051" id="mozTocId31051">Ant Editor code completion based on Ant 1.6.x</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId31051" id="mozTocId31051"> Code completion provided by the Ant editor does not respect the user-specified version of org.eclipse.ant.core plug-in or ANT_HOME. Code completion proposals are mostly
      based on Ant 1.6.x with some updates to Ant 1.8.3 (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=193046">bug 193046</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId925603" id="mozTocId925603">Setting build loggers not supported when debugging Ant builds</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId925603" id="mozTocId925603"> When debugging Ant builds within Eclipse, setting <code>-logger</code> as a program argument will be ignored.
    </a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId669417" id="mozTocId669417">Renaming an External Tool builder set to run during auto-build will cause errors</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId669417" id="mozTocId669417"> If you rename an existing external tool builder that is configured to run during auto-builds, you will get the following error: Errors during build. Errors running
      builder "Integrated External Tool Builder" on project &lt;PROJECT_NAME>. The builder launch configuration could not be found. The workaround is to first disable the builder for auto-builds
      and then rename the builder. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=118294">118294</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId772119" id="mozTocId772119">Slow typing/saving of the Ant editor with imports that define numerous macrodefs</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId772119" id="mozTocId772119"> The Ant editor is slow on saving with buildfiles that have &lt;import> declarations of buildfiles that have numerous &lt;macrodef>s. See bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=125117">125117</a> for a possible workaround
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId715004" id="mozTocId715004">Ant 1.8.x reports missing libraries as build failures</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId715004" id="mozTocId715004"> In Ant 1.8.x, if you try to use a task that requires additional libraries and you do not have the libraries on the Ant classpath, the build will now properly report as
      failed. In previous versions of Ant, the build would still report that it had succeeded even though it actually failed to run any of the tasks from additional bundles. See </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=344518">bug 344518</a>.
  </p>
  <p>
    For more information on tasks that require additional bundles please refer to the <a href="https://archive.apache.org/dist/ant/RELEASE-NOTES-apache-ant-1.8.2.html">Ant 1.8.2 release notes</a> and
    the <a href="http://ant.apache.org/manual/install.html#optionalTasks">Optional Tasks</a> section in the Ant manual.
  </p>
  <h3 id="I-Platform-User-Assistance">
    <a class="mozTocH3" name="mozTocId876322" id="mozTocId876322">Platform - User Assistance</a>
  </h3>
  <h4>
    <a class="mozTocH4" name="mozTocId828477" id="mozTocId828477">Welcome page not displayed properly (Linux/Unix)</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId828477" id="mozTocId828477"> The default Welcome implementation is HTML-based and requires a supported browser in order to work. If no supported browser can be found, Welcome falls back to its
      Forms-based implementation, which has a different (simpler) appearance. Consult the </a><a href="http://www.eclipse.org/swt/faq.php#browserplatforms">SWT FAQ</a> for supported browsers and setting
    up your browser to work with eclipse.
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId26110" id="mozTocId26110">Help browser tool bar buttons do not work for some documents</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId26110" id="mozTocId26110"> The Help browser's Print, Synchronize, and Bookmark buttons do not work for pages that are not actually installed with the product. However, you can always use the
      print command in the browser's context menu to print the page you're reading. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=44216">44216</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId324012" id="mozTocId324012">Help documents not displayed in a browser or very slow document loading (Windows only)</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId324012" id="mozTocId324012">If your LAN settings are not properly configured for local host access, your Help browser might open to a blank page or display an HTTP error instead of a help page, or
      you may experience long delays when loading help documents. Your system administrator can configure your LAN settings so that help documents can be accessed from the local help server.</a>
  </p>
  <blockquote><ol><li><a class="mozTocH4" name="mozTocId324012" id="mozTocId324012">In the Control Panel, open <b>Internet Options</b>, select the <b>Connections</b> tab and choose <b>LAN Settings</b>.
      </a></li><li><a class="mozTocH4" name="mozTocId324012" id="mozTocId324012">If your host was configured to use DHCP for IP assignment, make sure that the "Automatically detect settings" check box is cleared.</a></li><li><a class="mozTocH4" name="mozTocId324012" id="mozTocId324012">If you use a proxy server, ensure that the "Bypass proxy server for local addresses" is selected.</a></li><li><a class="mozTocH4" name="mozTocId324012" id="mozTocId324012">In "Advanced" settings for proxies, add "127.0.0.1;localhost" to the "Exceptions" if these addresses are not listed.</a></li><li><a class="mozTocH4" name="mozTocId324012" id="mozTocId324012">If you are using an automatic configuration script for proxy settings, and are not sure that the script is correct, clear the "Use automatic configuration script"
          check box.</a></li></ol></blockquote>
  <h4>
    <a class="mozTocH4" name="mozTocId227368" id="mozTocId227368">Working disconnected from the network (Windows only)</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId227368" id="mozTocId227368"> If you are experiencing problems when not connected to the network, you must install the loopback adapter from the Windows installation CD. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=831">831</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId121403" id="mozTocId121403">Using Internet Explorer in offline mode (Windows only)</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId121403" id="mozTocId121403">If you have been using Internet Explorer in Offline mode, when you access the help system you will get a message indicating that the web page you requested is not
      available offline or a blank page will display. Click <b>Connect</b> or deselect "Work Offline" in the Internet Explorer "File" menu to return the system behavior to normal.
    </a>
  </p>
  <h3 id="I-Platform-UI">
    <a class="mozTocH3" name="mozTocId683637" id="mozTocId683637">Platform - UI</a>
  </h3>
  <h4>
    <a class="mozTocH4" name="mozTocId348035" id="mozTocId348035">Dirty state not tracked properly for OLE documents (Windows only)</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId348035" id="mozTocId348035"> The dirty state for an OLE document is not updated properly. This causes Eclipse to prompt to save the contents of the editor when the document is closed, even if the
      contents have already been saved. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=2564">2564</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId878052" id="mozTocId878052">OLE document crashes can cause Eclipse to also crash (Windows only)</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId878052" id="mozTocId878052">If an OLE document crashes, Eclipse can crash, or the workbench menus can become inconsistent.</a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId452707" id="mozTocId452707">Toolbars only containing contributed controls exhibit display errors on Mac/Linux</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId452707" id="mozTocId452707"> Currently there is no way on the Max or Linux platforms to define the <b>height</b> for controls contributed to toolbars, nor will those platforms respect the size
      returned by the control's <code>computeSize</code> method. If you encounter this issue there is currently no truly viable workaround. (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=183003">183003</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId443682" id="mozTocId443682">Allocating enough memory and solving OutOfMemoryError</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId443682" id="mozTocId443682"> The native launcher checks the JVM but PDE launches simply use java and don't go through the native launchers. The workaround is to add the appropriate JVM arg to your
      launch config or to the <i>Preferences > Java > Installed JREs</i>. (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=339763">339763</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId862142" id="mozTocId862142">Capabilities and Activities don't affect the menus and toolbars</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId862142" id="mozTocId862142"> Capabilities used to hide GUI elements like menu entries work for commands and individual actionSet entries, but Capabilities have not been fully implemented. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=359778">359778</a>)
  </p>
  <h3 id="I-Platform-SWT">
    <a class="mozTocH3" name="mozTocId554478" id="mozTocId554478">Platform - SWT</a>
  </h3>
  <h4>
    <a class="mozTocH4" name="mozTocId565691" id="mozTocId565691">Support for macOS 11 (Big Sur)</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId565691" id="mozTocId565691">Eclipse/SWT 4.19 supports macOS 11 (Big Sur). Most of issues that were identified have been addressed in 4.19. The remaining open issues are tracked by a top level bug for the next release.
      (bugs </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=565691">565691</a> and <a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=569361">569361</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId534426" id="mozTocId534426">Usage of swt.autoScale and GDK_SCALE flag on GTK platforms</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId534426" id="mozTocId534426">With new implementation of hi-dpi support we are directly working with GTK3. So the users may see non-uniform scaling when you use swt.autoScale and GDK_SCALE flags. 
      Workaround is to set the scalefactor in display settings.</a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId554478" id="mozTocId554478">Non-uniform scaling of text vs. icons when using intermediate scaling factors on high-DPI displays</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId554478" id="mozTocId554478">Eclipse automatically scales images on high-DPI monitors based on the resolution of the monitor. However, this scaling works only with integer scaling factors like
      100%, 200% etc by default. So, at intermediate scaling factors like 150%, 175% etc., its likely that the icons and text are scaled differently as the text scaling is handled directly by the
      operating system.</a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId69222" id="mozTocId69222">Eclipse plug-in based on the SWT Browser throws exception</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId69222" id="mozTocId69222"> The SWT Browser widget uses a platform-specific web browser to render HTML. The org.eclipse.swt.SWTError exception ("No more handles") is thrown on platforms that don't
      meet the requirements for running the Browser widget. Supported platforms and prerequisites are listed on the SWT FAQ item </a><a href="http://www.eclipse.org/swt/faq.php#browserplatforms">
      "Which platforms support the SWT Browser?"</a>.
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId238090" id="mozTocId238090">Eclipse icon is duplicated in task-bar on Windows</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId238090" id="mozTocId238090"> Workaround is to pin the launched eclipse application and not the launcher, for more details, refer bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=314805">314805</a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId414883" id="mozTocId414883">BIDI Segments in Text controls</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId414883" id="mozTocId414883"> BIDI Segments in Text controls only work on Windows and GTK. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=388578">388578</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId518357" id="mozTocId518357">Block Selection functionality provided by StyledText is not BIDI aware</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId518357" id="mozTocId518357"> When the orientation of characters under the left and right edges of the block selection rectangle are not the same, the actual selection ranges (in memory) differ
      from the visual representation of the selection. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=277929">277929</a>)
  </p>
  <h3 id="I-Platform-Team-CVS">
    <a class="mozTocH3" name="mozTocId263012" id="mozTocId263012">Platform - Team - CVS</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId263012" id="mozTocId263012"> The following are known problems with the CVS repository provider only, and do not apply to other repository providers. Additional information on how to use CVS from
      Eclipse can be found in the </a><a href="https://wiki.eclipse.org/CVS_FAQ">Eclipse CVS FAQ</a>.
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId262771" id="mozTocId262771">CVS server compatibility</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId262771" id="mozTocId262771">The CVS plug-in parses messages returned from the CVS server. If the format of these messages is not as expected, some of the plug-in's functionality may be missing.
      The CVS plug-in is compatible with all stable 1.11.X builds of the CVS server, and should be compatible with future releases in that stream unless text message formats change (the last tested
      server was 1.11.22). As for the 1.12.X feature releases of CVS, the Eclipse CVS client has been tested with builds up to 1.12.13. However, future releases could easily break the Eclipse CVS
      client. Basic functionality, such as Checkout, Commit, and Update, should always work, but there may be problems with more advanced commands such as Synchronizing and Browsing the repository.</a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId532855" id="mozTocId532855">Connection cannot be found after initially missing</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId532855" id="mozTocId532855"> If a connection initially fails due to a network problem, the connection may continue to fail even when the network problem is fixed. In order to establish the
      connection you must exit and restart Eclipse. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=9295">9295</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId660590" id="mozTocId660590">Received broken pipe signal" error from server</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId660590" id="mozTocId660590"> Eclipse sometimes performs multiple commands within a single connection to the server. This may cause problems with CVS servers that are running server scripts in
      response to certain commands. (bugs </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=23575">23575</a> and <a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=23581">23581</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId971246" id="mozTocId971246">Terminated with fatal signal 10" error from server</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId971246" id="mozTocId971246"> There is a bug in the CVS server related to some compression levels. If you get this error, changing the compression level on the CVS preference page may help. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=15724">15724</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId689776" id="mozTocId689776">error using ext connection method</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId689776" id="mozTocId689776"> There are a few situations that can result in an "Unknown response" error messages when using the ext connection method. One situation involves using an external
      communications client (e.g. rsh or ssh) that adds CRs to the communications channel (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=21180">21180</a>). Another involves Eclipse not
    properly reading the stderr output of the external communications tool. (bug <a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=11633">11633</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId50418" id="mozTocId50418">A disabled CVS capability may not be auto-enabled in existing workspaces</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId50418" id="mozTocId50418"> New in 3.0 is the ability to disable capabilities and the CVS support in Eclipse can be disabled. However, for backwards compatibility the CVS capability is
      auto-enabled in existing workspaces that already contain CVS projects. The auto-enabling function may not run if the team support plugin is not loaded at startup. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=66977">66977</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId533799" id="mozTocId533799">Builder output files may appear as changed</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId533799" id="mozTocId533799">When folders containing build output are shared they may get improperly marked as dirty when build output is generated.</a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId253283" id="mozTocId253283">Enabling GNOME proxy support</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId253283" id="mozTocId253283"> GNOME applications can make use of proxy settings defined in this environment. If set, Eclipse will use it prior to proxy settings declared using env variables. This
      feature is disabled by default, to enable it launch Eclipse with <code>"-Dorg.eclipse.core.net.enableGnome"</code> switch. That is,
    </a>
  </p>
  <pre>
    <a class="mozTocH4" name="mozTocId253283" id="mozTocId253283">eclipse -Dorg.eclipse.core.net.enableGnome</a>
  </pre>
  <h3 id="I-Platform-Install-Update">
    <a class="mozTocH3" name="mozTocId805874" id="mozTocId805874">Platform - Install/Update</a>
  </h3>
  <h4>
    <a class="mozTocH4" name="mozTocId914600" id="mozTocId914600">Manually installing features and plug-ins on a FAT file system (Windows only)</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId914600" id="mozTocId914600">When features and plug-ins are manually installed on top of an Eclipse-based product install located on a FAT file system that has already been run at least once, the
      product must be explicitly restarted with -clean. That is,</a>
  </p>
  <pre>
    <a class="mozTocH4" name="mozTocId914600" id="mozTocId914600">eclipse.exe -clean</a>
  </pre>
  <h4>
    <a class="mozTocH4" name="mozTocId648565" id="mozTocId648565">Connecting to untrusted sites using https</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId648565" id="mozTocId648565">You cannot install or update software from a site using https whose certificate is not chained to a trusted root certificate in your local certificate store. This
      typically means the server is using a self-signed certificate, or a certificate authenticated by an unknown third party.</a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId104394" id="mozTocId104394">Extension location is lost if the install path changes</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId104394" id="mozTocId104394"> A previously configured extension location may be temporarily removed if the install is moved or mounted under a different path. This only happens when the link file
      that configures the extension location uses a relative path that points to a directory under the Eclipse install. On a second startup using the same install path, the extension location is added
      again (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=95403">95403</a>).
  </p>
  <h3 id="I-JDT">
    <a class="mozTocH3" name="mozTocId428861" id="mozTocId428861">Java development tools (JDT)</a>
  </h3>
  <h4>
    <a class="mozTocH4" name="mozTocId577868" id="mozTocId577868">Cut, copy, paste not working for linked resources in views showing Java elements</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId577868" id="mozTocId577868"> The cut, copy, and paste actions do not work for linked files and folders appearing in views that show Java elements, including the Package Explorer. The workaround is
      to use these actions from the Navigator view instead. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=34568">34568</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId554543" id="mozTocId554543">Java working sets not working correctly for elements from JRE system library container</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId554543" id="mozTocId554543"> Applying a working set consisting entirely of elements from the JRE System library container as a filter to the packages view might result in an empty Package
      Explorer. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=30442">30442</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId440090" id="mozTocId440090">Suspend on uncaught exception overrides exception breakpoint location filters</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId440090" id="mozTocId440090"> Exception breakpoints can be configured with location filters (inclusive and exclusive). When an unchecked exception is configured to <b>not</b> suspend execution in a
      specific class, execution will still suspend when the user preference to suspend on uncaught exceptions is on. (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=66770">66770</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId812347" id="mozTocId812347">Running Java programs with non-Latin-1 characters in package or class names</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId812347" id="mozTocId812347">You get a <code>java.lang.NoClassDefFoundError</code> when running Java programs with non-Latin characters in the package or class names. The workaround is to package
      the class files as a JAR file and run the program out of the JAR and not from the file system directly. (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=4181">4181</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId638407" id="mozTocId638407">Cannot run or debug class in a project with GB18030 characters in project name</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId638407" id="mozTocId638407"> Most class libraries do not properly support the creation of a system process (via <code>java.lang.Runtime.exec(...)</code> ) when the specified command line contains
      GB18030 characters. This limitation means the debugger cannot launch applications when the command line it generates contains GB18030 characters. (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=32206">32206</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId994970" id="mozTocId994970">Cannot detect installed JRE with GB18030 characters in path name</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId994970" id="mozTocId994970"> Automatic JRE detection fails when the JRE is stored in a directory containing GB18030 characters in its name. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=33844">33844</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId324283" id="mozTocId324283">Cannot generate Javadoc for packages with GB18030 characters in the name</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId324283" id="mozTocId324283"> Most class libraries do not properly support the creation of a system process (via <code>java.lang.Runtime.exec(...)</code> ) when the specified command line contains
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=32215">32215</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId524553" id="mozTocId524553">Unable to debug stack overflows</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId524553" id="mozTocId524553"> If a debug session suspends on a <code>java.lang.StackOverflowError</code> exception (due to an exception breakpoint), the debugger may not be able to retrieve any
      debug information from the target JVM. As well, the debugger may not be able to reliably interact with the target JVM past this point. (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=19217">19217</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId162517" id="mozTocId162517">Evaluation limitation</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId162517" id="mozTocId162517"> The debugger uses threads in the target JVM to perform evaluations (both explicit evaluations that the user requests, and implicit evaluations such as <code>toString()</code>
      invocations in the <b>Variables</b> view). The Java Debug Interface (JDI) requires that the thread in which an evaluation is performed be suspended by a user event (that is, a breakpoint or step
      request). Evaluations cannot be performed on threads suspended by the suspend action. As well, when a breakpoint is configured to suspend the JVM rather than just the individual thread, the
      threads which did not encounter the breakpoint are not in a valid state to perform an evaluation. When an evaluation is attempted in a thread that is not in a valid state to perform an
      evaluation, an error message will appear to the effect of "Thread must be suspended by step or breakpoint to perform method invocation". (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=34440">34440</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId408387" id="mozTocId408387">Missing debug attributes</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId408387" id="mozTocId408387">The debugger requires that class files be compiled with debug attributes if it is to be able to display line numbers and local variables. Quite often, class libraries
      (for example, " <code>rt.jar</code> ") are compiled without complete debug attributes, and thus local variables and method arguments for those classes are not visible in the debugger.
    </a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId330034" id="mozTocId330034">Using Hot Code Replace</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId330034" id="mozTocId330034">Hot code replace is supported on JDK 1.4.x VMs, and IBM J9 VMs. The debugger will attempt to replace all class files that change in the workspace as the user edits and
      builds source code. However, hot code replace is limited to changes that a particular virtual machine implementation supports. For example, changes within existing methods may be supported, but
      the addition or removal of members may not be.</a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId976120" id="mozTocId976120">Scrapbook</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId976120" id="mozTocId976120">Setting a breakpoint inside a scrapbook page is not supported.</a>
  </p>
  <p>
    <a class="mozTocH4" name="mozTocId976120" id="mozTocId976120"> When a snippet is run in the scrapbook which directly or indirectly calls <code>System.exit(int)</code> , the evaluation cannot be completed, and will result in a
      stack trace for a <code>com.sun.jdi.VMDisconnectedException</code> being displayed in the scrapbook editor.
    </a>
  </p>
  <p>
    <a class="mozTocH4" name="mozTocId976120" id="mozTocId976120"> Terminating a scrapbook page while it is performing an evaluation results in a <code>com.sun.jdi.VMDisconnectedException</code> being displayed in the scrapbook
      editor.
    </a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId666507" id="mozTocId666507">Debugging over slow connections</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId666507" id="mozTocId666507">A global Java debug preference specifies the debugger timeout, which is the maximum amount of time the debugger waits for a response from the target VM after making a
      request of that VM. Slow connections may require that this value be increased. The timeout value can be edited from the <b>Java > Debug </b>preference page. Changing the timeout value only
      affects subsequently launched VM, not VMs that are already running.
    </a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId207158" id="mozTocId207158">Updating of inspected values</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId207158" id="mozTocId207158">When inspecting the result of an evaluated expression in the debugger, it is important to note that the result displayed is the result of that expression at the time it
      was evaluated. For example, when inspecting a simple integer counter (primitive data type), the value displayed in the Expressions view is the value when the expression was evaluated. As the
      counter is changed in the running program, the inspected result will not change (since the view is not displaying the value bound to a variable - it is displaying the value of an expression, and
      the value of a primitive data type cannot change). However, if an expression results in an object, fields of that object will be updated in the inspector as they change in the running program
      (since the value bound to fields in an object can change).</a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId821393" id="mozTocId821393">Stepping over native methods that perform I/O</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId821393" id="mozTocId821393">When the debugger steps over native methods that perform I/O to <code>System.out</code> or <code>System.err</code>, the output may not appear immediately unless the
      native performs a flush on the output buffer.
    </a>
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId724969" id="mozTocId724969">VM and process termination running on IBM 1.3 JVM on Linux (Linux only)</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId724969" id="mozTocId724969">Terminating a launch, debug target, or system process associated with a debug target running on the IBM 1.3 JVM on the Linux platform does not work when the associated
      debug target has a suspended thread. To remove such debug targets from the debug UI, select <b>Terminate and Remove</b> from the debug view's pop-up menu (or use the shortcut "delete" key).
      Associated system processes in the OS may not be properly cleaned up. If a debug target has no suspended threads, termination works properly. (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=1631">1631</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId188069" id="mozTocId188069">Java indexing encounters problems when a folder is used both as a source and a class folder</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId188069" id="mozTocId188069"> Java indexing encounters problems when a folder is used both as a source folder in a project and as a class folder in another project. Hence, when this peculiar setup
      is used, the Java Search might miss matches located in such a folder. To avoid this kind of problem, it is strongly advised to use different folders for sources and binary classes. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=309903">309903</a>)
  </p>
  <h3 id="I-PDE">
    <a class="mozTocH3" name="mozTocId25456" id="mozTocId25456">Plug-in Development Environment (PDE)</a>
  </h3>
  <h4>
    <a class="mozTocH4" name="mozTocId179699" id="mozTocId179699">Feature manifest editor does not preserve all comments</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId179699" id="mozTocId179699"> When a non-source page of the feature manifest editor is used, PDE will convert changes back into XML by regenerating the file. Although the overall content and most
      of the comments are preserved, some comments may be lost. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=59502">59502</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId243421" id="mozTocId243421">PDE will not unzip source zips of some plug-ins</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId243421" id="mozTocId243421"> In the plug-in import wizard, when you choose to import plug-ins as "projects with source folders", PDE will not unzip the source for the org.apache.ant. This is
      because the source ZIPs contains code that will not compile when unzipped as it requires additional JARs that are not part of the SDK. To avoid the creation of plug-in projects that won't
      compile, PDE will import these plug-ins as binary and attach source, so you would still be able to read the source, you just won't be able to modify it. Also, PDE will not unzip the source for
      the org.eclipse.swt plug-ins. In this case, it is because, when shipped, the swt code is spread across a plug-in and a fragment, and when unzipped, it will require circular dependencies between
      the plug-in and fragment projects. These circular dependencies are at minimum marked as warnings by the JDT compiler and may result in unpredictable build behavior. Therefore, PDE always imports
      org.eclipse.swt as binary with source attached. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=66314">66314</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId722932" id="mozTocId722932">Emacs key bindings do not work in manifest editor fields</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId722932" id="mozTocId722932"> Non-default key bindings currently do not work in fields on non-source pages of the PDE manifest editors. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=19482">19482</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId828449" id="mozTocId828449">Export of plug-in may silently drop classes</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId828449" id="mozTocId828449"> When exporting a plug-in using the plug-in, feature or product wizards, some classes might be dropped from the resulting archive if their fully qualified name is too
      long. This typical path limitation can be worked around by creating the jar of the problematic plug-in by using the Jar export wizard. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=97150">97150</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId89714" id="mozTocId89714">Compilation errors when exporting projects not stored outside of the workspace</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId89714" id="mozTocId89714"> When exporting multiple plug-ins and one is stored outside of the workspace, compile errors occurs on export. To work around the problem, you can either export the
      plug-ins one by one, or change their location. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=98579">98579</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId270371" id="mozTocId270371">Headless build needs to be run from a fully qualified path</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId270371" id="mozTocId270371"> When running a headless build using the scripts provided by pde build, the properties <code>builder</code> and <code>buildDirectory</code> must refer to a fully
      qualified path. (bug
    </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=139554">139554</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId73293" id="mozTocId73293">Importing in Eclipse application fails if plug-in exists in host workspace</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId73293" id="mozTocId73293"> When running an Eclipse application (self-hosting) importing plug-ins will not work correctly if the plug-in being imported exists in the host Eclipse's workspace. This
      is because PDE modifies the target platform of the application to point at the running plug-ins from the host (target weaving). This also affects the PDE test suite. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=294005">294005</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId914239" id="mozTocId914239">Reusing a workspace after changing architectures silently breaks PDE models</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId914239" id="mozTocId914239"> If a workspace is reused on a machine with a different architecture, the PDE models used to build plug-ins may silently fail. To work around this problem, delete the
      metadata in &lt;workspace>/.metadata/.plugins/org.eclipse.pde.core. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=350172">350172</a>)
  </p>
  <h4>
    <a class="mozTocH4" name="mozTocId624312" id="mozTocId624312">Missing @since tag API Tools problems on interface fields containing @noreference tag</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId624312" id="mozTocId624312"> The Eclipse platform 4.6 release will not allow the API Tools @noreference tag on interface fields. This was changed because all interface fields are constant fields
      that cannot support the @noreference restriction. The tag was allowed in previous releases and this usage will now be considered an API change requiring a @since tag. It is recommended that you
      create an API Tools filter for the missing @since tag problem. This filter can be removed as soon as the API baseline has been regenerated. (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=402393">402393</a>)
  </p>
  
  <h2 id="RunningEclipse">
    <a class="mozTocH2" name="mozTocId19817" id="mozTocId19817">Running Eclipse</a>
  </h2>
  <p>
    <a class="mozTocH2" name="mozTocId19817" id="mozTocId19817"> After installing the Eclipse SDK in a directory, you can start the Workbench by running the Eclipse executable included with the release (you also need a Java SE 11 JRE,
      not included with the Eclipse SDK). With Oomph users can install required JRE courtesy of <a href="https://www.eclipse.org/justj/">JustJ</a>. On Windows, the executable file is called <samp>eclipse.exe</samp> , and is located in the <code>eclipse</code> sub-directory of the install. If installed at
      <code>c:\eclipse-SDK-4.19-win64</code> , the executable is <code>c:\eclipse-SDK-4.19-win64\eclipse\eclipse.exe</code> . <b>Note:</b> Set-up on most other operating environments is analogous.
      Special instructions for Mac OS X are listed
    </a><a href="#macosx">below</a>.
  </p>
  <h3>
    <a class="mozTocH3" name="mozTocId60052" id="mozTocId60052">Allocating enough memory and solving OutOfMemoryErrors</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId60052" id="mozTocId60052"> By default, Eclipse will allocate up to 1024 megabytes of Java heap memory. This should be ample for all typical development tasks. However, depending on the JRE that
      you are running, the number of additional plug-ins you are using, and the number of files you will be working with, you could conceivably have to increase this amount. Eclipse allows you to pass
      arguments directly to the Java VM using the <code>-vmargs</code> command line argument, which must follow all other Eclipse specific arguments. Thus, to increase the available heap memory, you
      would typically use:
    </a>
  </p>
  <blockquote>
    <p>
      <a class="mozTocH3" name="mozTocId60052" id="mozTocId60052"> <code>eclipse -vmargs -Xmx&lt;memory size></code>
      </a>
    </p>
  </blockquote>
  <p>
    <a class="mozTocH3" name="mozTocId60052" id="mozTocId60052"> with the <code>&lt;memory size></code> value set to greater than "1024M" (1024 megabytes -- the default).
    </a>
  </p>
  <p>
    <a class="mozTocH3" name="mozTocId60052" id="mozTocId60052">Note that setting memory sizes to be near or larger than the amount of available physical memory on your machine will cause Java to "thrash" as it copies objects back
      and forth to virtual memory, which will severely degrade your performance.</a>
  </p>
  <h3>
    <a class="mozTocH3" name="mozTocId735187" id="mozTocId735187">Selecting a workspace</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId735187" id="mozTocId735187"> When the Workbench is launched, the first thing you see is a dialog that allows you to select where the workspace will be located. The workspace is the directory where
      your work will be stored. If you do not specify otherwise, Eclipse creates the workspace in your user directory. This workspace directory is used as the default content area for your projects as
      well as for holding any required metadata. For shared or multi-workspace installs you must explicitly specify the location for your workspace using the dialog (or via the " <code>-data</code> "
      command line argument).
    </a>
  </p>
  <h3>
    <a class="mozTocH3" name="mozTocId620725" id="mozTocId620725">Specifying the Java virtual machine</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId620725" id="mozTocId620725">Here is a typical Eclipse command line:</a>
  </p>
  <blockquote>
    <p>
      <a class="mozTocH3" name="mozTocId620725" id="mozTocId620725"> <code>eclipse -vm c:\jdk11\bin\javaw</code>
      </a>
    </p>
  </blockquote>
  <p>
    <a class="mozTocH3" name="mozTocId620725" id="mozTocId620725"> <i>Tip:</i> It's generally a good idea to explicitly specify which Java VM to use when running Eclipse. This is achieved with the " <code>-vm</code> " command line
      argument as illustrated above. If you don't use " <code>-vm</code> ", Eclipse will look on the OS path. When you install other Java-based products, they may change your path and could result in
      a different Java VM being used when you next launch Eclipse.
    </a>
  </p>
  <p>
    <a class="mozTocH3" name="mozTocId620725" id="mozTocId620725">To create a Windows shortcut to an installed Eclipse:</a>
  </p><ol><li><a class="mozTocH3" name="mozTocId620725" id="mozTocId620725">Navigate to <code>eclipse.exe</code> in Windows Explorer and use Create Shortcut on the content menu.
    </a></li><li><a class="mozTocH3" name="mozTocId620725" id="mozTocId620725">Select the shortcut and edit its Properties. In the Target: field append the command line arguments.</a></li></ol><p>
    <a class="mozTocH3" name="mozTocId620725" id="mozTocId620725">Opening this shortcut launches Eclipse. (You can drag the shortcut to the Windows Desktop if you want to keep it in easy reach.)</a>
  </p>
  <h3 id="macosx">
    <a class="mozTocH3" name="mozTocId928700" id="mozTocId928700">Mac OS X</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId928700" id="mozTocId928700"> On Mac OS X, you start Eclipse by double clicking the Eclipse application. If you need to pass arguments to Eclipse, you'll have to edit the <code>eclipse.ini</code>
      file inside the Eclipse application bundle: select the Eclipse application bundle icon while holding down the Control Key. This will present you with a popup menu. Select "Show Package Contents"
      in the popup menu. Locate <code>eclipse.ini</code> file in the <code>Contents/Eclipse</code> sub-folder and open it with your favorite text editor to edit the command line options.
    </a>
  </p>
  <p>
    <a class="mozTocH3" name="mozTocId928700" id="mozTocId928700"> On MacOS X you can only launch a UI program more than once if you have separate copies of the program on disk. The reason for this behavior is that every UI
      application on Mac can open multiple documents, so typically there is no need to open a program twice. Since Eclipse cannot open more than one workspace, this means you have to make a copy of
      the Eclipse install if you want to open more then one workspace at the same time (bug </a><a href="https://bugs.eclipse.org/bugs/show_bug.cgi?id=139319">139319</a>).
  </p>
  <p>If you need to launch Eclipse from the command line, you can create a symbolic link such as "eclipse". It should point to the eclipse executable inside the application bundle and takes the
    same arguments as "eclipse.exe" on other platforms.</p>
  <p>On Mac OS X 10.4 and later, you may notice a slow down when working with significant numbers of resources if you allow Spotlight to index your workspace. To prevent this, start System
    Preferences, select the Spotlight icon, then the Privacy tab, then click the Add button ("+") and find your workspace directory in the dialog that appears.</p>
  <h3 id="SharedInstall">
    <a class="mozTocH3" name="mozTocId221199" id="mozTocId221199">Shared Install</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId221199" id="mozTocId221199"> The startup speed of a shared install can be improved if proper cache information is stored in the shared install area. To achieve this, after unzipping Eclipse
      distribution, run Eclipse once with the "-initialize" option from an account that has a write access to the install directory. See </a><a href="%20http://help.eclipse.org/luna/index.jsp?topic=%2Forg.eclipse.platform.doc.isv%2Freference%2Fmisc%2Fmulti_user_installs.html">shared installs</a> in Eclipse Help for more information.
  </p>
  <h2 id="Upgrading">
    <a class="mozTocH2" name="mozTocId575572" id="mozTocId575572">Upgrading Workspace from a Previous Release</a>
  </h2>
  <h3>
    <a class="mozTocH3" name="mozTocId401691" id="mozTocId401691">Users who don't use "-data"</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId401691" id="mozTocId401691">If you weren't previously using "-data" to specify your workspace, follow these steps to upgrade:</a>
  </p><ol><li><a class="mozTocH3" name="mozTocId401691" id="mozTocId401691">Find the workspace directory used by your old version of Eclipse. Typically this is located inside the directory in which Eclipse was installed in a sub-directory
        called "<code>workspace</code>". If you are using a shortcut or script to launch Eclipse, then it will be under the current working directory of that shortcut or script in a sub-directory
        called "workspace". For Windows users, this is specified by the "Start in:" argument in your shortcut properties.
    </a></li><li><a class="mozTocH3" name="mozTocId401691" id="mozTocId401691">Copy this workspace directory to a new, empty location outside of any Eclipse install directory.</a></li><li><a class="mozTocH3" name="mozTocId401691" id="mozTocId401691">Install the new version of Eclipse in a new location, separate from any old version of Eclipse.</a></li><li><a class="mozTocH3" name="mozTocId401691" id="mozTocId401691">If you had installed additional features and plug-ins into your old Eclipse, you should re-install them in the new Eclipse.</a></li><li><a class="mozTocH3" name="mozTocId401691" id="mozTocId401691">Start this new version of Eclipse and select this location using the workspace chooser dialog at startup (or use "<code>-data</code>" command line argument to
        pre-select the workspace location).
    </a></li></ol><h3>
    <a class="mozTocH3" name="mozTocId197750" id="mozTocId197750">Users who do use "-data"</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId197750" id="mozTocId197750"> If you were previously using the " <code>-data</code> " argument to start Eclipse, your upgrade path is much easier:
    </a>
  </p><ol><li><a class="mozTocH3" name="mozTocId197750" id="mozTocId197750">Optionally copy your workspace directory to a new, empty location outside of any Eclipse install directory as a backup.</a></li><li><a class="mozTocH3" name="mozTocId197750" id="mozTocId197750">Install the new version of Eclipse in a new location, separate from any old versions of Eclipse.</a></li><li><a class="mozTocH3" name="mozTocId197750" id="mozTocId197750">If you had installed additional features and plug-ins into your old Eclipse, you should re-install them in the new Eclipse.</a></li><li><a class="mozTocH3" name="mozTocId197750" id="mozTocId197750">Start this new version of Eclipse and select this location using the workspace chooser dialog at startup (or use "<code>-data</code>" command line argument to
        pre-select the workspace location).
    </a></li></ol><p>
    <a class="mozTocH3" name="mozTocId197750" id="mozTocId197750"> <i>Note:</i> Copying your workspace is recommended because, after you've upgraded your workspace, you won't be able to use it again with an older version of Eclipse.
      If you ever want to go "back in time" to an earlier release, you will need that backup.
    </a>
  </p>
  <h3>
    <a class="mozTocH3" name="mozTocId839433" id="mozTocId839433">Users who use User Libraries or classpath containers that contain JARs referencing other libraries via Class-Path in the MANIFEST.MF</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId839433" id="mozTocId839433">If you want the referenced JAR files to be included in the classpath, you can do one of the following:</a>
  </p><ul><li><a class="mozTocH3" name="mozTocId839433" id="mozTocId839433">Add the system property (<code>-DresolveReferencedLibrariesForContainers=true</code>) to the <code>-vmargs</code> list on start-up, or
    </a></li><li><a class="mozTocH3" name="mozTocId839433" id="mozTocId839433">Manually add the referenced JARs to the User Library or to the project.</a></li></ul><h3>
    <a class="mozTocH3" name="mozTocId623237" id="mozTocId623237">Dropped in bundles may not resolve after upgrade</a>
  </h3>
  <p>
    <a class="mozTocH3" name="mozTocId623237" id="mozTocId623237"> If you have installed bundles by dropping them into the <code>plugins</code> or <code>dropins</code> directory, they might no longer resolve when you upgrade to a new
      Eclipse Platform version. In each new version of the Eclipse Platform, there are new versions of bundles included in the platform, and often a small number of removed bundles. This may cause
      your previously dropped in bundles to no longer resolve and run. It is always recommended that you install software via the <code>Help > Install New Software</code> mechanism so you are made
      aware of any install-time failure to resolve dependencies.
    </a>
  </p>
  <h2 id="InteroperabilityWithPreviousReleases">
    <a class="mozTocH2" name="mozTocId638978" id="mozTocId638978">Interoperability with Previous Releases</a>
  </h2>
  <h3>
    <a class="mozTocH3" name="mozTocId759237" id="mozTocId759237">Interoperability of Release 4.19 with previous releases</a>
  </h3>
  <h4>
    <a class="mozTocH4" name="mozTocId226004" id="mozTocId226004">Sharing projects between heterogeneous Eclipse 4.19 and 4.18</a>
  </h4>
  <p>Special care is required when a project in a team repository is being loaded and operated on by developers using Eclipse-based products based on different feature or plug-in versions. The
    general problem is that the existence, contents, and interpretation of metadata files in the workspaces may be specific to a particular feature or plug-in version, and differ between versions. The
    workspace compatibility guarantees only cover cases where all developers upgrade their Eclipse workspaces in lock step. In those cases there should be no problem with shared metadata. However,
    when some developers are working in Eclipse 4.19 while others are working in Eclipse 3.x, there are no such guarantees. This section provides advice for what to do and not to do. It addresses the
    specific issues with the Eclipse SDK.</p>
  <p>The typical failure mode is noticed by the 4.19 user. 4.18 metadata is lost when a 4.19 user saves changes and then commits the updated metadata files to the repository. Here's how things
    typically go awry:</p><ul><li>A user working in Eclipse 4.19 creates or modifies a project in a way that results in changes to a shared metadata file that rely on 4.19-specific information. The user then commits the
      updated project files, including the shared metadata file, to the shared repository.</li><li><a class="mozTocH4" name="mozTocId226004" id="mozTocId226004">Another user working in Eclipse 4.18 or earlier shares this project from the same repository. The 4.19-specific information in the shared metadata file is not understood
        by Eclipse 4.18, and is generally discarded or ignored without warning. The user modifies the project in a way that results in changes to the shared metadata file, causing the shared metadata
        file to be rewritten without any of the 4.19-specific information. The user commits the updated project files, including the shared metadata file, to the shared repository. The user is
        generally unaware that shared information has just been lost as a result of their actions.</a></li><li><a class="mozTocH4" name="mozTocId226004" id="mozTocId226004">A user working in Eclipse 4.19 picks up the changes to a project from the shared repository, including the updated shared metadata file. The user may be unaware that
        they have just taken a retrograde step until later when things start to malfunction.</a></li></ul><p>
    <a class="mozTocH4" name="mozTocId226004" id="mozTocId226004">Here are some things to watch out for when sharing projects between Eclipse 4.19 and earlier releases:</a>
  </p><ul><li><a class="mozTocH4" name="mozTocId226004" id="mozTocId226004"><b>Virtual folders</b> - Eclipse 4.19 supports a notion of <i>virtual folders</i> that did not exist in Eclipse 3.5 or earlier. If such virtual folders are created in
        4.19, and the project is subsequently loaded into an Eclipse 3.5 or earlier workspace, these folders will not be recognized. Recommendation: avoid creating virtual folders where project
        compatibility with Eclipse 3.5 or earlier is required.</a></li><li><a class="mozTocH4" name="mozTocId226004" id="mozTocId226004"><b>Resource filters</b> - Eclipse 4.19 supports a notion of <i>resource filters</i> that did not exist in Eclipse 3.5 or earlier. If such filters are added to resources
        in 4.19, and the project is subsequently loaded into an Eclipse 3.5 or earlier workspace, these filters will not be recognized. Recommendation: avoid creating resource filters where project
        compatibility with Eclipse 3.5 or earlier is required.</a></li><li><a class="mozTocH4" name="mozTocId226004" id="mozTocId226004"><b>Predefined path variables</b> - Eclipse 4.19 supports a set of built in path variables that can be used as the basis for linked resource locations. Such variables
        will not be defined automatically in Eclipse 3.5 or earlier. If compatibility with 3.5 or earlier workspace is required, users on 3.5 or earlier workspaces will need to define such path
        variables manually.</a></li></ul><h4>
    <a class="mozTocH4" name="mozTocId574781" id="mozTocId574781">Using Eclipse 4.19 to develop plug-ins that work in Eclipse 4.18</a>
  </h4>
  <p>
    <a class="mozTocH4" name="mozTocId574781" id="mozTocId574781"> It is also possible (and reasonable) to use Eclipse 4.19 to develop a plug-in intended to work in Eclipse 4.18 or earlier. Use the <b>Plug-in Development > Target
        Platform </b>preference page to locate non-workspace plug-ins in an Eclipse 4.18 install. This ensures that the code for your plug-in is being compiled and tested against Eclipse 4.18 APIs,
      extension points, and plug-ins. (The above list of concerns do not apply since they affect the layout and interpretation of files in the plug-in <i>project</i> but none affect the actual
      deployed form of the plug-in.)
    </a>
  </p>
  <h2 id="appendix">
    <a class="mozTocH2" name="mozTocId317294" id="mozTocId317294">Appendix: Execution Environment by Bundle</a>
  </h2>
  <!--
     Remember, the URL to appendix link must be full URL, since some may be
     viewing this file, from a "file://" URL
-->
  <p>
    <a class="mozTocH2" name="mozTocId317294" id="mozTocId317294"> See the table in the </a><a href="https://www.eclipse.org/projects/project-plan.php?planurl=http://www.eclipse.org/eclipse/development/plans/eclipse_project_plan_4_19.xml#appendix">Eclipse 4.19 Project Plan Appendix</a> for
    the list of the minimum execution environment (Java class library) requirements of each bundle.
  </p>
  <hr/>
  <p>Sun, Solaris, Java and all Java-based trademarks are trademarks of Oracle Corporation. in the United States, other countries, or both.</p>
  <p>IBM is a trademark of International Business Machines Corporation in the United States, other countries, or both.</p>
  <p>Microsoft, Windows, Windows NT, Vista, and the Windows logo are trademarks of Microsoft Corporation in the United States, other countries, or both.</p>
  <p>Apple and Mac OS are trademarks of Apple Computer, Inc., registered in the U.S. and other countries.</p>
  <p>Other company, product, and service names may be trademarks or service marks of others.</p>
  <p>(c) Copyright Eclipse Contributors 2009, 2020</p>
</body>
