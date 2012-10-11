What is ZED?

ZED is a functional programming language originally designed and implemented by Zelah Hutchinson.

Who can use ZED?

Anyone can use ZED for any purpose whatsoever. Attribution is appreciated but not required.

Is ZED copyrighted?

My contributions to documents on this main branch are copyrighted © Zelah Hutchinson. I grant everyone the perpetual and non-exclusive right to copy and use this content. Read STATEMENT and UNLICENSE for more details.

What are the major design goals of this programming language?

Simplicity, efficiency, easy commenting, and easy debugging.

What is meant by "simplicity"?

Syntax in ZED is minimal, and the resulting programs are highly uniform, making programs easier to write and, also, easier to read.

What is meant by "efficiency"?

Programs written in ZED should be at least as performant as well written programs in Racket/Scheme. With planned additions, such as support for automatic parallelization and genetic programming, we hope to make it very much more performant than Racket/Scheme.

What is meant by "easy commenting"?

ZED will simplify commenting by making it easy to comment on individual branches of your program's conditional logic.

What is meant by "easy debugging"?

ZED will eventually provide an interpreted mode for the purpose of generating program traces. A program trace will be a hypertext document generated, at once, by tracing the execution of a ZED program. This document will show the minute details of program execution but will have forward references embedded as hypertext links so that a click of the mouse will skip past execution detail when it is not needed. A back button will allow the programmer to "travel back in time" to see an earlier part of the program trace. Debugging will occur most naturally by skipping most of the execution detail at the start of debugging and only refining the search when that becomes necessary. When the programmer first notices an error, he or she will "travel back in time" to before the error occurred and continue the search in finer detail.

Can you show me how this debugging might work in practice?

Sure! Here are two function definitions and a very short execution trace:

----------------------------------------

(square) number   
3   
(always)   
(*) number number   

(abs) number   
-5   
(<) number 0   
(-) 0 number   

(abs) number   
5   
(always)   
number   

----------------------------------------

(square) (abs) -3   
(square) (-) 0 -3   
(square) 3   
(*) 3 3   
9   

----------------------------------------

Clicking with the mouse on any of the application functions (application functions are surrounded by parentheses) will skip forward to the correct line of the program trace. For example, clicking on "(abs)", above, will take you to the third line in the program trace where "(abs) -3" has been replaced by the result of calling "(abs) -3". Any application function may be clicked on in this way.