import jpype
import jpype.imports
from jpype.types import *

# Start the JVM with the JAR file
jpype.startJVM(classpath=["C:\\Users\\amitb\\Desktop\\Software\\undefinedvar\\app.jar"])

# Import your Java package and class
from com.groovy import App  # Replace with your package and class

# Create an instance of the Java class
java_instance = App()

# Call a method from the Java class
result = java_instance.analyzeGroovyScript("""String A,F
B=0
def C,D
B=10
C=20
String[] abc = ["Hello Amit","A"]""")
print(result)

# Shutdown the JVM
jpype.shutdownJVM()
