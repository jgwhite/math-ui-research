# Math UI Research

Ongoing research into the following question:

> What is the most elegant UI for writing mathematical formulas on a
> mobile device?

The motivation for answering this question came from my own
experience taking the [“Introduction to Mathematical Thinking”][1]
course on Coursera. I wanted to complete coursework assignments from
the comfort of my iPhone, reasoning that the more convenient I can
make it, the more likely I am to do the work.

I got quite far using Apple Notes and [SciKey][2] but the experience
of writing mathematical formulas (even simple ones) remained
cumbersome, error-prone and frustrating even after weeks of daily
practice.

My next line of investigation is into auto-completion. Would a
specialized keyboard that offered a choice of next-most-likely
mathematical expressions be effective? Would it be annoying to need
to look at the keyboard all the time? Could suggestions provided
closer to the formula being written? How would such a thing work? Can
ML and NLP techniques like word2vec be applied to mathematical
constructions?

![A crude sketch of autocomplete](images/autocomplete-sketch.jpg)

## Query Auto Completion for Math Formula Search

To dig more into the final question above, I began by reading the
paper [“Query Auto Completion for Math Formula Search”][3] by Shaurya
Rohatgi, Wei Zhong, Richard Zanibbi, Jian Wu, and C. Lee Giles. What
follows are my notes from that paper.

> **Abstract**
>
> Query Auto Completion (QAC) is among the most appealing features of
> a web search engine. It helps users formulate queries quickly with
> less effort.

I don’t care about search UIs specifically, but I believe the
underpinnings will be relevant.

> Although there has been much effort in this area for text, to the
> best of our knowledge there is few work [sic] on mathematical formula
> auto completion.

This has been my experience too.

> In this paper, we implement 5 existing QAC methods on mathematical
> formula and evaluate them on the NTCIR-12 MathIR task dataset.

What is the “NTCIR-12 MathIR task dataset”?

Well, [NTCIR-12 MathIR][4] appears to be an academic project concerned with “Mathematical Information Retrieval”. In their words:

> Mathematical Information Retrieval is concerned with finding
> information in documents that include mathematics.

That gives us enough of an understanding for now. Returning to our
main paper…

> We report the efficiency of retrieved results using Mean Reciprocal
> Rank (MRR) and Mean Average Precision (MAP).

Might have to watch some YouTubes to understand these two statistical
analysis methods.

> Our study indicates that the Finite State Transducer outperforms
> other QAC models with a MRR score of 0.642.

“Finite State Transducer” sounds so cool it must be good.

> Keywords: Mathematical Information Retrieval (MIR), Query
> Auto-Complete (QAC)

Reading papers is a good way to learn terms to google for!

> While QAC for text input is a well-studied topic, QAC for math
> formula still remains an open research problem [4, 5].

4 and 5 refer to [Approach0][5] and [Symbolab][6], both extremely
interesting projects for math education.

> A challenge for math QAC is that the input in search boxes is not
> straightforward compared with plain text. Without a graphical
> interface where math equations can be drawn, a LATEX-like syntax is
> usually adopted.

LaTeX truly is the lingua franca of math on the web.

> Another challenge is the data structure used to store math formulae
> to facilitate searching. Similar to an inverted index, the
> prefix-tree is a commonly used data structure to store associations
> between prefix and query completions. These trees provide efficient
> lookups by matching prefixes.

TODO: Learn how to implement prefix tree and related procedures.

> In this study, We use the NTCIR-12 Wikipedia corpus, containing
> 580,068 formulae to evaluate different QAC systems.

I could use this corpus too. I wonder if it can be easily downloaded?

> We define a baseline for Math QAC by evaluating these auto-complete
> strategies using NTCIR-12 MathIR benchmark.

I don’t really know what “baseline” means in this context. I guess
“performance” of known algorithms with no additional optimization?

## Ideas for Further Investigation

- What does Wolfram do?
- What does PocketCAS do?
- Recommendation engines?
  - KNearest

[1]: https://www.coursera.org/learn/mathematical-thinking
[2]: https://apps.apple.com/us/app/scikey-scientific-keyboard/id927863083
[3]: https://arxiv.org/abs/1912.04115
[4]: http://ntcir-math.nii.ac.jp/
[5]: https://approach0.xyz/
[6]: https://www.symbolab.com/
