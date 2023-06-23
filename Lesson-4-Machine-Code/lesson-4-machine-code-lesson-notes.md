# Lesson 4 - Machine Code 

## Owners, group members, and everybody else

Machine code, also known as machine language, is the elemental language of computers. It is read by the computer's central processing unit (CPU), is composed of digital binary numbers and looks like a very long sequence of zeros and ones.

### Binary code is the only language that computer hardware can understand.

Each CPU has its own specific machine language. The processor reads and handles instructions, which tell the CPU to perform a simple task. Instructions are comprised of a certain number of bits. If instructions for a particular processor are 8 bits, for example, the first 4 bits part (the opcode) tells the computer what to do and the second 4 bits (the operand) tells the computer what data to use.

<img width="1098" alt="Снимок экрана 2023-06-23 в 11 59 09" src="https://github.com/Artyom7577/Lesson-4-Machine-Code/assets/108987460/d8ead7a5-4517-4929-a55e-a0ab7e261cbd">


The binary representations you provided are conversions from decimal numbers to their binary equivalents. Here's an explanation of each conversion:


 
                                                       Data type


In computer programming, data types refer to the classification or categorization of data that determines the type of values it can hold and the operations that can be performed on it. Data types define the nature of data and provide the compiler or interpreter with information on how to handle and manipulate that data.

* Integer data
* Symbol data
* Grphical data
* Audio data
* Floating-Point data



                                                       Integer data



The INTEGER data type stores whole numbers that range from -2,147,483,647 to 2,147,483,647 for 9 or 10 digits of precision.

The number 2,147,483,648 is a reserved value and cannot be used. The INTEGER value is stored as a signed binary integer and is typically used to store counts, quantities, and so on.

Arithmetic operations and sort comparisons are performed more efficiently on integer data than on float or decimal data. INTEGER columns, however, cannot store absolute values beyond (231-1). If a data value lies outside the numeric range of INTEGER, the database server does not store the value.

INTEGER data types require 4 bytes of storage per value.

Integer data represents whole numbers without decimal points. In the binary system, integers are represented using bits (binary digits) that can be either 0 or 1. Here are a few examples of integers represented in the binary system:

positive integers are represented directly in binary, while negative integers are typically represented using the two's complement representation. The two's complement representation allows for the representation of negative numbers by inverting the bits and adding 1 to the least significant bit.
It's important to note that the number of bits used to represent integers can vary based on the programming language or system architecture. The examples provided assume an 8-bit representation, but in practice, integers can be represented using different bit lengths, such as 16-bit, 32-bit, or 64-bit, depending on the specific requirements of the programming language or system.

The decimal number 48 is converted to its binary representation, which is 00110000. In binary, each digit can have two possible values: 0 or 1. The binary representation follows a positional system, where each digit represents a power of 2. Breaking down the conversion:


> '48' -> 00110000
> 
> '10' -> 00001010
> 
> '255' -> 11111111
>
> 
The rightmost digit represents 2^0 (which is 1) multiplied by 0, resulting in 0.
The second rightmost digit represents 2^1 (which is 2) multiplied by 0, resulting in 0.
All other digits to the left are also 0 because the decimal number 48 does not require higher powers of 2 for its binary representation

* take the decimal number 42 and represent it in binary using an 8-bit representation.

> Step 1: Convert 42 to binary:
>
> Divide 42 by 2 repeatedly until the quotient is 0, noting the remainders:
> 
* 42 ÷ 2 = 21  (remainder 0)
* 21 ÷ 2 = 10  (remainder 1)
* 10 ÷ 2 = 5   (remainder 0)
* 5 ÷ 2 = 2    (remainder 1)
* 2 ÷ 2 = 1    (remainder 0)
* 1 ÷ 2 = 0    (remainder 1)

> Reading the remainders from the bottom up, we have: 101010.

.  
> Step 2: Pad the binary number to 8 bits:
> Since the binary number 101010 has only 6 digits, we need to add leading zeros to make it an 8-bit representation
> Binary: 00101010



                                                    Symbol data


In the context of computer programming, symbol data refers to data types that represent symbols or identifiers. Symbols are often used to refer to variables, functions, constants, or other entities within a program. Symbol data types are typically used to store and manipulate these symbolic representations. Here is some information about symbol data types:

symbol data types include:

