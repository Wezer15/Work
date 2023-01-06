![](media/image55.png){width="8.499998906386702in"
height="10.999998906386702in"}

Table of Contents

> *[Title Page]{.underline}*
>
> *[Copyright Page]{.underline}*
>
> *[Dedication]{.underline}*
>
> *[Preface]{.underline}*
>
> *[Introduction]{.underline}*
>
> [Chapter 1 - Boolean Logic]{.underline}
>
> [1.1 Background]{.underline}
>
> [1.2 Specification]{.underline}
>
> [1.3 Implementation]{.underline}
>
> [1.4 Perspective]{.underline}
>
> [1.5 Project]{.underline}
>
> [Chapter 2 - Boolean Arithmetic]{.underline}
>
> [2.1 Background]{.underline}
>
> [2.2 Specification]{.underline}
>
> [2.3 Implementation]{.underline}
>
> [2.4 Perspective]{.underline}
>
> [2.5 Project]{.underline}
>
> [Chapter 3 - Sequential Logic]{.underline}
>
> [3.1 Background]{.underline}
>
> [3.2 Specification]{.underline}
>
> [3.3 Implementation]{.underline}
>
> [3.4 Perspective]{.underline}
>
> [3.5 Project]{.underline}
>
> [Chapter 4 - Machine Language]{.underline}
>
> [4.1 Background]{.underline}
>
> [4.2 Hack Machine Language Specification]{.underline}
>
> [4.3 Perspective]{.underline}
>
> [4.4 Project]{.underline}
>
> [Chapter 5 - Computer Architecture]{.underline}
>
> [5.1 Background]{.underline}
>
> [5.2 The Hack Hardware PlatformSpecification]{.underline}
>
> [5.3 Implementation]{.underline}
>
> [5.4 Perspective]{.underline}
>
> [5.5 Project]{.underline}
>
> [Chapter 6 - Assembler]{.underline}
>
> [6.1 Background]{.underline}
>
> [6.2 Hack Assembly-to-Binary Translation Specification]{.underline}
> [6.3 Implementation]{.underline}
>
> [6.4 Perspective]{.underline}
>
> [6.5 Project]{.underline}
>
> [Chapter 7 - Virtual Machine I: Stack Arithmetic]{.underline}
>
> [7.1 Background]{.underline}
>
> [7.2 VM Specification, Part I]{.underline}
>
> [7.3 Implementation]{.underline}
>
> [7.4 Perspective]{.underline}
>
> [7.5 Project]{.underline}
>
> [Chapter 8 - Virtual Machine II: ProgramControl]{.underline}
>
> [8.1 Background]{.underline}
>
> [8.2 VM Specification, Part II]{.underline}
>
> [8.3 Implementation]{.underline}
>
> [8.4 Perspective]{.underline}
>
> [8.5 Project]{.underline}
>
> [Chapter 9 - High-Level Language]{.underline}
>
> [9.1 Background]{.underline}
>
> [9.2 The Jack Language Specification]{.underline}
>
> [9.3 Writing Jack Applications]{.underline}
>
> [9.4 Perspective]{.underline}
>
> [9.5 Project]{.underline}
>
> [Chapter 10 - Compiler I: Syntax Analysis]{.underline}
>
> [10.1 Background]{.underline}
>
> [10.2 Specification]{.underline}
>
> [10.3 Implementation]{.underline}
>
> [10.4 Perspective]{.underline}
>
> [10.5 Project]{.underline}
>
> [Chapter 11 - Compiler II: Code Generation]{.underline}
>
> [11.1 Background]{.underline}
>
> [11.2 Specification]{.underline}
>
> [11.3 Implementation]{.underline}
>
> [11.4 Perspective]{.underline}
>
> [11.5 Project]{.underline}
>
> [Chapter 12 - Operating System]{.underline}
>
> [12.1 Background]{.underline}
>
> [12.2 The Jack OS Specification]{.underline}
>
> [12.3 Implementation]{.underline}
>
> [12.4 Perspective]{.underline}
>
> [12.5 Project]{.underline}
>
> [Chapter 13 - Postscript: More Fun to Go]{.underline}
>
> [13.1 Hardware Realizations]{.underline}
>
> [13.2 Hardware Improvements]{.underline}
>
> [13.3 High-Level Languages]{.underline}
>
> [13.4 Optimizations]{.underline}
>
> [13.5 Communications]{.underline}
>
> [Appendix A: - Hardware Description Language (HDL)]{.underline}
> [Appendix B: - Test Scripting Language]{.underline}
>
> *[Index]{.underline}*

![](media/image57.png){width="5.66in" height="6.56in"}

© 2005 Massachusetts Institute of Technology

> All rights reserved. No part of this book may be reproduced in any
> form by any electronic or mechanicalmeans (including photocopying,
> recording, or information storage and retrieval) without permission in
> writing from the publisher.

This book was set in Times New Roman on 3B2 by Asco Typesetters, Hong
Kong.

Printed and bound in the United States of America.

Library of Congress Cataloging-in-Publication Data

Nisan, Noam.

> The elements of computing systems: building a modern computer from
> first principles / Noam Nisan and Shimon Schocken. p. cm.

Includes bibliographical references and index.

ISBN 0-262-14087-X (alk. paper)

1\. Electronic digitalcomputers. I. Schocken, Shimon. II. Title.

TK7888.3.N57 2005

004.16---dc22

2005042807

10 9 8 7 6 5 4 3 2 1

Note on Software

> The book's Web site ([http://www.idc.ac.il/tecs)]{.underline} provides
> the tools and materials necessary to build all the hardware and
> software systems described in the book. These include a hardware
> simulator,a CPU emulator,a VM emulator,and executable versions of the
> assembler, virtual machine,compiler,and operating system described in
> the book. The Web site also includes all the project materials---about
> 200 test programs
>
> and test scripts,allowing incremental development and unit-testing of
> each one of the 12 projects. All the supplied software tools and
> project materials can be used as is on any computer equipped with
> either Windows or Linux.
>
> *To our parents,*
>
> *For teaching us that less is more.*

Preface

> *What I hear, I forget; What I see, I remember; What I do, I
> understand.*

*---Confucius, 551-479 BC*

> Once upon a time, every computer specialist had a gestalt
> understanding of how computers worked. The overall interactions among
> hardware, software, compilers, and the operating system were simple
> and transparent enough to produce a coherent picture of the computer's
> operations. As modern computer technologies have become increasingly
> more complex, this clarity is all but lost: the most fundamental ideas
> and techniques in computer science---the very essence of the
> field---are now hidden under many layers of obscure interfaces and
> proprietary implementations. An inevitable consequence of this
> complexity has been specialization, leading to computer science
> curricula of many courses, each covering a single aspect of the field.
>
> We wrote this book because we felt that many computer science students
> are missing the forest for the trees. The typical student is marshaled
> through a series of courses in programming, theory, and engineering,
> without pausing to appreciate the beauty of the picture at large. And
> the picture at large is such that hardware and software systems are
> tightly interrelated through a hidden web of abstractions, interfaces,
> and contract-based implementations. Failure to see this intricate
> enterprise in the flesh leaves many students and professionals with an
> uneasy feeling that, well, they don't fully understand what's going on
> inside computers.
>
> We believe that the best way to understand how computers work is to
> build one from scratch. With that in mind, we came up with the
> following concept. Let's specify a simple but sufficiently powerful
> computer system, and have the students build its hardware platform and
> software hierarchy from the ground up, starting with nothing more than
> elementary logic gates. And while we are at it, let's do it right. We
> say this because building a general-purpose computer from first
> principles is a huge undertaking. Therefore, we identified a unique
> educational opportunity not only to build the thing, but also to
> illustrate, in a hands-on fashion, how to effectively plan and manage
> large-scale hardware and software development projects. In addition,
> we sought to demonstrate the ability to construct, through recursive
> ascent and human reasoning, fantastically complex and useful systems
> from nothing more than a few primitive building blocks.

Scope

> The book exposes students to a significant body of computer science
> knowledge, gained through a series of hardware and software
> construction tasks. These tasks demonstrate how theoretical and
> applied techniques taught in other computer science courses are used
> in practice. In particular, the following topics are illustrated in a
> hands-on fashion:
>
> ■ *Hardware:* Logic gates, Boolean arithmetic, multiplexors,
> flip-flops, registers, RAM units, counters, Hardware Description
> Language (HDL), chip simulation and testing.
>
> ■ *Architecture:* ALU/CPU design and implementation, machine code,
> assembly language programming, addressing modes, memory-mapped
> input/output (I/O).
>
> ■ *Operating systems:* Memory management, math library, basic I/O
> drivers, screen management, file I/O, high-level language support.
>
> ■ *Programming languages:* Object-based design and programming,
> abstract data types, scoping rules, syntax and semantics, references.
>
> ■ *Compilers:* Lexical analysis, top-down parsing, symbol tables,
> virtual stack-based machine, code generation, implementation of arrays
> and objects.
>
> ■ *Data structures and algorithms:* Stacks, hash tables, lists,
> recursion, arithmetic algorithms, geometric algorithms, running time
> considerations.
>
> ■ *Software engineering:* Modular design, the interface/implementation
> paradigm, API design and documentation, proactive test planning,
> programming at the large, quality assurance.
>
> All these topics are presented with a very clear purpose: building a
> modern computer from the ground up. In fact, this has been our topic
> selection rule: The book focuses on the minimal set of topics
> necessary for building a fully functioning computer system. As it
> turns out, this set includes many fundamental ideas in applied
> computer science.

Courses

> The book is intended for students of computer science and other
> engineering disciplines in colleges and universities, at both the
> undergraduate and graduate levels. A course based on this book is
> "perpendicular" to the normal computer science curriculum and can be
> taken at almost any point during the program. Two natural slots are
> "CS-2"---immediately after learning programming, and "CS-199"---a
> capstone course coming at the end of the program. The former course
> can provide a systems-oriented introduction to computer science, and
> the latter an integrative, project-oriented systems building course.
> Possible names for such courses may be Constructive Introduction to
> Computer Science, Elements of Computing Systems, Digital Systems
> Construction, Computer Construction Workshop, Let's Build a Computer,
> and the like. The book can support both one- and two-semester courses,
> depending on topic selection and pace of work.
>
> The book is completely self-contained, requiring only programming (in
> any language) as a prerequisite. Thus, it lends itself not only to
> computer science majors, but also to computer-savvy students seeking
> to gain a hands-on view of hardware architectures, operating systems,
> and modern software engineering in the framework of one course. The
> book and the accompanying Web site can also be used as a self-study
> learning unit, suitable to students from any technical or scientific
> discipline following a programming course.

Structure

> The introduction chapter presents our approach and previews the main
> hardware and software abstractions discussed in the book. This sets
> the stage for chapters 1-12, each dedicated to a key hardware or
> software abstraction, a proposed implementation, and an actual project
> that builds and tests it. The first five chapters focus on
> constructing the hardware platform of a simple modern computer. The
> remaining seven chapters describe the design and implementation of a
> typical multi-tier software hierarchy, culminating in the construction
> of an object-based programming language and a simple operating system.
> The complete game plan is depicted in figure P.1.
>
> The book is based on an abstraction-implementation paradigm. Each
> chapter starts with a Background section, describing relevant concepts
> and a generic hardware or software system. The next section is always
> Specification, which provides a clear statement of the system's
> abstraction---namely, the various services that it is expected to
> deliver. Having presented the what, each chapter proceeds to discuss
> how the abstraction can be implemented, leading to a (proposed)
> Implementation section. The next section is always Perspective, in
> which we highlight noteworthy issues left out from the chapter. Each
> chapter ends with a Project section that provides step-by-step
> building instructions, testing materials, and software tools for
> actually building and unit-testing the systemdescribed in the chapter.

![](media/image60.png){width="4.929998906386702in" height="2.77in"}

> Figure P.1 Book and proposed course map, with chapter numbers in
> circles.

Projects

> The computer system described in the book is *for real*---it can
> actually be built, and it works! A reader who takes the time and
> effort to gradually build this computer will gain a level of intimate
> understanding unmatched by mere reading. Hence, the book is geared
> toward active readers who are willing to roll up their sleeves and
> build a computer fromthe ground up.
>
> Each chapter includes a complete description of a stand-alone hardware
> or software development project. The four projects that construct the
> computer platform are built using a simple Hardware Description
> Language (HDL) and simulated on a hardware simulator supplied with the
> book. Five of the subsequent software projects (assembler, virtual
> machine I and II, and compiler I and II) can be written in any modern
> programming language. The remaining three projects (low-level
> programming, high-level programming, and the operating system) are
> written in the assembly language and high-level language implemented
> in previous projects.
>
> Project Tips There are twelve projects altogether. On average, each
> project entails a weekly homework load in a typical, rigorous
> university-level course. The projects are completely self-contained
> and can be done (or skipped) in any desired order. Of course the "full
> experience" package requires doing all the projects in their order of
> appearance, but this is just one option.
>
> When we teach courses based on this book, we normally make two
> significant concessions. First, except for obvious cases, we pay no
> attention to optimization, leaving this very important subject to
> other, more specific courses. Second, when developing the translators
> suite (assembler, VM implementation, and compiler), we supply
> error-free test files (source programs), allowing the students to
> assume that the inputs of these translators are error-free. This
> eliminates the need to write code for handling errors and exceptions,
> making the software projects significantly more manageable. Dealing
> with incorrect input is of course critically important, but once again
> we assume that students can hone this skill elsewhere, for example, in
> dedicated programming and software design courses.

