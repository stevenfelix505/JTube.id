# forked from <a href="https://github.com/shinovon">@Shinovon</a> repository to add Indonesian language

# JTube.id
Klien YouTube berdasarkan kode API Invidious untuk perangkat Java dengan dukungan MIDP 2.0

<a href="FAQ.md">FAQ</a><br>

JTube Lite:<br>
https://github.com/shinovon/JTubeLite <i>(Tidak lagi didukung)</i>

## Running JTube from other MIDlets
<a href="https://github.com/shinovon/MIDletIntegrationLibrary">MIDletIntegration library</a><br>

Example code:<br>
```
try {
	if(MIDletIntegration.startApp(this, "JTube", "nnproject", "0xAFCE0816", 1260, "url=" + Util.encodeURL("https://youtube.com/watch?v=somevideo"))) {
		notifyDestroyed();
	}
} catch (MIDletNotFoundException e) {
	e.printStackTrace();
} catch (ProtocolNotSupportedException e) {
	e.printStackTrace();
} catch (IOException e) {
	e.printStackTrace();
}
```

## Building

```
You will need:
Any J2ME SDK (e. g WTK, S40 5th, etc)
Symbian^3 JAR libraries
JDK 1.5.0
Last version of Eclipse SDK
MTJ plugin 2.0.1
```

Clone the repository<br>

Import project from directory in Eclipse SDK<br>

Open "Application Descriptor" in Package Explorer
![image](https://user-images.githubusercontent.com/43963888/154848600-b6f30e9c-a412-4771-80bf-527afe11076e.png)<br>

Click on "Create package"
![image](https://user-images.githubusercontent.com/43963888/154848614-72752480-b988-40cd-a3c6-9cad1e02d77c.png)<br>

Check the "Use deployment directory"<br>

To use "Obfuscate the code" option you must set up proguard in preferences first<br>

Then press "Finish"<br>

![image](https://user-images.githubusercontent.com/43963888/154848648-2f054800-b72e-49e6-8b6c-7e3cb6d3c216.png)<br>

Builded JAR & JAD files will appear at \<project path\>/deployed/S40_5th_Edition_SDK/
