![logo](https://avatars1.githubusercontent.com/u/124156?v=3&s=100)
==========================
* [Learn Markdown](https://bitbucket.org/tutorials/markdowndemo)

## Synopsis
* This is a Gradle multiproject composed by 2 projects. 
* The one is **AppinstallerDrivers**; a war exposing a Javawebstart (jnlp) depending on a series of jars and embedded native libraries.
	* A gradle task imports an Ant build.xml to build the war.
* The other is **DriversNativoC**, the same project as [installerdriverscgradle](https://github.com/elbillyto/installerdriverscGradle.git), which adopts a gradle Layout

## DLL API Reference (DriversNativoC)
```c
JNIEXPORT jstring JNICALL Java_proyectoJava_Programa_getString (JNIEnv *, jobject);
JNIEXPORT int JNICALL Java_proyectoJava_Programa_addAtoB (JNIEnv *, jobject, jint, jint);
```  

## Code Example (DriversNativoC)
The signature of the library function must follow the rule:
Java_packageName_ClassName_libraryfuncionName
```c
Java_proyectoJava_Programa_getString
```
where: 
**libraryfunctionName** is the actual name of the function, 
**ClassName** is the name of the java class from where this native function is called, and
**packageName** is the name of the package where the class resides.```  
  
## Motivation
**POC** to address **native invocation through jni/java** from a java Webstart Aplication 
* Build a WAR project with jar and native libs dependencies
* Build a gradle multiproject 
	* War Application (imports Ant task)
	* native library (dll/so)
* Play aroung with gradle/groovy

## Installation
* Needs Gradle
* Clone repository
* run gradle construyeWar


## Tests


## Contributors
elbillyto

## License

This document and the project files are not copyrighted and are released into the public domain.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