Software

> The book's Web site ([www.idc.ac.il/tecs)]{.underline} provides the
> tools and materials necessary to build all the hardware and software
> systems described in the book. These include a hardware simulator, a
> CPU emulator, a VM emulator, and executable versions of the assembler,
> virtual machine, compiler, and operating system described in the book.
> The Web site also includes all the project materials---about two
> hundred test programs and test scripts, allowing incremental
> development and unit-testing of each one of the twelve projects. All
> the supplied software tools and project materials can be used as is on
> any computer equipped with either Windows or Linux.

Acknowledgments

> All the software that accompanies the book was developed by our
> students at the Efi Arazi School of Computer Science of the
> Interdisciplinary Center Herzliya, a new Israeli university. The chief
> software architect was Yaron Ukrainitz, and the developers included
> Iftach Amit, Nir Rozen, Assaf Gad, and Hadar Rosen-Sior. Working with
> these student-developers has been a great pleasure, and we feel proud
> and fortunate to have had the opportunity to play a role in their
> education. We also wish to thank our teaching assistants,
> MuawyahAkash, David Rabinowitz, Ran Navok, and Yaron Ukrainitz, who
> helped us run early versions of the course that led to this book.
> Thanks also to Jonathan Gross and Oren Baranes, who worked on related
> projects under the excellent supervision of Dr. Danny Seidner, to Uri
> Zeira and Oren Cohen, for designing an integrated development
> environment for the Jack language, to Tal Achituv, for useful advice
> on open source issues, and to Aryeh Schnall, for careful reading and
> meticulous editing suggestions.
>
> Writing the book without taking any reduction in our regular
> professional duties was not simple, and so we wish to thank esti
> romem, administrative director of the EFI Arazi School of Computer
> Science, for holding the fort in difficult times. Finally, we are
> indebted to the many students who endured early versions of this book
> and helped polish it through numerous bug reports. In the process, we
> hope, they have learned first-hand that insight of James Joyce, that
> mistakes are the portals of discovery.
>
> NoamNisan
>
> Shimon Schocken

![](media/image58.png){width="4.34in" height="6.33in"}

> Figure I.1 The major abstractions underlying the design of a typical
> computing system. The implementation of each level is accomplished
> using abstract services and building blocks from the level below.

Introduction: Hello, World Below

> *The true voyage of discovery consists not of going to new places, but
> of having a new pair of eyes.*

*---Marcel Proust (1871-1922)*

This book is a voyage of discovery. You are about to learn three things:
how computers work, how to

> break complex problems into manageable modules, and how to develop
> large-scale hardware and software systems. This will be a hands-on
> process as you create a complete and working computer systemfrom the
> ground up. The lessons you will learn, which are far more important
> and general than the computer itself, will be gained as side effects
> of this activity. According to the psychologist Carl Rogers, "the only
> kind of learning which significantly influences behavior is
> self-discovered or self-appropriated ---truth that has been
> assimilated in experience." This chapter sketches some of the
> discoveries, truths, and experiences that lie ahead.

The World Above

> If you have taken any programming course, you've probably encountered
> something like the programbelow early in your education. This
> particular program is written in *Jack*---a simple high-level language
> that has a conventional object-based syntax.

![](media/image53.png){width="4.929998906386702in" height="1.52in"}

> Trivial programs like Hello World are deceptively simple. Did you ever
> think about what it takes to actually run such a program on a
> computer? Let's look under the hood. For starters, note that the
> program is nothing more than a bunch of dead characters stored in a
> text file. Thus, the first thing we must do is parse this text,
> uncover its semantics, and reexpress it in some low-level language
> understood by our computer. The result of this elaborate translation
> process, known as compilation, will be yet another text file,
> containing machine-level code.
>
> Of course machine language is also an abstraction---an agreed upon set
> of binary codes. In order to make this abstract formalism concrete, it
> must be realized by some hardware architecture. And this architecture,
> in turn, is implemented by a certain chip *set*---registers, memory
> units, ALU, and so on. Now, every one of these hardware devices is
> constructed from an integrated package of elementary logic gates. And
> these gates, in turn, can be built from primitive gates like Nand and
> Nor. Of course every one of these gates consists of several switching
> devices, typically implemented by transistors. And each transistor is
> made of---Well, we won't go further than that, because that's where
> computer science ends and physics starts.
>
> You may be thinking: "On my computer, compiling and running a program
> is much easier---all I have to do is click some icons or write some
> commands!" Indeed, a modern computer system is like a huge iceberg,
> and most people get to see only the top. Their knowledge of computing
> systems is sketchy and superficial. If, however, you wish to explore
> beneath the surface, then lucky you! There's a fascinating world down
> there, made of some of the most beautiful stuff in computer science.
> An intimate understanding of this underworld is one of the things that
> separate naïve programmers from sophisticated developers---people who
> can create not only application programs, but also complex hardware
> and software technologies. And the best way to understand how these
> technologies work---and we mean understand themin the marrow of your
> bones---is to build a complete computer systemfromscratch.

Abstractions

> You may wonder how it is humanly possible to construct a complete
> computer system from the ground up, starting with nothing more than
> elementary logic gates. This must be an enormously complex enterprise!
> We deal with this complexity by breaking the project into modules, and
> treating each module separately, in a stand-alone chapter. You might
> then wonder, how is it possible to describe and construct these
> modules in isolation? Obviously they are all interrelated! As we will
> show throughout the book, a good modular design implies just that: You
> can work on the individual modules independently, while completely
> ignoring the rest of the system. In fact, you can even build these
> modules in any desired order!
>
> It turns out that this strategy works well thanks to a special gift
> unique to humans: our ability to create and use abstractions. The
> notion of abstraction, central to many arts and sciences, is normally
> taken to be a mental expression that seeks to separate in thought, and
> capture in some concise manner, the essence of some entity. In
> computer science, we take the notion of abstraction very concretely,
> defining it to be a statement of "what the entity does" and ignoring
> the details of "how it does it." This functional description must
> capture all that needs to be known in order to use the entity's
> services, and nothing more. All the work, cleverness, information, and
> drama that went into the entity's implementation are concealed from
> the client who is supposed to use it, since they are simply
> irrelevant. The articulation, use, and implementation of such
> abstractions are the bread and butter of our professional practice:
> Every hardware and software developer is routinely defining
> abstractions (also called "interfaces") and then implementing them, or
> asking other people to implement them. The abstractions are often
> built layer upon layer, resulting in higher and higher levels of
> capabilities.
>
> Designing good abstractions is a practical art, and one that is best
> acquired by seeing many examples. Therefore, this book is based on an
> abstraction-implementation paradigm. Each book chapter presents a key
> hardware or software abstraction, and a project designed to actually
> implement it. Thanks to the modular nature of these abstractions, each
> chapter also entails a stand-alone intellectual unit, inviting the
> reader to focus on two things only: understanding the given
> abstraction (a rich world of its own), and then implementing it using
> abstract services and building blocks from the level below. As you
> push ahead in this journey, it will be rather thrilling to look back
> and appreciate the computer that is gradually taking shape in the wake
> of your efforts.

The World Below

> The multi-tier collection of abstractions underlying the design of a
> computing system can be described top-down, showing how high-level
> abstractions can be reduced into, or expressed by, simpler ones. This
> structure can also be described bottom-up, focusing on how lower-level
> abstractions can be used to construct more complex ones. This book
> takes the latter approach: We begin with the most basic elements
> ---primitive logic gates---and work our way upward, culminating in the
> construction of a general-purpose computer system. And if building
> such a computer is like climbing Mount Everest, then planting a flag
> on the mountaintop is like having the computer run a program written
> in some high-level language. Since we are going to ascend this
> mountain from the ground up, let us survey the book plan in the
> opposite direction ---fromthe top down---starting in the familiar
> territory of high-level programming.
>
> Our tour consists of three main legs. We start at the top, where
> people write and run high-level programs (chapters 9 and 12). We then
> survey the road down to hardware land, tracking the fascinating twists
> and curves of translating high-level programs into machine language
> (chapters 6, 7, 8, 10, 11). Finally, we reach the low grounds of our
> journey, describing how a typical hardware platform is actually
> constructed (chapters 1-5).

High-Level Language Land

> The topmost abstraction in our journey is the art of programming,
> where entrepreneurs and programmers dream up applications and write
> software that implements them. In doing so, they blissfully take for
> granted the two key tools of their trade: the high-level language in
> which they work, and the rich library of services that supports it.
> For example, consider the statement do Output.printString(ʹ ʹHello
> Worldʹ ʹ ). This code invokes an abstract service for printing
> strings---a service that must be implemented somewhere. Indeed, a bit
> of drilling reveals that this service is usually supplied jointly by
> the host operating systemand the standard language library.
>
> What then is a standard language library? And how does an operating
> system (OS) work? These questions are taken up in chapter 12. We start
> by presenting key algorithms relevant to OS services, and then use
> them to implement various mathematical functions, string operations,
> memory allocation tasks, and input/output (I/O) routines. The result
> is a simple operating system, written in the Jack programming
> language.
>
> Jack is a simple object-based language, designed for a single purpose:
> to illustrate the key software engineering principles underlying the
> design and implementation of modern programming languages like Java
> and C#. Jack is presented in chapter 9, which also illustrates how to
> build Jack-based applications, for example, computer games. If you
> have any programming experience with a modern object-oriented
> language, you can start writing Jack programs right away and watch
> them execute on the computer platform developed in previous chapters.
> However, the goal of chapter 9 is not to turn you into a Jack
> programmer, but rather to prepare you to develop the compiler and
> operating system described in subsequent chapters.

The Road Down to Hardware Land

> Before any program can actually run and do something for real, it must
> be translated into the machine language of some target computer
> platform. This compilation process is sufficiently complex to be
> broken into several layers of abstraction, and these usually involve
> three translators: a compiler, a virtual machine implementation, and
> an assembler. We devote five book chapters to this trio, as follows.
>
> The translation task of the compiler is performed in two conceptual
> stages: syntax analysis and code generation. First, the source text is
> analyzed and grouped into meaningful language constructs that can be
> kept in a data structure called a "parse tree." These parsing tasks,
> collectively known as syntax analysis, are described in chapter 10.
> This sets the stage for chapter 11, which shows how the parse tree can
> be recursively processed to yield a program written in an intermediate
> language. As with Java and C#, the intermediate code generated by the
> Jack compiler describes a sequence of generic steps operating on a
> stack-based virtual machine (VM). This classical model, as well as a
> VM implementation that realizes it on an actual computer, are
> elaborated in chapters 7-8. Since the output of our VM implementation
> is a large assembly program, we have to translate it further into
> binary code. Writing an assembler is a relatively simple task, taken
> up in chapter 6.

Hardware Land

> We have reached the most profound step in our journey---the descent
> from machine language to the machine itself---the point where software
> finally meets hardware. This is also the point where Hack enters the
> picture. Hack is a general-purpose computer system, designed to strike
> a balance between simplicity and power. On the one hand, the Hack
> architecture can be built in just a few hours of work, using the
> guidelines and chip set presented in chapters 1-3. At the same time,
> Hack is sufficiently general to illustrate the key operating
> principles and hardware elements underlying the design of any digital
> computer.
>
> The machine language of the Hack platform is specified in chapter 4,
> and the computer design itself is discussed and specified in chapter
> 5. Readers can build this computer as well as all the chips and gates
> mentioned in the book on their home computers, using the
> software-based hardware simulator supplied with the book and the
> Hardware Description Language (HDL) documented in appendix A. All the
> developed hardware modules can be tested using supplied test scripts,
> written in a scripting language documented in appendix B.
>
> The computer that emerges from this construction is based on typical
> components like CPU, RAM, ROM, and simulated screen and keyboard. The
> computer's registers and memory systems are built in chapter 3,
> following a brief discussion of sequential logic. The computer's
> combinational logic, culminating in the Arithmetic Logic Unit (ALU)
> chip, is built in chapter 2, following a brief discussion of Boolean
> arithmetic. All the chips presented in these chapters are based on a
> suite of elementary logic gates, presented and built in chapter 1.
>
> Of course the layers of abstraction don't stop here. Elementary logic
> gates are built from transistors, using technologies based on
> solid-state physics and ultimately quantum mechanics. Indeed, this is
> where the abstractions of the natural world, as studied and formulated
> by physicists, become the building blocks of the abstractions of the
> synthetic worlds built and studied by computer scientists.
>
> This marks the end of our grand tour preview---the descent from the
> high-level peaks of object-based software, all the way down to the
> bricks and mortar of the hardware platform. This typical modular
> rendition of a multi-tier system represents not only a powerful
> engineering paradigm, but also a central dogma in human reasoning,
> going back at least 2,500 years:
>
> *We deliberate not about ends, but about means. For a doctor does not
> deliberate whether he shall heal, nor an orator whether he shall
> persuade \... They assume the end and consider how and by what means
> it is attained, and if it seems easily and best produced thereby;
> while if it is achieved by other means, they consider how it will be
> achieved and by what means this will be achieved, until they come to
> the first cause \... and what is last in the order of analysis seems
> to be first in the order of becoming*. (Aristotles, Nicomachean
> Ethics, Book III, 3, 1112b)
>
> So here's the plan, in the order of becoming. Starting with the
> construction of elementary logic gates (chapter 1), we go bottom-up to
> combinational and sequential chips (chapters 2-3), through the design
> of a typical computer architecture (chapters 4-5) and a typical
> software hierarchy (chapters 6-8), all the way to implementing a
> compiler (chapters 10-11) for a modern object-based language (chapter
> 9), ending with the design and implementation of a simple operating
> system (chapter 12). We hope that the reader has gained a general idea
> of what lies ahead and is eager to push forward on this grand tour of
> discovery. So, assuming that you are ready and set, let the countdown
> start: 1, 0, Go!