* Variables: 
> Variables are symbols used to represent memory locations that store values. They are typically declared with a specific data type and can hold
> different values during program execution.
> 
* Constants:
> Constants are symbols that represent fixed values that do not change during program execution. They are typically defined with a name and ?>assigned a specific value that remains constant.
> 
* Labels:
> Labels are symbols used in control flow statements or jumps within the program. They mark specific points in the code, allowing the program to >branch to or repeat sections based on conditional statements or loops.
> 

Symbol data types play a crucial role in program organization, readability, and maintainability by providing meaningful names and references to program entities. They enable efficient data management, control flow, and modular programming practices.



                                                    Floating-Point 



The floating-point representation can implement operations for high range values. The numerical evaluations are carried out using floating-point values. It can create calculations easy, scientific numbers are described as follows −

The number 5,600,000 can be described as 0.56 * 107.

Therefore, 0.56 is the mantissa and 7 is the value of the exponent.

Binary numbers can also be described in exponential form. The description of binary numbers in the exponential form is called floating-point representation. The floating-point representation breaks the number into two parts, the left-hand side is a signed, fixed-point number known as a mantissa and the right-hand side of the number is known as the exponent. The floating-point values are also authorized with a sign; 0 denoting the positive value and 1 denoting the negative value.

The structure of floating-point representation for a binary number typically follows the IEEE 754 standard, which is widely used in modern computing systems. The structure consists of three components: the sign bit, the exponent, and the fraction (mantissa). Here is the structure:

Example − Convert 111101.1000110 into floating-point value.

111101.1000110 = 1.111011000110 * 25Converted to floating-point value

→ Denotes negative sign value

In this example, the integer value is converted to a floating-point value by changing the radix point next to the signed integer and scaling up the number to the exponential form by multiplying the value with the base 2. The value remains unaltered and this phase is known as the normalized method.


                                                    Graphical data


Graphical data refers to information that is visually represented using graphical elements such as charts, graphs, diagrams, maps, and images. It involves the use of visual cues and patterns to convey complex data in a more intuitive and accessible manner. By presenting data visually, graphical representations help users understand and interpret information, identify patterns, trends, and relationships, and make informed decisions.

> RGB
> 
RGB stands for Red, Green, Blue, which are the primary colors used in additive color models. In digital graphics and displays, RGB is a color model where colors are created by combining varying intensities of red, green, and blue light. Each color channel (red, green, and blue) is represented by an 8-bit value ranging from 0 to 255, allowing for a total of 16.7 million possible colors. By adjusting the intensity of each color channel, different colors can be created, enabling a wide range of color possibilities in digital images, monitors, and other display devices.
In the RGB color model, each color channel (red, green, and blue) is typically represented by an 8-bit value ranging from 0 to 255. Here are some examples of RGB colors represented in bytes (8-bit values):

1.
* Pure Red:
* Red: 255
* Green: 0
* Blue: 0
* RGB Byte Representation: (255, 0, 0)

2.  
* White:
* Red: 255
* Green: 255
* Blue: 255
* RGB Byte Representation: (255, 255, 255)

> HST
> 
"HST" is a less commonly used acronym in the context of graphical data. Without further context, it's difficult to determine the specific meaning of "HST" in this case. However, in astronomy, "HST" commonly refers to the Hubble Space Telescope, which is a space-based observatory operated by NASA and the European Space Agency. The Hubble Space Telescope captures high-resolution images and spectroscopic data of celestial objects, contributing to our understanding of the universe.



                                                       Audio data



Audio data refers to the representation of sound in digital form. It encompasses the recording, storage, and playback of sound waves using numerical values. Digital audio data is widely used in various applications, including music, voice recordings, podcasts, telecommunications, multimedia, and more.

* some key aspects and concepts related to audio data:

> Sample Rate: The sample rate refers to the number of samples captured per second and is typically measured in Hertz (Hz). Common sample rates for audio data include 44.1 kHz (CD quality), 48 kHz, and 96 kHz, among others. Higher sample rates provide better fidelity and capture more details of the audio signal.
>
> File Formats: Audio data is typically stored in various file formats, such as WAV, MP3, AAC, FLAC, and OGG. Each format has its own characteristics, features, and compatibility with different devices and software.
> 

> '49' -> 00110001
> 

The decimal number 49 is converted to its binary representation, which is 00110001. Following the same principles as above:
The rightmost digit represents 2^0 (which is 1) multiplied by 1, resulting in 1.

