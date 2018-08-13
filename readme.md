# About Expatpp

Expatpp is both a pattern and C++ code, for writing complex streaming parsers for XML.

The core principles can be adapted to any event-driven parser. Basically, write simple _sub-parsers_ which parse a portion of the tree and cleanly return to their calling context.

## Warning
I have included the original expat folder copied here for historical reasons, as well as early CodeWarrior projects.

Please use modern [expat from github][libexpat]. See [Issue 2]

## History
Expatpp was written when we started saving complex reports to XML and I realised that the typical examples for using the popular [expat] parser encouraged fragile nested switch statements and we were _writing legacy code_.

See the documents [expatpp.html] and [expatppnesting.html] for more discussion on how to use expatpp and how it works.

### Valve
Unknown to me, after I published it on [Sourceforge][SF1] it was picked up by Valve and used as the basis for their parsing in Steam. I found out about it many years later in a Dr Dobbs magazine article on [Server-Side Persistence & Embedded Database Engines][DD]

>(If you are using XML in C++, check out Andy Dent's expatpp wrapper around James Clark's famously fast expat parser [4]. The best feature of this wrapper is the expatppNesting class. This feature lets you define completely separate parser classes for child records and then invoke those parsers to handle the appropriate nested elements of large documents. We have found this feature to be essential to managing complex record hierarchies. In fact, we fixed a minor bug and added some optimizations to expatpp to make this feature even better.

Sorry, as they didn't submit the optimizations back to me I have no idea what happened to them. I'd gratefully accept them if someone wants to send me the code or, even better, submit a PR.

### C++ XML Book
Another user of the library, Fabio Arjona Arciniegas,  wrote a book [C++ XML][CX] SAMS 2001 which has a good example in Ch 3 on event-driven processing, you can see in [Safari Library][SL]

[expat]: https://libexpat.github.io/
[SF1]: https://sourceforge.net/projects/expatpp/
[DD]: http://www.drdobbs.com/server-side-persistence-embedded-databa/184401945
[CX]: http://www.informit.com/articles/article.aspx?p=23277&seqNum=3
[SL]: http://my.safaribooksonline.com/book/programming/cplusplus/073571052x/event-driven-processing/ch03lev1sec2?bookview=search&query=expatpp&reader=html&imagepage=
[Issue 2]: https://github.com/AndyDentFree/expatpp/issues/2
[libexpat]: https://github.com/libexpat/libexpat
[expatpp.html]: ./expatpp.html
[expatppnesting.html]: ./expatppnesting.html