1

Boolean Logic

> *Such simple things, And we make of them something so complex it
> defeats us, Almost. ---John Ashbery (b. 1927), American poet*
>
> Every digital device---be it a personal computer, a cellular
> telephone, or a network router---is based on a set of chips designed
> to store and process information. Although these chips come in
> different shapes and forms, they are all made from the same building
> blocks: Elementary logic gates. The gates can be physically
> implemented in many different materials and fabrication technologies,
> but their logical behavior is consistent across all computers. In this
> chapter we start out with one primitive logic gate---Nand---and build
> all the other logic gates from it. The result is a rather standard set
> of gates, which will be later used to construct our computer's
> processing and storage chips. This will be done in chapters 2 and 3,
> respectively.
>
> All the hardware chapters in the book, beginning with this one, have
> the same structure. Each chapter focuses on a well-defined task,
> designed to construct or integrate a certain family of chips. The
> prerequisite knowledge needed to approach this task is provided in a
> brief Background section. The next section provides a complete
> Specification of the chips' abstractions, namely, the various services
> that they should deliver, one way or another. Having presented the
> what, a subsequent Implementation section proposes guidelines and
> hints about how the chips can be actually implemented. A Perspective
> section rounds up the chapter with concluding comments about important
> topics that were left out from the discussion. Each chapter ends with
> a technical Project section. This section gives step-by-step
> instructions for actually building the chips on a personal computer,
> using the hardware simulator supplied with the book.
>
> This being the first hardware chapter in the book, the Background
> section is somewhat lengthy, featuring a special section on hardware
> description and simulation tools.

1.1 Background

> This chapter focuses on the construction of a family of simple chips
> called Boolean gates. Since Boolean gates are physical implementations
> of Boolean functions, we start with a brief treatment of Boolean
> algebra. We then show how Boolean gates implementing simple Boolean
> functions can be interconnected to deliver the functionality of more
> complex chips. We conclude the background section with a description
> of how hardware design is actually done in practice, using software
> simulation tools.

1.1.1 BooleanAlgebra

> Boolean algebra deals with Boolean (also called binary) values that
> are typically labeled true/false, 1/0, yes/no, on/off, and so forth.
> We will use 1 and 0. A Boolean function is a function that operates on
> binary inputs and returns binary outputs. Since computer hardware is
> based on the representation and manipulation of binary values, Boolean
> functions play a central role in the specification, construction, and
> optimization of hardware architectures. Hence, the ability to
> formulate and analyze Boolean functions is the first step toward
> constructing computer architectures.
>
> Truth Table Representation The simplest way to specify a Boolean
> function is to enumerate all the possible values of the function's
> input variables, along with the function's output for each set of
> inputs. This is called the truth table representation of the function,
> illustrated in figure 1.1.
>
> The first three columns of figure 1.1 enumerate all the possible
> binary values of the function's variables. For each one of the 2*^n^*
> possible tuples *υ*~1~\...*υ*~n~(here *n* = 3), the last column gives
> the value of *f*(*υ*~1~\...*υ~n~*).
>
> Boolean Expressions In addition to the truth table specification, a
> Boolean function can also be specified using Boolean operations over
> its input variables. The basic Boolean operators that are typically
> used are "And" (*x* And *y* is 1 exactly when both x and *y* are 1)
> "Or" (*x* Or *y* is 1 exactly when either *x* or *y* or both are 1),
> and "Not" (Not *x* is 1 exactly when *x* is 0). We will use a common
> arithmetic-like notation for these operations: *x* · *y* (or xy) means
> *x* And *y, x* + *y* means *x* Or y, and means Not
> ![](media/image61.png){width="6.0e-2in" height="8.0e-2in"}*x*.
>
> To illustrate, the function defined in figure 1.1 is equivalently
> given by the Boolean expression ![](media/image64.png){width="1.31in"
> height="0.13in"}. For example, let us evaluate this expression on the
> inputs *x* = 0, *y* = 1, *z* = 0 (third row in the table). Since *y*
> is 1, it follows that x + *y* = 1 and thus . The complete verification
> of the equivalence![](media/image56.png){width="5.0e-2in"
> height="0.11in"} between the expression and the truth table is
> achieved by evaluating the expression on each of the eight possible
> input combinations, verifying that it yields the same value listed in
> the table's right column.

![](media/image51.png){width="1.45in" height="1.62in"}

> Figure 1.1 Truth table representation of a Boolean function (example).

Canonical Representation As it turns out, every Boolean function can be
expressed using at least one

> Boolean expression called the *canonical representation*. Starting
> with the function's truth table, we focus on all the rows in which the
> function has value 1. For each such row, we construct a termcreated
> byAnd ing together literals (variables or their negations) that fix
> the values of all the row's inputs. For example, let us focus on the
> third row in figure 1.1, where the function's value is 1. Since the
> variable values in this row are *x* = 0, *y* = 1, *z* = 0, we
> construct the term ![](media/image65.png){width="0.2in"
> height="0.11in"}. Following the same procedure, we construct the terms
> ![](media/image62.png){width="0.2in" height="0.11in"}and
> ![](media/image54.png){width="0.2in" height="0.1in"}for rows 5 and 7.
> Now, if we Or-together all these terms (for all the rows where the
> function has value 1), we get a Boolean expression that is equivalent
> to the given truth table. Thus the canonical representation of the
> Boolean function shown in figure 1.1 is *f* (*x, y, z*) =
> ![](media/image59.png){width="0.95in" height="0.11in"}. This
> construction leads to an important conclusion: Every Boolean function,
> no matter how complex, can be expressed using three Boolean operators
> only: And, Or, and Not.
>
> Two-Input Boolean Functions An inspection of figure 1.1 reveals that
> the number of Boolean functions that can be defined over n binary
> variables is ![](media/image52.png){width="0.16in" height="0.11in"}.
> For example, the sixteen Boolean functions spanned by two variables
> are listed in figure 1.2. These functions were constructed
> systematically, by enumerating all the possible 4-wise combinations of
> binary values in the four right columns. Each function has a
> conventional name that seeks to describe its underlying operation.
> Here are some examples: The name of the Nor function is shorthand for
> Not-Or: Take the Or of *x* and y, then negate the result. The Xor
> function ---shorthand for "exclusive or"---returns 1 when its two
> variables have opposing truth-values and 0 otherwise. Conversely, the
> Equivalence function returns 1 when the two variables have identical
> truth values. The If-*x*-then-*y* function (also known as *x* → y, or
> "*x* Implies *y"*) returns 1 when *x* is 0 or when both *x* and *y*
> are 1. The other functions are self-explanatory.

![](media/image63.png){width="3.22in" height="3.37in"}

> Figure 1.2 All the Boolean functions of two variables.
>
> The Nand function (as well as the Nor function) has an interesting
> theoretical property: Each one of the operations And, Or, and Not can
> be constructed from it, and it alone (e.g., *x* Or *y* = (*x* Nand x)
> Nand (*y* Nand y). And since every Boolean function can be constructed
> fromAnd, Or, and Not operations using the
>
> canonical representation method, it follows that every Boolean
> function can be constructed from Nand operations alone. This result
> has far-reaching practical implications: Once we have in our disposal
> a physical device that implements Nand, we can use many copies of this
> device (wired in a certain way) to implement in hardware any Boolean
> function.

1.1.2 Gate Logic

> A *gate* is a physical device that implements a Boolean function. If a
> Boolean function f operates on n variables and returns *m* binary
> results (in all our examples so far, m was 1), the gate that
> implements f will have n input pins and m output pins. When we put
> some values v~1~\...v~n~in the gate's input pins, the gate's
> "logic"---its internal structure---should compute and output
> *f*(*υ*~1~\...*υ*~n~). And just like complex Boolean functions can be
> expressed in terms of simpler functions, complex gates are composed
> frommore elementary gates. The simplest gates of all are made from
> tiny switching devices, called transistors, wired in a certain
> topology designed to effect the overall gate functionality.
>
> Although most digital computers today use electricity to represent and
> transmit binary data from one gate to another, any alternative
> technology permitting switching and conducting capabilities can be
> employed. Indeed, during the last fifty years, researchers have built
> many hardware implementations of Boolean functions, including
> magnetic, optical, biological, hydraulic, and pneumatic mechanisms.
> Today, most gates are implemented as transistors etched in silicon,
> packaged as chips. In this book we use the words chip and gate
> interchangeably, tending to use the termgates for simple chips.
>
> The availability of alternative switching technology options, on the
> one hand, and the observation that Boolean algebra can be used to
> abstract the behavior of any such technology, on the other, is
> extremely important. Basically, it implies that computer scientists
> don't have to worry about physical things like electricity, circuits,
> switches, relays, and power supply. Instead, computer scientists can
> be content with the abstract notions of Boolean algebra and gate
> logic, trusting that someone else (the physicists and electrical
> engineers---bless their souls) will figure out how to actually realize
> themin hardware. Hence, a primitive gate (see figure 1.3) can be
> viewed as a black box device that implements an elementary logical
> operation in one way or another---we don't care how. A hardware
> designer starts from such primitive gates and designs more complicated
> functionality by interconnecting them, leading to the construction of
> composite gates.

![](media/image28.png){width="3.9in" height="0.39in"}

Figure 1.3 Standard symbolic notation of some elementary logic gates.

![](media/image34.png){width="4.45in" height="1.29in"}

Figure 1.4 Composite implementation of a three-way And gate. The
rectangle on the right defines the

> conceptual boundaries of the gate interface.
>
> Primitive and Composite Gates Since all logic gates have the same
> input and output semantics (0's and 1's), they can be chained
> together, creating composite gates of arbitrary complexity. For
> example, suppose we are asked to implement the 3-way Boolean function
> And(*a, b, c*). Using Boolean algebra, we can begin by observing that
> *a·b·c* = (*a*·*b*)·*c*, or, using prefix notation, And(*a*, b, c) =
> And(And(*a, b*), *c*). Next, we can use this result to construct the
> composite gate depicted in figure 1.4.
>
> The construction described in figure 1.4 is a simple example of gate
> logic, also called logic design. Simply put, logic design is the art
> of interconnecting gates in order to implement more complex
> functionality, leading to the notion of composite gates. Since
> composite gates are themselves realizations of (possibly complex)
> Boolean functions, their "outside appearance" (e.g., left side of
> figure 1.4) looks just like that of primitive gates. At the same time,
> their internal structure can be rather complex.
>
> We see that any given logic gate can be viewed from two different
> perspectives: external and internal. The right-hand side of figure 1.4
> gives the gate's internal architecture, or implementation, whereas the
> left side shows only the gate interface, namely, the input and output
> pins that it exposes to the outside world. The former is relevant only
> to the gate designer, whereas the latter is the right level of detail
> for other designers who wish to use the gate as an abstract
> off-the-shelf component, without paying attention to its internal
> structure.
>
> Let us consider another logic design example---that of a Xor gate. As
> discussed before, Xor(*a*, b) is 1 exactly when either a is 1 and *b*
> is 0, or when a is 0 and *b* is 1. Said otherwise, Xor(*a, b*) =
> Or(And(*a*, Not(*b*)), And(Not(*a*), *b*)). This definition leads to
> the logic design shown in figure 1.5.
>
> Note that the gate interface is unique: There is only one way to
> describe it, and this is normally done using a truth table, a Boolean
> expression, or some verbal specifica-tion. This interface, however,
> can be realized using many different implementations, some of which
> will be better than others in terms of cost, speed, and simplicity.
> For example, the Xor function can be implemented using four, rather
> than five, And, Or, and Not gates. Thus, from a functional standpoint,
> the fundamental requirement of logic design is that *the gate
> implementation will realize its stated interface, in one way or
> another*. From an efficiency standpoint, the general rule is to try to
> do more with less, that is, use as few gates as possible.

![](media/image35.png){width="4.9in" height="1.58in"}

> Figure 1.5 Xor gate, along with a possible implementation.
>
> To sum up, the art of logic design can be described as follows: Given
> a gate specification (interface), find an efficient way to implement
> it using other gates that were already implemented. This, in a
> nutshell, is what we will do in the rest of this chapter.

1.1.3 Actual Hardware Construction

> Having described the logic of composing complex gates from simpler
> ones, we are now in a position to discuss how gates are actually
> built. Let us start with an intentionally naïve example. Suppose we
> open a chip fabrication shop in our home garage. Our first contract is
> to build a hundred Xor gates. Using the order's downpayment, we
> purchase a soldering gun, a roll of copper wire, and three bins
> labeled "And gates," "Or gates," and "Not gates," each containing many
> identical copies of these elementary logic gates. Each of these gates
> is sealed in a plastic casing that exposes some input and output pins,
> as well as a power supply plug. To get started, we pin figure 1.5 to
> our garage wall and proceed to realize it using our hardware. First,
> we take two And gates, two Not gates, and one Or gate, and mount them
> on a board according to the figure's layout. Next, we connect the
> chips to one another by running copper wires among them and by
> soldering the wire ends to the respective input/output pins. Now, if
> we follow the gate diagram carefully, we will end up having three
> exposed wire ends. We then solder a pin to each one of these wire
> ends, seal the entire device (except for the three pins) in a plastic
> casing, and label it "Xor." We can repeat this assembly process many
> times over. At the end of the day, we can store all the chips that
> we've built in a new bin and label it "Xor gates." If we (or other
> people) are asked to construct some other chips in the future, we'll
> be able to use these Xor gates as elementary building blocks, just as
> we used the And, Or, and Not gates before.
>
> As the reader has probably sensed, the garage approach to chip
> production leaves much to be desired. For starters, there is no
> guarantee that the given chip diagram is correct. Although we can
> prove correctness in simple cases like Xor, we cannot do so in many
> realistically complex chips. Thus, we must settle for empirical
> testing: Build the chip, connect it to a power supply, activate and
> deactivate the input pins in various configurations, and hope that the
> chip outputs will agree with its specifications. If the chip fails to
> deliver the desired outputs, we will have to tinker with its physical
> structure---a rather messy affair. Further, even if we will come up
> with the right design, replicating the chip assembly process many
> times over will be a time-consuming and error-prone affair. There must
> be a better way!

