First this requires some recent history. Some two weeks ago I recieved the Raspberry foundation RP2040 Pico MCU. While the initial demos and simplistic Thonny IDE were adequate a challenge presented by a friend found me and this simple system wanting. After flailing around for these previous weeks I commited (I know irony, right?) to this approach.

The aim is to build a personally effective Python (uPY and cPY varients) development system. While suggestions were made -- I am a visual user not a CLI geek. This seeming contradiction is mittigated by my experience in publishing and writing. Most applications I use are GUI and WISIWIG based offering me a visual reference to manipulate and place the text and images I create. This is the distinction between and GUI and CLI, all or most control elements are 'click' or text respectively. 

You may imagine that in the early computing days I was both, around and a reluctant though interested user. I even bought a Swiss mouse and "Wogs" (Widowed opperating graphical system) for the Amstrad CPC464 in the mid 1980s, it needed too much RAM to be useful but it turned my head away from the CLI world into a GUI user and my next computer. The Amiga 500 and its amazing Workbench fitted my predilictions and biases spawning the first real debate between CLI and GUI users. BTW, these are Amiga terms I still use today. 

Enough moaning, back to work. These suggestions were from a CLI developer geek so somewhat challenging for me. This pricipitated my confusion and misdirected effort along with other factors. But the realisation of this personal truth has reenvigorated this quest for MCU development skills. By concentrating on a visual development workflow I can harness my bias and be less unproductive. Part of the confusion was the implication and historical notion of C as a root language. The Pi Pico arrived with two SDK guides, C/C++ and Micropython. While the main, C SDK, was easier to install it complicated a fraught decision matrix for the inexperienced but knowledgable user. 

Further there are two 'Python for MCU' variants available, uPython and cPython (Micro and Circuit Pythons respectively.) cPython can be confused with CPython used on PC's and SBC's. The differences between are distinct and both are incompatible with the other although they both work within CPython. First uPython is a serious community effort to replicate the power and capabilities of CPython on MCU's. Whereas Circuit or cPython was developed to simplify sensor and display deployments for the average unskilled consumer. Again, both are implementing ports for the RP2040 MCU, uPython with formal support fron the Raspberry Pi foundation while Adafruit is both, building RP2040 boards and porting cPython with informal support from the foundation. 

Onto what my activities yesterday and today have wrought before now. Decisions, concentrate on Python and its variants, learn a more sophisticated IDE (VSC, Visual Studio Code) and create an ordered file structure that spans the veriaty of platforms I use. Some research and notions of effective development indicated version control is important leading to the use of Git and Github. Also, I determined that I need to establish a complete development environment including uPython and cPython source trees. This required learning how to use Git, a CLI application so I sought a GUI option. This led to the Github Desktop application that this document is being used to experiment with. 

[02/04/2021 10:31am]

Using an ancient celeron x86 platform with Win10 (2004). Installed the latest Visual Studio Code, VSC extentions Python, RT-Thread Micropython, Language Tool, Circuitpython and Pylance. 

Installed Github desktop and began learning its operation. Tried to clone the Micropython src, failed. Need to fork and clone using my Github account.

Began and continued writing this document and others.

Need to add a TODO list. [11:17am] "To Do Tasks" extension to create and manage .todo and .tasks project files.

[>03:50pm] Transfered over to a Linux VSC and configured Git and using a browser forked Micropython and then cloned it onto the Linux platform. Found that CircuitPython as a fork of Micropython cannot be forked itself. It may be possible but I do not understand enough. Triped over a permissions issue. Learning enough to solve these issues. 

[04/04/2021 1:25am]

Begun early Easter Sunday by investigating GUI possibilities. Got fixated upon QT, particularly QT on Python for a RPI4 dev platform. Reminding myself about the objective I considered the simplicity required despite the repetative nature of GUI definitions. While there is little informantion about using TKinter with MicroPython or CircuitPython both seen to have community developments aimed at providing display modules. nano_GUI is one whilst Adafruit have built displayio as a base module. 

After following those shinny new ideas (not so shinny or new) the complexity of choice (QT4, QT5 or the current QT6) along with installation on the PI reduced my immediate interest. So I spent a portion of yesterday begining a specs document for my principle project idea. Here is a quote from that doc that gives a sense of this project.

""" 
    Before getting too deep into the weeds of my speculative design mind I should state that this vehicle is designed as a safe, effective, low-impact cargo and people transport using human hybrid power. Configured to transport up to three adult passengers with rider or between 300kg and 400kg of well distributed cargo or a combination. Limited to around 30kph with a powered range of less than 100km. Intended for local, short ranged transport by domestic and commercial users.
"""

This part of the project is to design, develop and build a 'proof of concept' deployment for a control system. Building a development environment, selecting hardware, firmware and the toolchains to build them depend upon the specs and skills I write and have. But decisions and commitment are issues I currently suffer a lack of. Anyway, using a pair of PI's connected wirelessly to host local MCU function modules simplifies the inherent mechanical issues while separating functional elements into thier own modules simplifies deployment, I hope. 

At present, the firm design intents are, a primary RPI connected to a 5" to 10" touch display as rider instrumentation and secondary control. Also this PI is the edge server between the contained system and the rest of the world. While maintaining and opperational wireless connection to the second PI hosting the rear function modules. 

Each PI is directly wired into thier respective local MCU modules, the primary to the forward box cargo section and wheels with the secondary to the energy, power and drive sections. Not mentioned is an attempt at lowering costs, prototyping is typically more expensive than a deployment but with limited resources somewhat fraught. 

In my mind the most developed idea is an attempt to build a lightweight version of ABS braking. In addition a version of a dual hydraulic safety system. These ideas will be detailed in, when available, the aforementioned specs documents. 

So, back on point. this project element using this venue is to develop the firmware and software needed to implement an intelligent light electric vehicle (LEV) control system tailored for hybrid (Human/electric) powered vehicles. Using traditional and emerging bicycle technologies, particularly digital monitoring and control, newer MCU and SBC devices to implement these ideas. 

In practical terms these elements are, UI/control, energy collection/management/delivery, environmental monitoring/optimisation and retardation/drive. While interconnected these are the principle elements needed. Other necessary aspects will emerge but these are enough to contend with. [6:10am]