The second rightmost digit represents 2^1 (which is 2) multiplied by 0, resulting in 0.
All other digits to the left are 0 because the decimal number 49 does not require higher powers of 2 for its binary representation.



##  ASCII (American Standard Code for Information Interchange)

The ASCII (American Standard Code for Information Interchange) table is a widely used character encoding standard that assigns numeric values to represent characters. It was developed to facilitate the exchange of information between different computer systems and devices. In the ASCII table, each character is assigned a unique 7-bit binary number, allowing computers to store, process, and communicate textual data. For example, the ASCII value for the uppercase letter 'A' is 65, 'a' is 97, and the digit '0' is 48. The ASCII table includes a wide range of characters, including letters, numbers, punctuation marks, and control characters, providing a consistent encoding scheme for text-based communication and data representation.

Unicode is a character encoding standard that aims to represent every character from every writing system in the world. It assigns a unique code point to each character, allowing consistent and interoperable handling of text across different platforms, languages, and devices. With support for over 143,000 characters, Unicode enables multilingual communication and facilitates the exchange of information globally. It provides a foundation for internationalization and localization efforts in software development, ensuring that diverse scripts and symbols can be accurately displayed and processed.

Symbols in data representation, such as Latin letters A, B, and C, are often used to represent different types of data or variables in various contexts. Here's an explanation of symbols in the context of data representation:

## Latin Letters: Latin letters, such as A, B, C, etc., are commonly used as placeholders or labels to represent variables or data elements in mathematical equations, programming languages, and data analysis.


In binary representation, Latin letters A, B, and C are represented using their respective binary codes. Here are the binary representations of these letters using the 8-bit ASCII encoding:

* Letter A: 01000001 
* Letter B: 01000010 
* Letter C: 01000011



                                                       Drivers

                                                         
> OS Drivers
> 
 
OS Drivers: Operating System (OS) drivers, also known as device drivers or hardware drivers, are software components that facilitate communication between the operating system and hardware devices. They act as intermediaries, allowing the OS to interact with and control various hardware components such as printers, scanners, sound cards, network adapters, and more. OS drivers provide a standardized interface for the operating system to access and utilize hardware resources effectively.

> Monitor Drivers
> 
 
Monitor Drivers: Monitor drivers, also called display drivers, are a specific type of OS driver that enables the operating system to communicate with and control computer monitors. These drivers provide the necessary instructions for the monitor to display images, adjust resolution, color settings, refresh rate, and other visual parameters. Monitor drivers ensure compatibility between the monitor and the operating system, allowing optimal performance and accurate representation of graphics and visual content.

Both OS drivers and monitor drivers play crucial roles in enabling hardware functionality and ensuring seamless communication between hardware devices and the operating system. They are essential for proper system operation, performance, and compatibility. Operating systems often come with built-in drivers for common hardware, but manufacturers may provide specific drivers to unlock additional features or improve performance.


                                                       Files

File extensions are suffixes attached to the end of a file name, typically separated by a period. They indicate the file's format or type, providing a way for operating systems and applications to recognize and handle files appropriately. Common file extensions in programming include .cpp for C++ source code files, .java for Java source code files, .py for Python source code files, .html for HTML files, and .css for CSS style sheet files. These extensions help identify the programming language or technology associated with the file, allowing developers and tools to interpret and process the code or content correctly. By recognizing file extensions, software can apply language-specific syntax highlighting, perform code analysis, or execute the code within the appropriate runtime environment.

* .cpp: The .cpp file extension is used for C++ source code files. C++ is a general-purpose programming language known for its object-oriented features and high-performance capabilities.
* .java: The .java file extension is used for Java source code files. Java is a widely-used programming language known for its platform independence and extensive libraries.
* .py: The .py file extension is used for Python source code files. Python is a versatile and beginner-friendly programming language known for its readability and simplicity.
* .js: The .js file extension is used for JavaScript source code files. JavaScript is a programming language primarily used for adding interactivity and dynamic behavior to web pages.
* .swift: The .swift file extension is used for Swift source code files. Swift is a programming language developed by Apple, designed for building applications for iOS, macOS, watchOS, and tvOS.
* .sql: The .sql file extension is used for SQL (Structured Query Language) files. SQL is a language used for managing and manipulating databases.

  


   