1.1.4 Hardware Description Language (HDL)

> Today, hardware designers no longer build anything with their bare
> hands. Instead, they plan and optimize the chip architecture on a
> computer workstation, using structured modeling formalisms like
> Hardware Description Language, or HDL (also known as VHDL, where V
> stands for *Virtual*). The designer specifies the chip structure by
> writing an HDL program, which is then subjected to a rigorous battery
> of tests. These tests are carried out virtually, using computer
> simulation: A special software tool, called a hardware simulator,
> takes the HDL program as input and builds an image of the modeled chip
> in memory. Next, the designer can instruct the simulator to test the
> virtual chip on various sets of inputs, generating simulated chip
> outputs. The outputs can then be compared to the desired results, as
> mandated by the client who ordered the chip built.
>
> In addition to testing the chip's correctness, the hardware designer
> will typically be interested in a variety of parameters such as speed
> of computation, energy consumption, and the overall cost implied by
> the chip design. All these parameters can be simulated and quantified
> by the hardware simulator, helping the designer optimize the design
> until the simulated chip delivers desired cost/performance levels.
>
> Thus, using HDL, one can completely plan, debug, and optimize the
> entire chip before a single penny is spent on actual production. When
> the HDL program is deemed complete, that is, when the performance of
> the simulated chip satisfies the client who ordered it, the HDL
> program can become the blueprint from which many copies of the
> physical chip can be stamped in silicon. This final step in the chip
> life cycle---
>
> from an optimized HDL program to mass production---is typically
> out-sourced to companies that specialize in chip fabrication, using
> one switching technology or another.
>
> Example: Building a XorGate As we have seen in figures 1.2 and 1.5,
> one way to define exclusive or is Xor(*a*, *b*) = Or(And(*a*,
> Not(*b*)), And(Not(*a*), *b*)). This logic can be expressed either
> graphically, as a gate diagram, or textually, as an HDL program. The
> latter program is written in the HDL variant used throughout this
> book, defined in appendix A. See figure 1.6 for the details.
>
> Explanation An HDL definition of a chip consists of a header section
> and a parts section. The header section specifies the chip interface,
> namely the chip name and the names of its input and output pins. The
> parts section describes the names and topology of all the lower-level
> parts (other chips) from which this chip is constructed. Each part is
> represented by a statement that specifies the part name and the way it
> is connected to other parts in the design. Note that in order to write
> such statements legibly, the HDL programmer must have a complete
> documentation of the underlying parts' interfaces. For example, figure
> 1.6 assumes that the input and output pins of the Not gate are labeled
> in and out, and those of And and Or are labeled a, b and out. This
> API-type information is not obvious, and one must have access to it
> before one can plug the chip parts into the present code.
>
> Inter-part connections are described by creating and connecting
> internal pins, as needed. For example, consider the bottom of the gate
> diagram, where the output of a Not gate is piped into the input of a
> subsequent And gate. The HDL code describes this connection by the
> pair of statements Not(\...,out=nota) and And(a=nota,\...). The first
> statement creates an internal pin (outbound wire) named nota, feeding
> out into it. The second statement feeds the value of nota into the a
> input of an And gate. Note that pins may have an unlimited fan out.
> For example, in figure 1.6, each input is simultaneously fed into two
> gates. In
>
> gate diagrams, multiple connections are described using forks. In HDL,
> the existence of forks is implied by the code.

![](media/image32.png){width="5.66in" height="4.1in"}

> Figure 1.6 HDL implementation of a Xor gate.
>
> Testing Rigorous quality assurance mandates that chips be tested in a
> specific, replicable, and well documented fashion. With that in mind,
> hardware simulators are usually designed to run test scripts, written
> in some scripting language. For example, the test script in figure 1.6
> is written in the scripting language understood by the hardware
> simulator supplied with the book. This scripting language is described
> fully in appendix B.
>
> Let us give a brief description of the test script from figure 1.6.
> The first two lines of the test script instruct the simulator to load
> the Xor.hdl program and get ready to print the values of selected
> variables. Next, the script lists a series of testing scenarios,
> designed to simulate the various contingencies under which the Xor
> chip will have to operate in "real-life" situations. In each scenario,
> the script instructs the simulator to bind the chip inputs to certain
> data values, compute the resulting output, and record the test results
> in a designated output file. In the case of simple gates like Xor, one
> can write an exhaustive test script that enumerates all the possible
> input values of the gate. The resulting output file (right side of
> figure 1.6) can then be viewed as a complete empirical proof that the
> chip is well designed. The luxury of such certitude is not feasible in
> more complex chips, as we will see later.

1.1.5 Hardware Simulation

> Since HDL is a hardware construction language, the process of writing
> and debugging HDL programs is quite similar to software development.
> The main difference is that instead of writing code in a language like
> Java, we write it in HDL, and instead of using a compiler to translate
> and test the code, we use a hardware simulator. The hardware simulator
> is a computer programthat knows how to parse and interpret HDL code,
> turn it into an executable representation, and test it according to
> the specifications of a given test script. There exist many commercial
> hardware simulators on the market, and these vary greatly in terms of
> cost, complexity, and ease of use. Together with this book we provide
> a simple (and free!) hardware simulator that is sufficiently powerful
> to support sophisticated hardware design projects. In particular, the
> simulator provides all the necessary tools for building, testing, and
> integrating all the chips presented in the book, leading to the
> construction of a general-purpose computer. Figure 1.7 illustrates a
> typical chip simulation session.

1.2 Specification

> This section specifies a typical set of gates, each designed to carry
> out a common Boolean operation. These gates will be used in the
> chapters that follow to construct the full architecture of a typical
> modern computer. Our starting point is a single primitive Nand gate,
> from which all other gates will be derived recursively. Note that we
> provide only the gates' specifications, or interfaces, delaying
> implementation details until a subsequent section. Readers who wish to
> construct the specified gates in HDL are encouraged to do so,
> referring to appendix A as needed. All the gates can be built and
> simulated on a personal computer, using the hardware simulator
> supplied with the book.

![](media/image33.png){width="5.66in" height="4.22in"}

> Figure 1.7 A screen shot of simulating an Xor chip on the hardware
> simulator. The simulator state is shown just after the test script has
> completed running. The pin values correspond to the last simulation
> step (*a* = *b* = 1). Note that the output file generated by the
> simulation is consistent with the Xor truth table, indicating that the
> loaded HDL program delivers a correct Xor functionality. The compare
> file, not shown in the figure and typically specified by the chip's
> client, has exactly the same structure and contents as that of the
> output file. The fact that the two files agree with each other is
> evident from the status message displayed at the bottomof the screen.

1.2.1 The NandGate

> The starting point of our computer architecture is the Nand gate, from
> which all other gates and chips are built. The Nand gate is designed
> to compute the following Boolean function:

![](media/image42.png){width="1.3in" height="0.88in"}

> Throughout the book, we use "chip API boxes" to specify chips. For
> each chip, the API specifies the chip name, the names of its input and
> output pins, the function or operation that the chip effects, and an
> optional comment.

![](media/image39.png){width="4.929998906386702in" height="1.16in"}

1.2.2 Basic Logic Gates

> Some of the logic gates presented here are typically referred to as
> "elementary" or "basic." At the same time, every one of them can be
> composed from Nand gates alone. Therefore, they need not be viewed as
> primitive.
>
> Not The single-input Not gate, also known as "converter," converts its
> input from 0 to 1 and vice versa. The gate API is as follows:

![](media/image40.png){width="4.929998906386702in" height="0.78in"}

> And The And function returns 1 when both its inputs are 1, and 0
> otherwise.

![](media/image46.png){width="4.929998906386702in" height="0.78in"}

> Or The Or function returns 1 when at least one of its inputs is 1, and
> 0 otherwise. ![](media/image47.png){width="4.929998906386702in"
> height="0.78in"}
>
> Xor The Xor function, also known as "exclusive or," returns 1 when its
> two inputs have opposing values, and 0 otherwise.

![](media/image44.png){width="4.929998906386702in" height="0.78in"}

> Multiplexor A multiplexor (figure 1.8) is a three-input gate that uses
> one of the inputs, called "selection bit," to select and output one of
> the other two inputs, called "data bits." Thus, a better name for this
> device might have been selector. The name multiplexor was adopted from
> communications systems, where similar devices are used to serialize
> (multiplex) several input signals over a single output wire.

![](media/image45.png){width="4.93in" height="0.78in"}

![](media/image49.png){width="3.11in" height="1.62in"}

> Figure 1.8 Multiplexor. The table at the top right is an abbreviated
> version of the truth table on the left.

![](media/image50.png){width="2.82in" height="0.87in"}

> Figure 1.9 Demultiplexor.

![](media/image48.png){width="4.93in" height="0.81in"}

1.2.3 Multi-Bit Versions of Basic Gates

> Computer hardware is typically designed to operate on multi-bit arrays
> called "buses." For example, a basic requirement of a 32-bit computer
> is to be able to compute (bit-wise) an And function on two given
> 32-bit buses. To implement this operation, we can build an array of 32
> binary And gates, each operating separately on a pair of bits. In
> order to enclose all this logic in one package, we can encapsulate the
> gates array in a single chip interface consisting of two 32-bit input
> buses and one 32-bit output bus.
>
> This section describes a typical set of such multi-bit logic gates, as
> needed for the construction of a typical 16-bit computer. We note in
> passing that the architecture of *n*-bit logic gates is basically the
> same irrespective of *n*'s value.
>
> When referring to individual bits in a bus, it is common to use an
> array syntax. For example, to refer to individual bits in a 16-bit bus
> named data, we use the notation data \[0\], data \[1\],\...,
> data\[15\].
>
> Multi-Bit Not An *n*-bit Not gate applies the Boolean operation Not to
> every one of the bits in its *n*-bit input bus:

![](media/image3.png){width="4.929998906386702in" height="0.81in"}

> Multi-Bit And An *n*-bit And gate applies the Boolean operation And to
> every one of the n bit-pairs arrayed in its two *n*-bit input buses:

![](media/image4.png){width="4.929998906386702in" height="0.81in"}

> Multi-Bit Or An *n*-bit Or gate applies the Boolean operation Or to
> every one of the n bit-pairs arrayed in its two *n*-bit input buses:

![](media/image1.png){width="4.929998906386702in" height="0.81in"}

> Multi-Bit Multiplexor An *n*-bit multiplexor is exactly the same as
> the binary multiplexor described in figure 1.8, except that the two
> inputs are each *n*-bit wide; the selector is a single bit.

![](media/image2.png){width="4.93in" height="0.99in"}

1.2.4 Multi-Way Versions of Basic Gates

> Many 2-way logic gates that accept two inputs have natural
> generalization to multi-way variants that accept an arbitrary number
> of inputs. This section describes a set of multi-way gates that will
> be used subsequently in various chips in our computer architecture.
> Similar generalizations can be developed for other architectures, as
> needed.
>
> Multi-Way Or An *n*-way Or gate outputs 1 when at least one of its n
> bit inputs is 1, and 0 otherwise. Here is the 8-way variant of this
> gate:

![](media/image7.png){width="4.929998906386702in" height="0.81in"}

> Multi-Way/Multi-Bit Multiplexor An *m*-way *n*-bit multiplexor selects
> one of m n-bit input buses and outputs it to a single *n*-bit output
> bus. The selection is specified by a set of *k* control bits, where
> *k* = log~2~*m*. Figure 1.10 depicts a typical example.
>
> The computer platform that we develop in this book requires two
> variations of this chip: A 4-way 16- bit multiplexor and an 8-way
> 16-bit multiplexor:

![](media/image8.png){width="3.7899989063867014in" height="1.25in"}

> Figure 1.10 4-way multiplexor. The width of the input and output buses
> may vary.

![](media/image5.png){width="4.93in" height="3.49in"}

> Multi-Way/Multi-Bit Demultiplexor An *m*-way *n*-bit demultiplexor
> (figure 1.11) channels a single *n*-bit input into one of *m* possible
> *n*-bit outputs. The selection is specified by a set of *k* control
> bits, where *k* = log~2~*m*.
>
> The specific computer platform that we will build requires two
> variations of this chip: A 4-way 1-bit demultiplexor and an 8-way
> 1-bit multiplexor, as follows.

