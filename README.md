# prolog-cfg
The program implements a toy [context-free grammar (CFG)](https://en.wikipedia.org/wiki/Context-free_grammar) parser, that extracts knowledge from text.
The parser understands sentences that follow proper grammar rules of the English language. Also the vocabulary used in the text must be defined in advanced in the knowledge base.

Resources: [1], [2]

# Examples:
You can add facts to the knowledge base:
```
?- say('vaggelis runs fast').
The fact runs(vaggelis,fast) was added to the KB.
true .

?- say('chris gave a program to themis').
The fact gave(chris,program,themis) was added to the KB.
true .
```
And then ask questions:

```
?- ask('who runs fast?').
Answer: vaggelis
true .

?- ask('how does vaggelis run?').
Answer: fast
true .

?- ask('what did chris give to themis?').
Answer: program
true .

?- ask('who gave a program to themis?').
Answer: chris
true .
```

# Import facts from text file:
You can also import fact from a text file. The file must have one sentence per line.
```
?- readfile('Haste makes Waste.txt').
Importing facts... :

had(woman,mongoose)
had(woman,baby)
faithful(mongoose)
went(woman,market)
left(woman,baby,mongoose)
entered(big(cobra),house)
fought(mongoose,cobra)
killed(mongoose,cobra)
returned(woman,house)
laid(mongoose,entrance)
saw(woman,mongoose)
had(mongoose,bloody(mouth))
noticed(woman,had(mongoose,bloody(mouth)))
hasteful(woman)
thought(woman,killed(mongoose,baby))
became(woman,furious)
threw(woman,waterpot,mongoose)
killed(woman,mongoose)
entered(woman,house)
filled(woman,remorse)
alive(baby)
played(baby,cheerfully)
laid(big(cobra),nearby)
dead(big(cobra))
cried(woman)
true .
```

[1]: Striegnitz, Kristina, et al. "Algorithms for Computational Linguistics." (2003).

[2]: Blackburn, Patrick, Johannes Bos, and Kristina Striegnitz. Learn prolog now!. Vol. 7. No. 7. London: College Publications, 2006.
