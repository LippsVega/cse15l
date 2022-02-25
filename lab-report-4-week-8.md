# Testing code snippets on 2 separate implementations!
This lab report tests 3 different snippets of code on 2 separate implementations of `MarkdownParse.java`. The first implementation to be tested on is [mine](https://github.com/LippsVega/markdown-parse/blob/main/MarkdownParseTest.java), and the second is [this one](https://github.com/johnsonli010801/markdown-parse/blob/main/MarkdownParse.java).

***Getting started***

The tests I created can be found [here](https://github.com/LippsVega/markdown-parse/blob/main/MarkdownParseTest.java).

Here they are for reference:

![Image](tests.png)

To run these tests, I placed them all in `MarkdownParseTest.java` on both [my implementation](https://github.com/LippsVega/markdown-parse/blob/main/MarkdownParseTest.java) and the [other's implementation](https://github.com/johnsonli010801/markdown-parse/blob/main/MarkdownParseTest.java). Then I proceeded to run the tests using `make test` to run each repository's Makefile which ran the JUnit tests contained in `MarkdownParsetTest.java`. Here's [my Makefile](https://github.com/LippsVega/markdown-parse/blob/main/Makefile), and here's [the other](https://github.com/johnsonli010801/markdown-parse/blob/main/makefile).

Here's the complete output of running `make test` on my implementation:

![Image](test-output.png)

Now, running `make test` on the other implementation didn't work at first:

![Image](other-test-issue.png)

It turned out, that it was missing an import:

![Image](other-test-fix.png)

After fixing that, it ran:

![Image](other-test-output.png)

As you can see, all 3 tests failed on both implementations! Next we'll examine each code snippet more closely, and theorize as to whether a small or large code change can fix the issue.
<br /><br /><br />

***Code snippet 1***

So let's start with the first code snippet test contained in [snippet1](https://github.com/LippsVega/markdown-parse/blob/main/snippet1.md).

![Image](snippet1.png)

For reference, here's the output of my `JUnit` test:

![Image](snippet1-output.png)

And on the other implementation:

![Image](other-snippet1-output.png)

As you can see, the test didn't pass on either!
<br /><br /><br />

***Code snippet2***

Now let's move on to the code snippet contained in [snippet2](https://github.com/LippsVega/markdown-parse/blob/main/snippet2.md).

![Image](snippet2.png)

Here's my JUnit output:

![Image](snippet2-output.png)

And the other:

![Image](other-snippet2-output.png)

Again, the test didn't pass on either!
<br /><br /><br />

***Code snippet3***

And lastly, the code found in [snippet3](https://github.com/LippsVega/markdown-parse/blob/main/snippet3.md).

![Image](snippet3.png)

My output:

![Image](snippet3-output.png)

Other output:

![Image](other-snippet3-output.png)

Again, the test failed on both implementations.