![](media/image6.png){width="4.55in" height="1.14in"}

> Figure 1.11 4-way demultiplexor.

![](media/image9.png){width="4.93in" height="3.1399989063867015in"}

1.3 Implementation

> Similar to the role of axioms in mathematics, primitive gates provide
> a set of elementary building blocks from which everything else can be
> built. Operationally, primitive gates have an "off-the-shelf"
> implementation that is supplied externally. Thus, they can be used in
> the construction of other gates and chips without worrying about their
> internal design. In the computer architecture that we are now
> beginning to build, we have chosen to base all the hardware on one
> primitive gate only: Nand. We now turn to outlining the first stage of
> this bottom-up hardware construction project, one gate at a time.
>
> Our implementation guidelines are intentionally partial, since we want
> you to discover the actual gate architectures yourself. We reiterate
> that each gate can be implemented in more than one way; the simpler
> the implementation, the better.
>
> Not: The implementation of a unary Not gate froma binary Nand gate is
> simple. Tip: Think positive. And: Once again, the gate implementation
> is simple. Tip: Think negative.
>
> Or/Xor: These functions can be defined in terms of some of the Boolean
> functions implemented previously, using some simple Boolean
> manipulations. Thus, the respective gates can be built using
> previously built gates.
>
> Multiplexor/ Demultiplexor: Likewise, these gates can be built using
> previously built gates.
>
> Multi-Bit Not/And/Or Gates: Since we already know how to implement the
> elementary versions of these gates, the implementation of their
> *n*-ary versions is simply a matter of constructing arrays of n
> elementary gates, having each gate operate separately on its bit
> inputs. This implementation task is rather boring, but it will carry
> its weight when these multi-bit gates are used in more complex chips,
> as described in subsequent chapters.
>
> Multi-Bit Multiplexor: The implementation of an *n*-ary multiplexor is
> simply a matter of feeding the same selection bit to every one of *n*
> binary multiplexors. Again, a boring task resulting in a very useful
> chip.
>
> Multi-Way Gates: Implementation tip: Think forks.

1.4 Perspective

> This chapter described the first steps taken in an applied digital
> design project. In the next chapter we will build more complicated
> functionality using the gates built here. Although we have chosen to
> use Nand as our basic building block, other approaches are possible.
> For example, one can build a complete computer platform using Nor
> gates alone, or, alternatively, a combination of And, Or, and Not
> gates. These constructive approaches to logic design are theoretically
> equivalent, just as all theorems in
>
> geometry can be founded on different sets of axioms as alternative
> points of departure. The theory and practice of such constructions are
> covered in standard textbooks about digital design or logic design.
> Throughout the chapter, we paid no attention to efficiency
> considerations such as the number of elementary gates used in
> constructing a composite gate or the number of wire crossovers implied
> by the design. Such considerations are critically important in
> practice, and a great deal of computer science and electrical
> engineering expertise focuses on optimizing them. Another issue we did
> not address at all is the physical implementation of gates and chips
> using the laws of physics, for example, the role of transistors
> embedded in silicon. There are of course several such implementation
> options, each having its own characteristics (speed, power
> requirements, production cost, etc.). Any nontrivial coverage of these
> issues requires some background in electronics and physics.

1.5 Project

> Objective Implement all the logic gates presented in the chapter. The
> only building blocks that you can use are primitive Nand gates and the
> composite gates that you will gradually build on top of them.
>
> Resources The only tool that you need for this project is the hardware
> simulator supplied with the book. All the chips should be implemented
> in the HDL language specified in appendix A. For each one of the chips
> mentioned in the chapter, we provide a skeletal .hdl program (text
> file) with a missing implementation part. In addition, for each chip
> we provide a .tst script file that tells the hardware simulator how to
> test it, along with the correct output file that this script should
> generate, called .cmp or "compare file." Your job is to complete the
> missing implementation parts of the supplied .hdl programs.
>
> Contract When loaded into the hardware simulator, your chip design
> (modified .hdl program), tested on the supplied .tst file, should
> produce the outputs listed in the supplied .cmp file. If that is not
> the case, the simulator will let you know.
>
> Tips The Nand gate is considered primitive and thus there is no need
> to build it: Whenever you use Nand in one of your HDL programs, the
> simulator will automatically invoke its built-in
> tools/builtIn/Nand.hdl implementation. We recommend implementing the
> other gates in this project in the order in which they appear in the
> chapter. However, since the builtIn directory features working
> versions of all the chips described in the book, you can always use
> these chips without defining them first: The simulator will
> automatically use their built-in versions.
>
> For example, consider the skeletal Mux.hdl program supplied in this
> project. Suppose that for one reason or another you did not complete
> this program's implementation, but you still want to use Mux gates as
> internal parts in other chip designs. This is not a problem, thanks to
> the following convention. If our simulator fails to find a Mux.hdl
> file in the current directory, it automatically invokes a built-in Mux
> implementation, pre-supplied with the simulator's software. This
> built-in implementation---a Java class stored in the built In
> directory---has the same interface and functionality as those of the
> Mux gate described in the book. Thus, if you want the simulator to
> ignore one or more of your chip implementations, simply move the
> corresponding .hdl files out of the current directory.
>
> Steps We recommend proceeding in the following order:
>
> 0\. The *hardware simulator* needed for this project is available in
> the tools directory of the book's software suite.
>
> 1\. Read appendix A, sections A1-A6 only.
>
> 2\. Go *through the hardware simulator tutorial,* parts I, II, and III
> only.
>
> 3\. Build and simulate all the chips specified in the projects/01
> directory.

2

Boolean Arithmetic

> *Counting is the religion of this generation, its hope and salvation.*

*---Gertrude Stein (1874-1946)*

> In this chapter we build gate logic designs that represent numbers and
> perform arithmetic operations on them. Our starting point is the set
> of logic gates built in chapter 1, and our ending point is a fully
> functional Arithmetic Logical Unit. The ALU is the centerpiece chip
> that executes all the arithmetic and logical operations performed by
> the computer. Hence, building the ALU functionality is an important
> step toward understanding how the Central Processing Unit (CPU) and
> the overall computer work.
>
> As usual, we approach this task gradually. The first section gives a
> brief Background on how binary codes and Boolean arithmetic can be
> used, respectively, to represent and add signed numbers. The
> Specification section describes a succession of adder chips, designed
> to add two bits, three bits, and pairs of *n*-bit binary numbers. This
> sets the stage for the ALU specification, which is based on a
> sophisticated yet simple logic design. The Implementation and Project
> sections provide tips and guidelines on how to build the adder chips
> and the ALU on a personal computer, using the hardware simulator
> supplied with the book.
>
> Binary addition is a simple operation that runs deep. Remarkably, most
> of the operations performed by digital computers can be reduced to
> elementary additions of binary numbers. Therefore, constructive
> understanding of binary addition holds the key to the implementation
> of numerous computer operations that depend on it, one way or another.

2.1 Background

> Binary Numbers Unlike the decimal system, which is founded on base 10,
> the binary system is founded on base 2. When we are given a certain
> binary pattern, say "10011," and we are told that this pattern is
> supposed to represent an integer number, the decimal value of this
> number is computed by convention as follows:

![](media/image10.png){width="3.23in" height="0.16in"}

> \(1\)
>
> In general, let *x* = *x~n~x~n~*~-1~\...*x*~0~ be a string of digits.
> The value of *x* in base b, denoted (*x*)*~b~,* is defined as follows:

![](media/image11.png){width="1.57in" height="0.34in"}

> \(2\)
>
> The reader can verify that in the case of (10011)*~two~*, rule (2)
> reduces to calculation (1). The result of calculation (1) happens to
> be 19. Thus, when we press the keyboard keys labeled '1', '9' and
> ENTER while running, say, a spreadsheet program, what ends up in some
> register in the computer's memory is the binary code 10011. More
> precisely, if the computer happens to be a 32-bit machine, what gets
> stored in the register is the bit pattern
> 00000000000000000000000000010011.
>
> Binary AdditionA pair of binary numbers can be added digit by digit
> from right to left, according to the same elementary school method
> used in decimal addition. First, we add the two right-most digits,
> also called the least significant bits (LSB) of the two binary
> numbers. Next, we add the resulting carry bit (which is either 0 or 1)
> to the sum of the next pair of bits up the significance ladder. We
> continue the process until the two most significant bits (MSB) are
> added. If the last bit-wise addition generates a carry of 1, we can
> report overflow; otherwise, the addition completes successfully:

![](media/image14.png){width="2.71in" height="0.87in"}

> We see that computer hardware for binary addition of two *n*-bit
> numbers can be built from logic gates designed to calculate the sum of
> three bits (pair of bits plus carry bit). The transfer of the
> resulting carry bit forward to the addition of the next significant
> pair of bits can be easily accomplished by proper wiring of the 3-bit
> adder gates.
>
> Signed Binary Numbers A binary system with n digits can generate a set
> of 2*^n^* different bit patterns. If we have to represent signed
> numbers in binary code, a natural solution is to split this space into
> two equal subsets. One subset of codes is assigned to represent
> positive numbers, and the other negative numbers. Ideally, the coding
> scheme should be chosen in such a way that the introduction of signed
> numbers would complicate the hardware implementation as little as
> possible.
>
> This challenge has led to the development of several coding schemes
> for representing signed numbers in binary code. The method used today
> by almost all computers is called the 2's complement method, also
> known as radix complement. In a binary system with n digits, the 2's
> complement of the number *x* is defined as follows:

![](media/image15.png){width="1.38in" height="0.33in"}

> For example, in a 5-bit binary system, the 2's complement
> representation of--2 or "minus(00010)*~two~*" is 2^5^--(00010)*~two~*
> = (32)*~ten~*--(2)*~ten~* = (30)*~ten~* = (11110)*~two~*. To check the
> calculation, the reader can verify that (00010)*~two~* +
> (11110)*~two~* = (00000)*~two~*. Note that in the latter computation,
> the sum is actually (100000)*~two~*, but since we are dealing with a
> 5-bit binary system, the left-most sixth bit is simply ignored. As a
> rule, when the 2's complement method is applied to *n*-bit numbers,
> *x* + (--*x*) always sums up to 2*^n^* (i.e., 1 followed by n 0's)---a
> property that gives the method its name. Figure 2.1 illustrates a
> 4-bit binary systemwith the 2's complement method.
>
> An inspection of figure 2.1 suggests that an *n*-bit binary system
> with 2's complement representation has the following properties:

![](media/image12.png){width="1.48in" height="1.97in"}

> Figure 2.1 2's complement representation of signed numbers in a 4-bit
> binary system.
>
> ■ The systemcan code a total of 2*^n^* signed numbers, of which the
> maximal and minimal numbers are 2^*n*--1^-- 1 and--2^*n*--1^,
> respectively.
>
> ■ The codes of all positive numbers begin with a 0.
>
> ■ The codes of all negative numbers begin with a 1.
>
> ■ To obtain the code of--*x* fromthe code of x, leave all the trailing
> (least significant) 0's and the first least significant 1 intact, then
> flip all the remaining bits (convert 0's to 1's and vice versa). An
> equivalent shortcut, which is easier to implement in hardware, is to
> flip all the bits of *x* and add 1 to the result.
>
> A particularly attractive feature of this representation is that
> addition of any two signed numbers in 2's complement is exactly the
> same as addition of positive numbers. Consider, for example, the
> addition operation (--2) + (--3). Using 2's complement (in a 4-bit
> representation), we have to add, in binary, (1110)*~two~* +
> (1101)*~two~*. Without paying any attention to which numbers (positive
> or negative) these codes represent, bit-wise addition will yield 1011
> (after throwing away the overflow bit). As figure 2.1 shows, this
> indeed is the 2's complement representation of -5.
>
> In short, we see that the 2's complement method facilitates the
> addition of any two signed numbers without requiring special hardware
> beyond that needed for simple bit-wise addition. What about
> subtraction? Recall that in the 2's complement method, the arithmetic
> negation of a signed number *x*, that is, computing--*x*, is achieved
> by negating all the bits of *x* and adding 1 to the result. Thus
> subtraction can be easily handled by *x*--*y* = *x* + (--*y*). Once
> again, hardware complexity is kept to a minimum.
>
> The material implications of these theoretical results are
> significant. Basically, they imply that a single chip, called
> Arithmetic Logical Unit, can be used to encapsulate all the basic
> arithmetic and logical operators performed in hardware. We now turn to
> specify one suchALU, beginning with the specification of an adder
> chip.

2.2 Specification

2.2.1 Adders

> We present a hierarchy of three adders, leading to a multi-bit adder
> chip:
>
> • *Half-adder:* designed to add two bits
>
> • *Full-adder:* designed to add three bits
>
> • *Adder:* designed to add two *n*-bit numbers

![](media/image13.png){width="4.929998906386702in" height="2.34in"}

> Figure 2.2 Half-adder, designed to add 2 bits.
>
> We also present a special-purpose adder, called incrementer, designed
> to add 1 to a given number.
>
> Half-Adder The first step on our way to adding binary numbers is to be
> able to add two bits. Let us call the least significant bit of the
> addition sum, and the most significant bit carry. Figure 2.2 presents
> a chip, called half-adder, designed to carry out this operation.
>
> Full-Adder Now that we know how to add two bits, figure 2.3 presents a
> *full-adder* chip, designed to add three bits. Like the half-adder
> case, the full-adder chip produces two outputs: the least significant
> bit of the addition, and the carry bit.
>
> Adder Memory and register chips represent integer numbers by *n*-bit
> patterns, n being 16, 32, 64, and so forth---depending on the computer
> platform. The chip whose job is to add such numbers is called a multi
> bit adder, or simply adder. Figure 2.4 presents a 16-bit adder, noting
> that the same logic and specifications scale up as is to any *n*-bit
> adder.

IncrementerIt is convenient to have a special-purpose chip dedicated to
adding the constant 1 to a given number. Here is the specification of a
16-bit incrementer:

![](media/image18.png){width="4.93in" height="2.88in"}

Figure 2.3 Full-adder, designed to add 3 bits.

![](media/image19.png){width="4.93in" height="2.08in"}

Figure 2.4 16-bit adder. Addition of two *n*-bit binary numbers for any
n is "more of the same."![](media/image16.png){width="4.93in"
height="1.14in"}

2.2.2 The Arithmetic Logic Unit (ALU)

> The specifications of the adder chips presented so far were generic,
> meaning that they hold for any computer. In contrast, this section
> describes an ALU that will later become the centerpiece of a specific
> computer platform called Hack. At the same time, the principles
> underlying the design of our ALU are rather general. Further, our ALU
> architecture achieves a great deal of functionality using a minimal
> set of internal parts. In that respect, it provides a good example of
> an efficient and elegant logic design.
>
> The Hack ALU computes a fixed set of functions out = *f~i~*(*x*, y)
> where *x* and *y* are the chip's two 16-bit inputs, out is the chip's
> 16-bit output, and *f~i~*is an arithmetic or logical function selected
> from a fixed repertoire of eighteen possible functions. We instruct
> the ALU which function to compute by setting six input bits, called
> control bits, to selected binary values. The exact input-output
> specification is given in figure 2.5, using pseudo-code.
>
> Note that each one of the six control bits instructs the ALU to carry
> out a certain elementary operation. Taken together, the combined
> effects of these operations cause the ALU to compute a variety of
> useful functions. Since the overall operation is driven by six control
> bits, the ALU can potentially compute 2^6^ = 64 different functions.
> Eighteen of these functions are documented in figure 2.6.
>
> We see that programming our ALU to compute a certain function *f*(*x*,
> y) is done by setting the six control bits to the code of the desired
> function. From this point on, the internal ALU logic specified in
> figure 2.5 should cause the ALU to output the value *f*(*x*, y)
> specified in figure 2.6. Of course, this does not happen miraculously,
> it's the result of careful design.
>
> For example, let us consider the twelfth row of figure 2.6, where the
> ALU is instructed to compute the function x-1. The zx and nx bits are
> 0, so the x input is neither zeroed nor negated. The zy and ny bits
> are 1, so the y input is first zeroed, and then negated bit-wise.
> Bit-wise negation of zero, (000 \...00)~two~, gives (111 \...11)~two~,
> the 2's complement code of -1. Thus the ALU inputs end up being x and
> -1. Since the f-bit is 1, the selected operation is arithmetic
> addition, causing the ALU to calculate *x*+ (-1). Finally, since the
> no bit is 0, the output is not negated but rather left as is. To
> conclude, the ALU ends up computing x-1, which was our goal.
>
> ![](media/image17.png){width="5.66in" height="5.98in"}Figure 2.5 The
> Arithmetic Logic Unit.

![](media/image20.png){width="5.65in" height="4.19in"}

> Figure 2.6 The ALU truth table. Taken together, the binary operations
> coded by the first six columns effect the function listed in the right
> column (we use the symbols !, &, and \| to represent the operators
> Not, And, and Or, respectively, performed bit-wise). The complete ALU
> truth table consists of sixty-four rows, of which only the eighteen
> presented here are of interest.
>
> Does the ALU logic described in figure 2.6 compute every one of the
> other seventeen functions listed in the figure's right column? To
> verify that this is indeed the case, the reader can pick up some other
> rows in the table and prove their respective ALU operation. We note
> that some of these computations, beginning with the function *f*(*x*,
> *y*) = 1, are not trivial. We also note that there are some other
> useful functions computed by the ALU but not listed in the figure.
>
> It may be instructive to describe the thought process that led to the
> design of this particular ALU. First, we made a list of all the
> primitive operations that we wanted our computer to be able to perform
> (right column in figure 2.6). Next, we used backward reasoning to
> figure out how x, y, and out can be manipulated in binary fashion in
> order to carry out the desired operations. These processing
> requirements, along with our objective to keep the ALU logic as simple
> as possible, have led to the design decision to use six control bits,
> each associated with a straightforward binary operation. The
> resultingALU is simple and elegant. And in the hardware business,
> simplicity and elegance imply inexpensive and powerful computer
> systems.

2.3 Implementation

> Our implementation guidelines are intentionally partial, since we want
> you to discover the actual chip architectures yourself. As usual, each
> chip can be implemented in more than one way; the simpler the
> implementation, the better.
>
> Half-Adder An inspection of figure 2.2 reveals that the functions
> sum(*a*, b) and carry(*a*, b) happen to be identical to the standard
> Xor(*a*, b) and And(*a*, b) Boolean functions. Thus, the
> implementation of this adder is straightforward, using previously
> built gates.
>
> Full-Adder A full adder chip can be implemented from two half adder
> chips and one additional simple gate. A direct implementation is also
> possible, without using half-adder chips.
>
> Adder The addition of two signed numbers represented by the 2's
> complement method as two *n*-bit buses can be done bit-wise, from
> right to left, in n steps. In step 0, the least significant pair of
> bits is added, and the carry bit is fed into the addition of the next
> significant pair of bits. The process continues until in step *n*--1
> the most significant pair of bits is added. Note that each step
> involves the addition of three bits. Hence, an *n*-bit adder can be
> implemented by creating an array of n full-adder chips and propagating
> the carry bits up the significance ladder.
>
> Incrementer An *n*-bit incrementer can be implemented trivially from
> an *n*-bit adder. ALU Note that our ALU was carefully planned to
> effect all the desired ALU operations logically, using simple Boolean
> operations. Therefore, the physical implementation of the ALU is
> reduced to implementing these simple Boolean operations, following
> their pseudo-code specifications. Your first step will likely be to
> create a logic circuit that manipulates a 16-bit input according to
> the nx and zx control bits (i.e., the circuit should conditionally
> zero and negate the 16-bit input). This logic can be used to
> manipulate the x and y inputs, as well as the out output. Chips for
> bit-wise And-ing and addition have already been built in this and in
> the previous chapter. Thus, what remains is to build logic that
> chooses between them according to the f control bit. Finally, you will
> need to build logic that integrates all the other chips into the
> overall ALU. (When we say "build logic," we mean "write HDL code").

2.4 Perspective

> The construction of the multi-bit adder presented in this chapter was
> standard, although no attention was paid to efficiency. In fact, our
> suggested adder implementation is rather inefficient, due to the long
> delays incurred while the carry bit propagates from the least
> significant bit pair to the most significant bit pair. This problem
> can be alleviated using logic circuits that effect so-called carry
> look-ahead techniques. Since addition is one of the most prevalent
> operations in any given hardware platform, any such low-level
> improvement can result in dramatic and global performance gains
> throughout the computer.
>
> In any given computer, the overall functionality of the
> hardware/software platform is delivered jointly by the ALU and the
> operating system that runs on top of it. Thus, when designing a new
> computer system, the question of how much functionality the ALU should
> deliver is essentially a cost/performance issue. The general rule is
> that hardware implementations of arithmetic and logical operations are
> usually more costly, but achieve better performance. The design
> trade-off that we have chosen in this book is to specify an ALU
> hardware with a limited functionality and then implement as many
> operations as possible in software. For example, our ALU features
> neither multiplication nor division nor floating point arithmetic. We
> will implement some of these operations (as well as more mathematical
> functions) at the operating systemlevel, described in chapter 12.
>
> Detailed treatments of Boolean arithmetic and ALU design can be found
> in most computer architecture textbooks.

2.5 Project

> Objective Implement all the chips presented in this chapter. The only
> building blocks that you can use are the chips that you will gradually
> build and the chips described in the previous chapter.
>
> Tip When your HDL programs invoke chips that you may have built in the
> previous project, we recommend that you use the built-in versions of
> these chips instead. This will ensure correctness and speed up the
> operation of the hardware simulator. There is a simple way to
> accomplish this convention: Make sure that your project directory
> includes only the .hdl files that belong to the present project.
>
> The remaining instructions for this project are identical to those of
> the project from the previous chapter, except that the last step
> should be replaced with "Build and simulate all the chips specified in
> the projects/02 directory."

3

Sequential Logic

> *It's a poor sort of memory that only works backward.*

*---Lewis Carroll (1832-1898)*

> All the Boolean and arithmetic chips that we built in chapters 1 and 2
> were combinational. Combinational chips compute functions that depend
> solely on combinations of their input values. These relatively simple
> chips provide many important processing functions (like the ALU), but
> they cannot maintain state. Since computers must be able to not only
> compute values but also store and recall values, they must be equipped
> with memory elements that can preserve data over time. These memory
> elements are built from sequential chips.
>
> The implementation of memory elements is an intricate art involving
> synchronization, clocking, and feedback loops. Conveniently, most of
> this complexity can be embedded in the operating logic of very
> low-level sequential gates called flip-flops. Using these flip-flops
> as elementary building blocks, we will specify and build all the
> memory devices employed by typical modern computers, from binary cells
> to registers to memory banks and counters. This effort will complete
> the construction of the chip set needed to build an entire
> computer---a challenge that we take up in the chapter 5.
>
> Following a brief overview of clocks and flip-flops, the Background
> section introduces all the memory chips that we will build on top of
> them. The next two sections describe the chips Specification and
> Implementation, respectively. As usual, all the chips mentioned in the
> chapter can be built and tested using the hardware simulator supplied
> with the book, following the instructions given in the final Project
> section.

3.1 Background

> The act of "remembering something" is inherently time-dependent: You
> remember now what has been committed to memory before. Thus, in order
> to build chips that "remember" information, we must first develop some
> standard means for representing the progression of time.
>
> The Clock In most computers, the passage of time is represented by a
> master clock that delivers a continuous train of alternating signals.
> The exact hardware implementation is usually based on an oscillator
> that alternates continuously between two phases labeled 0-1, low-high,
> tick-tock, etc. The elapsed time between the beginning of a "tick" and
> the end of the subsequent "tock" is called cycle, and each clock cycle
> is taken to model one discrete time unit. The current clock phase
> (*tick* or tock) is represented by a binary signal. Using the
> hardware's circuitry, this signal is simultaneously broadcast to every
> sequential chip throughout the computer platform.
>
> Flip-Flops The most elementary sequential element in the computer is a
> device called a flip-flop, of which there are several variants. In
> this book we use a variant called a data flip-flop, or DFF, whose
> interface consists of a single-bit data input and a single-bit data
> output. In addition, the DFF has a clock input that continuously
> changes according to the master clock's signal. Taken together, the
> data and the clock inputs enable the DFF to implement the time-based
> behavior *out*(*t*) = *in*(*t* - 1), where in and out are the gate's
> input and output values and *t* is the current clock cycle. In other
> words, the DFF simply outputs the input value fromthe previous time
> unit.
>
> As we now show, this elementary behavior can form the basis of all the
> hardware devices that computers use to maintain state, from binary
> cells to registers to arbitrarily large random access memory (RAM)
> units.
>
> Registers A register is a storage device that can "store," or
> "remember," a value over time, implementing the classical storage
> behavior *out*(*t*) = *out*(*t* - 1). A DFF, on the other hand, can
> only output its previous input, namely, *out*(*t*) = *in*(*t* - 1).
> This suggests that a register can be implemented from a DFF by simply
> feeding the output of the latter back into its input, creating the
> device shown in the middle of figure 3.1. Presumably, the output of
> this device at any time *t* will echo its output at time *t* - 1,
> yielding the classical function expected froma storage unit.

![](media/image21.png){width="5.66in" height="1.62in"}

> Figure 3.1 From a DFF to a single-bit register. The small triangle
> represents the clock input. This icon is used to state that the marked
> chip, as well as the overall chip that encapsulates it, is
> time-dependent.
>
> Well, not so. The device shown in the middle of figure 3.1 is invalid.
> First, it is not clear how we'll ever be able to load this device with
> a new data value, since there are no means to tell the DFF when to
> draw its input from the in wire and when from the out wire. More
> generally, the rules of chip design dictate that internal pins must
> have a fan-in of 1, meaning that they can be fed froma single source
> only.
>
> The good thing about this thought experiment is that it leads us to
> the correct and elegant solution shown in the right side of figure
> 3.1. In particular, a natural way to resolve our input ambiguity is to
> introduce a multiplexor into the design. Further, the "select bit" of
> this multiplexor can become the "load bit" of the overall register
> chip: If we want the register to start storing a new value, we can put
> this value in the in input and set the load bit to 1; if we want the
> register to keep storing its internal value until further notice, we
> can set the load bit to 0.
>
> Once we have developed the basic mechanism for remembering a single
> bit over time, we can easily construct arbitrarily wide registers.
> This can be achieved by forming an array of as many single-bit
> registers as needed, creating a register that holds multi-bit values
> (figure 3.2). The basic design parameter of such a register is its
> *width*---the number of bits that it holds---e.g., 16, 32, or 64. The
> multi-bit contents of such registers are typically referred to as
> words.
>
> Memories Once we have the basic ability to represent words, we can
> proceed to build memory banks of arbitrary length. As figure 3.3
> shows, this can be done by stacking together many registers to form a
> Random Access Memory RAM unit. The term random access memory derives
> from the requirement that read/write operations on a RAM should be
> able to access randomly chosen words, with no restrictions on the
> order in which they are accessed. That is to say, we require that any
> word in the memory--- irrespective of its physical location---be
> accessed directly, in equal speed.

![](media/image22.png){width="4.36in" height="1.33in"}

> Figure 3.2 From single-bit to multi-bit registers. A multi-bit
> register of width w can be constructed from an array of w 1-bit chips.
> The operating functions of both chips is exactly the same, except that
> the "=" assignments are single-bit and multi-bit, respectively.

![](media/image25.png){width="2.81in" height="2.86in"}

> Figure 3.3 RAM chip (conceptual). The width and length of the RAM can
> vary.
>
> This requirement can be satisfied as follows. First, we assign each
> word in the n-register RAM a unique address (an integer between 0 to
> *n* - 1), according to which it will be accessed. Second, in addition
> to building an array of n registers, we build a gate logic design
> that, given an address *j*, is capable of selecting the individual
> register whose address is *j*. Note however that the notion of an
> "address" is not an explicit part of the RAM design, since the
> registers are not "marked" with addresses in any physical sense.
> Rather, as we will see later, the chip is equipped with direct access
> logic that implements the notion of addressing using logical means.
>
> In sum, a classical RAM device accepts three inputs: a data input, an
> address input, and a load bit. The address specifies which RAM
> register should be accessed in the current time unit. In the case of a
> read operation (load=0), the RAM's output immediately emits the value
> of the selected register. In the case of a write operation (load=1),
> the selected memory register commits to the input value in the next
> time unit, at which point the RAM's output will start emitting it.
>
> The basic design parameters of a RAM device are its data *width*---the
> width of each one of its words, and its *size*---the number of words
> in the RAM. Modern computers typically employ 32- or 64-bit-wide RAMs
> whose sizes are up to hundreds of millions.
>
> Counters A counter is a sequential chip whose state is an integer
> number that increments every time unit, effecting the function
> *out*(*t*) = *out*(*t* - 1) + c, where c is typically 1. Counters play
> an important role in digital architectures. For example, a typical CPU
> includes a program counter whose output is interpreted as the address
> of the instruction that should be executed next in the current
> program.
>
> A counter chip can be implemented by combining the input/output logic
> of a standard register with the combinatorial logic for adding a
> constant. Typically, the counter will have to be equipped with some
> additional functionality, such as possibilities for resetting the
> count to zero, loading a new counting base, or decrementing instead of
> incrementing.
>
> Time Matters All the chips described so far in this chapter are
> sequential. Simply stated, a sequential chip is a chip that embeds one
> or more DFF gates, either directly or indirectly. Functionally
> speaking, the
>
> DFF gates endow sequential chips with the ability to either maintain
> state (as in memory units) or operate on state (as in counters).
> Technically speaking, this is done by forming feedback loops inside
> the sequential chip (see figure 3.4). In combinational chips, where
> time is neither modeled nor recognized, the introduction of feedback
> loops is problematic: The output would depend on the input, which
> itself would depend on the output, and thus the output would depend on
> itself. On the other hand, there is no difficulty in feeding the
> output of a sequential chip back into itself, since the DFFs introduce
> an inherent time delay: The output at time *t* does not depend on
> itself, but rather on the output at time *t* - 1. This property guards
> against the uncontrolled "data races" that would occur in
> combinational chips with feedback loops.

![](media/image26.png){width="4.07in" height="1.39in"}

> Figure 3.4 Combinational versus sequential logic (in and out stand for
> one or more input and output variables). Sequential chips always
> consist of a layer of DFFs sandwiched between optional combinational
> logic layers.
>
> Recall that the outputs of combinational chips change when their
> inputs change, irrespective of time. In contrast, the inclusion of the
> DFFs in the sequential architecture ensures that their outputs change
> only at the point of transition from one clock cycle to the next, and
> not within the cycle itself. In fact, we allow sequential chips to be
> in unstable states during clock cycles, requiring only that at the
> beginning of the next cycle they output correct values.
>
> This "discretization" of the sequential chips' outputs has an
> important side effect: It can be used to synchronize the overall
> computer architecture. To illustrate, suppose we instruct the
> arithmetic logic unit (ALU) to compute *x* + *y* where *x* is the
> value of a nearby register and *y* is the value of a remote
> RAMregister. Because of various physical constraints (distance,
> resistance, interference, random noise, etc.) the electric signals
> representing *x* and *y* will likely arrive at the ALU at different
> times. However, being a combinational chip, the ALU is insensitive to
> the concept of time---it continuously adds up whichever data values
> happen to lodge in its inputs. Thus, it will take some time before the
> ALU's output stabilizes to the correct *x* + *y* result. Until then,
> the ALU will generate garbage.
>
> How can we overcome this difficulty? Well, since the output of the ALU
> is always routed to some sort of a sequential chip (a register, a RAM
> location, etc.), we don't really care. All we have to do is ensure,
> when we build the computer's clock, that the length of the clock cycle
> will be slightly longer that the time it takes a bit to travel the
> longest distance from one chip in the architecture to another. This
> way, we are guaranteed that by the time the sequential chip updates
> its state (at the beginning of the next clock cycle), the inputs that
> it receives from the ALU will be valid. This, in a nutshell, is the
> trick that synchronizes a set of stand-alone hardware components into
> a well-coordinated system, as we shall see in chapter 5.

3.2 Specification

> This section specifies a hierarchy of sequential chips:
>
> • Data-flip-flops (DFFs)
>
> • Registers (based on DFFs)
>
> • Memory banks (based on registers)
>
> • Counter chips (also based on registers)

3.2.1 Data-Flip-Flop

> The most elementary sequential device that we present---the basic
> component from which all memory elements will be designed---is the
> *data flip-flop* gate. A DFF gate has a single-bit input and a
> single-bit output, as follows:

![](media/image23.png){width="4.92in" height="1.34in"}

> Like Nand gates, DFF gates enter our computer archtecture at a very
> low level. Specifically, all the sequential chips in the computer
> (registers, memory, and counters) are based on numerous DFF gates. All
> these DFFs are connected to the same master clock, forming a huge
> distributed "chorus line." At the beginning of each clock cycle, the
> outputs of all the DFFs in the computer commit to their inputs during
> the previous time unit. At all other times, the DFFs are "latched,"
> meaning that changes in their inputs have no immediate effect on their
> outputs. This conduction operation effects any one of the millions of
> DFF gates that make up the system, about a billion times per second
> (depending on the computer's clock frequency).
>
> Hardware implementations achieve this time dependency by
> simultaneously feeding the master clock signal to all the DFF gates in
> the platform. Hardware simulators emulate the same effect in software.
> As far as the computer architect is concerned, the end result is the
> same: The inclusion of a DFF gate in the design of any chip ensures
> that the overall chip, as well as all the chips up the hardware
> hierarchy that depend on it, will be inherently time-dependent. These
> chips are called sequential, by definition.
>
> The physical implementation of a DFF is an intricate task, and is
> based on connecting several elementary logic gates using feedback
> loops (one classic design is based on Nand gates alone). In this book
> we have chosen to abstract away this complexity, treating DFFs as
> primitive building blocks. Thus, our hardware simulator provides a
> built-in DFF implementation that can be readily used by other chips.

3.2.2 Registers

> A single-bit register, which we call Bit, or binary cell, is designed
> to store a single bit of information (0 or 1). The chip interface
> consists of an input pin that carries a data bit, a load pin that
> enables the cell for writes, and an output pin that emits the current
> state of the cell. The interface diagram and API of a binary cell are
> as follows:

![](media/image24.png){width="4.929998906386702in" height="0.98in"}

> The API of the Register chip is essentially the same, except that the
> input and output pins are designed to handle multi-bit values:

![](media/image30.png){width="5.66in" height="1.11in"}

> The Bit and Register chips have exactly the same read/write behavior:
>
> *Read:* To read the contents of a register, we simply probe its
> output.
>
> *Write:* To write a new data value d into a register, we put d in the
> in input and assert (set to 1) the load input. In the next clock
> cycle, the register commits to the new data value, and its output
> starts emitting d.

3.2.3 Memory

> A direct-access memory unit, also called RAM, is an array of n *w*-bit
> registers, equipped with direct access circuitry. The number of
> registers (*n*) and the width of each register (*w*) are called the
> memory's size and width, respectively. We will now set out to build a
> hierarchy of such memory devices, all 16 bits wide, but with varying
> sizes: RAM8, RAM64, RAM512, RAM4K, and RAM16K units. All these memory
> chips have precisely the same API, and thus we describe themin one
> parametric diagram:

![](media/image31.png){width="5.66in" height="2.68in"}

> *Read:* To read the contents of register number m, we put *m* in the
> address input. The RAM's direct-access logic will select register
> number m, which will then emit its output value to the RAM's output
> pin. This is a combinational operation, independent of the clock.
>
> *Write:* To write a new data value d into register number m, we put
> *m* in the address input, d in the in input, and assert the load input
> bit. This causes the RAM's direct-access logic to select register
> number m, and the load bit to enable it. In the next clock cycle, the
> selected register will commit to the new value (*d*), and the RAM's
> output will start emitting it.

3.2.4 Counter

> Although a *counter* is a stand-alone abstraction in its own right, it
> is convenient to motivate its specification by saying a few words
> about the context in which it is normally used. For example, consider
> a counter chip designed to contain the address of the instruction that
> the computer should fetch and execute next. In most cases, the counter
> has to simply increment itself by 1 in each clock cycle, thus causing
> the computer to fetch the next instruction in the program. In other
> cases, for example, in "jump to execute instruction number *n*," we
> want to be able to set the counter to n, then have it continue its
> default counting behavior with n + 1, n + 2, and so forth. Finally,
> the program's execution can be restarted anytime by resetting the
> counter to 0, assuming that that's the address of the program's first
> instruction. In short, we need a loadable and resettable counter.
>
> With that in mind, the interface of our Counter chip is similar to
> that of a register, except that it has two additional control bits
> labeled reset and inc. When inc=1, the counter increments its state in
> every clock cycle, emitting the value out(t)= out (t-1)+1. If we want
> to reset the counter to 0, we assert the reset bit; if we want to
> initialize it to some other counting base *d*, we put d in the in
> input and assert the load bit. The details are given in the counter
> API, and an example of its operation is depicted in figure 3.5.

3.3 Implementation

> Flip-Flop DFF gates can be implemented from lower-level logic gates
> like those built in chapter 1. However, in this book we treat DFFs as
> primitive gates, and thus they can be used in hardware construction
> projects without worrying about their internal implementation.

![](media/image27.png){width="5.66in" height="5.58in"}

> Figure 3.5 Counter simulation. At time 23 a reset signal is issued,
> causing the counter to emit 0 in the following time unit. The 0
> persists until an inc signal is issued at time 25, causing the counter
> to start incrementing, one time unit later. The counting continues
> until, at time 29, the load bit is asserted. Since the counter's input
> holds the number 527, the counter is reset to that value in the next
> time unit. Since inc is still asserted, the counter continues
> incrementing until time 33, when inc is de-asserted.
>
> 1-Bit Register(Bit) The implementation of this chip was given in
> figure 3.1.
>
> Register The construction of a *w*-bit Register chip from 1-bit
> registers is straightforward. All we have to do is construct an array
> of w Bit gates and feed the register's load input to every one of
> them.
>
> 8-Register Memory (RAM8) An inspection of figure 3.3 may be useful
> here. To implement a RAM8 chip, we line up an array of eight
> registers. Next, we have to build combinational logic that, given a
> certain address value, takes the RAM8's in input and loads it into the
> selected register. In a similar fashion, we have to build
> combinational logic that, given a certain address value, selects the
> right register and pipes its out value to the RAM8's out output. Tip:
> This combinational logic was already implemented in chapter 1.
>
> *n*-Register Memory A memory bank of arbitrary length (a power of 2)
> can be built recursively from smaller memory units, all the way down
> to the single register level. This view is depicted in figure 3.6.
> Focusing on the right-hand side of the figure, we note that a
> 64-register RAM can be built froman array of eight 8-register RAM
> chips. To select a particular register from the RAM64 memory, we use a
> 6-bit address, say xxxyyy. The MSB xxx bits select one of the RAM8
> chips, and the LSB yyy bits select one of the registers within the
> selected RAM8. The RAM64 chip should be equipped with logic circuits
> that effect this hierarchical addressing scheme.
>
> Counter A *w*-bit counter consists of two main elements: a regular
> *w*-bit register, and combinational logic. The combinational logic is
> designed to (a) compute the counting function, and (b) put the counter
> in the right operating mode, as mandated by the values of its three
> control bits. Tip: Most of this logic was already built in chapter 2.

3.4 Perspective

> The cornerstone of all the memory systems described in this chapter is
> the flip-flop---a gate that we treated here as an atomic, or
> primitive, building block. The usual approach in hardware textbooks is
> to construct flip-flops from elementary combinatorial gates (e.g.,
> Nand gates) using appropriate feedback loops. The standard
> construction begins by building a simple (non-clocked) flip-flop that
> is bi-stable, namely, that can be set to be in one of two states. Then
> a clocked flip-flop is obtained by cascading two such simple
> flip-flops, the first being set when the clock ticks and the second
> when the clock tocks. This "master-slave" design endows the overall
> flip-flop with the desired clocked synchronization functionality.

![](media/image29.png){width="4.37in" height="2.75in"}

> Figure 3.6 Gradual construction of memory banks by recursive ascent. A
> *w*-bit register is an array of w binary cells, an 8-register RAM is
> an array of eight *w*-bit registers, a 64-register RAM is an array of
> eight RAM8 chips, and so on. Only three more similar construction
> steps are necessary to build a 16K RAMchip.
>
> These constructions are rather elaborate, requiring an understating of
> delicate issues like the effect of feedback loops on combinatorial
> circuits, as well as the implementation of clock cycles using a two
> phase binary clock signal. In this book we have chosen to abstract
> away these low-level considerations by treating the flip-flop as an
> atomic gate. Readers who wish to explore the internal structure of
> flip-flop gates can find detailed descriptions in most logic design
> and computer architecture textbooks.
>
> In closing, we should mention that memory devices of modern computers
> are not always constructed from standard flip-flops. Instead, modern
> memory chips are usually very carefully optimized, exploiting the
> unique physical properties of the underlying storage technology. Many
> such alternative technologies are available today to computer
> designers; as usual, which technology to use is a cost-performance
> issue.
>
> Aside from these low-level considerations, all the other chip
> constructions in this chapter---the registers and memory chips that
> were built on top of the flip-flop gates---were standard.

3.5 Project

> Objective Build all the chips described in the chapter. The only
> building blocks that you can use are primitive DFF gates, chips that
> you will build on top of them, and chips described in previous
> chapters.
>
> Resources The only tool that you need for this project is the hardware
> simulator supplied with the book. All the chips should be implemented
> in the HDL language specified in appendix A. As usual, for each chip
> we supply a skeletal .hdl program with a missing implementation part,
> a .tst script file that tells the hardware simulator how to test it,
> and a .cmp compare file. Your job is to complete the missing
> implementation parts of the supplied .hdl programs.
>
> Contract When loaded into the hardware simulator, your chip design
> (modified .hdl program), tested on the supplied .tst file, should
> produce the outputs listed in the supplied .cmp file. If that is not
> the case, the simulator will let you know.
>
> Tip The Data Flip-Flop (DFF) gate is considered primitive and thus
> there is no need to build it: When the simulator encounters a DFF gate
> in an HDL program, it automatically invokes the built-in
> tools/builtIn/DFF.hdl implementation.
>
> The Directory Structure of This Project When constructing RAM chips
> from smaller ones, we recommend using built-in versions of the latter.
> Otherwise, the simulator may run very slowly or even out of (real)
> memory space, since large RAM chips contain tens of thousands of
> lower-level chips, and all these chips are kept in memory (as software
> objects) by the simulator. For this reason, we have placed the
> RAM512.hdl, RAM4K.hdl, and RAM16K.hdl programs in a separate
> directory. This way, the recursive descent construction of the RAM4K
> and RAM16K chips stops with the RAM512 chip, whereas the lower-level
> chips fromwhich the latter chip is made are bound to be built-in
> (since the simulator does not find themin this directory).
>
> Steps We recommend proceeding in the following order:
>
> 0\. The hardware simulator needed for this project is available in the
> tools directory of the book's software suite.
>
> 1\. Read appendix A, focusing on sections A.6 and A.7.
>
> 2\. Go through the *hardware simulator tutorial,* focusing on parts IV
> and V.
>
> 3\. Build and simulate all the chips specified in the projects/03
> directory.

4

Machine Language

> *Make everything as simple as possible, but not simpler.*

*---Albert Einstein (1879-1955)*

> A computer can be described constructively, by laying out its hardware
> platform and explaining how it is built from low-level chips. A
> computer can also be described abstractly, by specifying and
> demonstrating its machine language capabilities. And indeed, it is
> convenient to get acquainted with a new computer system by first
> seeing some low-level programs written in its machine language. This
> helps us understand not only how to program the computer to do useful
> things, but also why its hardware was designed in a certain way. With
> that in mind, this chapter focuses on low-level programming in machine
> language. This sets the stage for chapter 5, where we complete the
> construction of a general-purpose computer designed to run machine
> language programs. This computer will be constructed from the chip set
> built in chapters 1-3.
>
> A machine language is an agreed-upon formalism, designed to code
> low-level programs as series of machine instructions. Using these
> instructions, the programmer can command the processor to
> performarithmetic and logic operations, fetch and store values from
> and to the memory, move values from one register to another, test
> Boolean conditions, and so on. As opposed to high-level languages,
> whose basic design goals are generality and power of expression, the
> goal of machine language's design is direct execution in, and total
> control of, a given hardware platform. Of course, generality, power,
> and elegance are still desired, but only to the extent that they
> support the basic requirement of direct execution in hardware.
>
> Machine language is the most profound interface in the overall
> computer enterprise---the fine line where hardware and software meet.
> This is the point where the abstract thoughts of the programmer, as
> manifested in symbolic instructions, are turned into physical
> operations performed in silicon. Thus, machine language can be
> construed as both a programming tool and an integral part of the
> hardware platform. In fact, just as we say that the machine language
> is designed to exploit a given hardware platform, we can say that the
> hardware platform is designed to fetch, interpret, and execute
> instructions written in the given machine language.
>
> The chapter begins with a general introduction to machine language
> programming. Next, we give a detailed specification of the Hack
> machine language, covering both its binary and its symbolic assembly
> versions. The project that ends the chapter engages you in writing a
> couple of machine language programs. This project offers a hands-on
> appreciation of low-level programming and prepares you for building
> the computer itself in the next chapter.
>
> Although most people will never write programs directly in machine
> language, the study of low-level programming is a prerequisite to a
> complete understanding of computer architectures. Also, it is rather
> fascinating to realize how the most sophisticated software systems
> are, at bottom, long series of
>
> elementary instructions, each specifying a very simple and primitive
> operation on the underlying hardware. As usual, this understanding is
> best achieved constructively, by writing some low-level code and
> running it directly on the hardware platform.

4.1 Background

> This chapter is language-oriented. Therefore, we can abstract away
> most of the details of the underlying hardware platform, deferring its
> description to the next chapter. Indeed, to give a general description
> of machine languages, it is sufficient to focus on three main
> abstractions only: a processor, a memory, and a set of registers.

4.1.1 Machines

> A *machine language* can be viewed as an agreed-upon formalism,
> designed to manipulate a memory using a processor and a set of
> registers.
>
> Memory The term*memory* refers loosely to the collection of hardware
> devices that store data and instructions in a computer. From the
> programmer's standpoint, all memories have the same structure: A
> continuous array of cells of some fixed width, also called words or
> locations, each having a unique address. Hence, an individual word
> (representing either a data item or an instruction) is specified by
> supplying its address. In what follows we will refer to such
> individual words using the equivalent notation Memory\[address\],
> RAM\[address\], or M\[address\] for brevity.
>
> Processor The processor, normally called Central Processing Unit or
> CPU, is a device capable of performing a fixed set of elementary
> operations. These typically include arithmetic and logic operations,
> memory access operations, and control (also called branching)
> operations. The operands of these operations are binary values that
> come from registers and selected memory locations. Likewise, the
> results of the operations (the processor's output) can be stored
> either in registers or in selected memory locations.
>
> Registers Memory access is a relatively slow operation, requiring long
> instruction formats (an address may require 32 bits). For this reason,
> most processors are equipped with several registers, each capable of
> holding a single value. Located in the processor's immediate
> proximity, the registers serve as a high speed local memory, allowing
> the processor to manipulate data and instructions quickly. This
> setting enables the programmer to minimize the use of memory access
> commands, thus speeding up the program's execution.

4.1.2 Languages

> A machine language program is a series of coded instructions. For
> example, a typical instruction in a 16- bit computer may be
> 1010001100011001. In order to figure out what this instruction means,
> we have to know the rules of the game, namely, the instruction set of
> the underlying hardware platform. For example, the language may be
> such that each instruction consists of four 4-bit fields: The
> left-most field codes a CPU operation, and the remaining three fields
> represent the operation's operands. Thus the previous command may code
> the operation set R3 to R1 + R9, depending of course on the hardware
> specification and the machine language syntax.
>
> Since binary codes are rather cryptic, machine languages are normally
> specified using both binary codes and symbolic mnemonics (a mnemonic
> is a symbolic label whose name hints at what it stands for---in our
> case hardware elements and binary operations). For example, the
> language designer can decide that the operation code 1010 will be
> represented by the mnemonic add and that the registers of the machine
> will be symbolically referred to using the symbols R0, R1, R2, and so
> forth. Using these conventions, one can specify machine language
> instructions either directly, as 1010001100011001, or symbolically,
> as,
>
> say, ADD R3,R1,R9.
>
> Taking this symbolic abstraction one step further, we can allow
> ourselves not only to read symbolic notation, but to actually write
> programs using symbolic commands rather than binary instructions.
> Next, we can use a text processing program to parse the symbolic
> commands into their underlying fields (mnemonics and operands),
> translate each field into its equivalent binary representation, and
> assemble the resulting codes into binary machine instructions. The
> symbolic notation is called assembly language, or simply assembly, and
> the programthat translates fromassembly to binary is called assembler.
>
> Since different computers vary in terms of CPU operations, number and
> type of registers, and assembly syntax rules, there is a Tower of
> Babel of machine languages, each with its own obscure syntax. Yet
> irrespective of this variety, all machine languages support similar
> sets of generic commands, which we now describe.

4.1.3 Commands

> Arithmetic and Logic Operations Every computer is required to perform
> basic arithmetic operations like addition and subtraction as well as
> basic Boolean operations like bit-wise negation, bit shifting, and so
> forth. Here are some examples, written in typical machine language
> syntax:

![](media/image38.png){width="4.0799989063867015in" height="1.0in"}

> Memory Access Memory access commands fall into two categories. First,
> as we have just seen, arithmetic and logical commands are allowed to
> operate not only on registers, but also on selected memory locations.
> Second, all computers feature explicit load and store commands,
> designed to move data between registers and memory. These memory
> access commands may use several types of addressing *modes*---ways of
> specifying the address of the required memory word. As usual,
> different computers offer different possibilities and different
> notations, but the following three memory access modes are almost
> always supported:
>
> ■ *Direct addressing* The most common way to address the memory is to
> express a specific address or use a symbol that refers to a specific
> address, as follows:

![](media/image36.png){width="3.91in" height="0.65in"}

> ■ *Immediate addressing* This form of addressing is used to load
> constants---namely, load values that appear in the instruction code:
> Instead of treating the numeric field that appears in the instruction
> as an address, we simply load the value of the field itself into the
> register, as follows:

![](media/image37.png){width="1.84in" height="0.1in"}

> ■ *Indirect addressing* In this addressing mode the address of the
> required memory location is not hard coded into the instruction;
> instead, the instruction specifies a memory location that holds the
> required address. This addressing mode is used to handle pointers. For
> example, consider the high-level command x=foo\[j\], where foo is an
> array variable and x and j are integer variables. What is the machine
> language equivalent of this command? Well, when the array foo is
> declared and initialized in the high-level
>
> program, the compiler allocates a memory segment to hold the array
> data and makes the symbol foo refer to the base address of that
> segment.
>
> Now, when the compiler later encounters references to array cells like
> foo\[j\], it translates them as follows. First, note that the jth
> array entry should be physically located in a memory location that is
> at a displacement j from the array's base address (assuming, for
> simplicity, that each array element uses a single word). Hence the
> address corresponding to the expression foo\[j\] can be easily
> calculated by adding the value of j to the value of foo. Thus in the C
> programming language, for example, a command like x=foo\[j\] can be
> also expressed as x=\*(foo+j), where the notation "\*n" stands for
> "the value of Memory\[n\]". When translated into machine language,
> such commands typically generate the following code (depending on the
> assembly language syntax):

![](media/image41.png){width="3.02in" height="0.64in"}

> Flow of Control While programs normally execute in a linear fashion,
> one command after the other, they also include occasional branches to
> locations other than the next command. Branching serves several
> purposes including repetition (jump backward to the beginning of a
> loop), conditional execution (if a Boolean condition is false, jump
> forward to the location after the "if-then" clause), and subroutine
> calling (jump to the first command of some other code segment). In
> order to support these programming constructs, every machine language
> features the means to jump to selected locations in the program, both
> conditionally and unconditionally. In assembly languages, locations in
> the program can also be given symbolic names, using some syntax for
> specifying labels. Figure 4.1 illustrates a typical example.

![](media/image43.png){width="5.66in" height="1.41in"}

> Figure 4.1 High- and low-level branching logic. The syntax of goto
> commands varies from one language to another, but the basic idea is
> the same.
>
> *Unconditional jump commands* like JMP beginWhile specify only the
> address of the target location. *Conditional jump* commands like JNG
> R1,endWhile must also specify a Boolean condition, expressed in some
> way. In some languages the condition is an explicit part of the
> command, while in others it is a by product of executing a previous
> command.
>
> This ends our informal introduction to machine languages and the
> generic operations that they normally support. The next section gives
> a formal description of one specific machine language---the native
> code of the computer that we will build in chapter 5.
