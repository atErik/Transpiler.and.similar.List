 # Transpiler.And.Similar.List

List Of Transpilers, TransCompilers, Decompilers, etc [source-code to source-code converter][1], &amp; similar &amp; related tools/apps.  
  
( History : I created a [question](https://stackoverflow.com/questions/64180191/) in StackOverflow(SO), where i have initially asked Which transpiler can convert `"Go"` source-code into `"C"` source-code, and then i had to change question & ask : Which transpiler (out of four specific transpiler) can convert from `Go` to `C/C++` and can still keep (almost all) high-level algorithms & structures used in source-code , fairly accurately same/intact in output source-code . And this project/data borned from that research, so later when StackOverflow's `"PRO-GOOGLE"` & `"PRO-GO"` do-evil mods ganged-up on my Quesiton+Answer & deleted it (vote to undelete [here](https://stackoverflow.com/users/recently-deleted-questions/3553808)) , i had to publish from this github project, & improve it here. )

<a name="License"></a>
<div width="100%"><b>LICENSE of this project "Transpiler.And.Similar.List":</b><br />
 "Transpiler.And.Similar.List" project pages, info, data, file, etc
 are <b>Released with following combined LICENSE(s) + 
 RESTRICTIONs + PERMISSIONs:</b><dl>
 <dd> 
  <b class="b">•</b> Do Not Use This To Kill/Harm/Violate (or Steal-from)(Any) Human/Community,Earth,etc.<br />
  <b class="b">•</b> Do Not Use Any Data/File From This Project Into Military/Offense/Attack/Killing Forces,etc.<br />
  <b class="b">•</b> Do Not Use Any Data/File From This Project To File LawSuit Against Someone Who Uses It/Derivative To Save/Protect Life,Liberty,Privacy,Community,Earth,etc.<br />
  <b class="b">•</b> GNU Affero General Public License Version 3 
  (<a href="https://www.gnu.org/licenses/agpl-3.0.html" target="_blank">AGPL v3</a>).<br />
  <b class="b">•</b> Copyright <b>©</b> 2020 atErik (Erik T. Ashfolk) (&lt;at&#69;rik＠Ö&#965;ťĹö&#333;ķ·ċ&#333;m;
  at&#69;rïķ＠&#65;śh&#70;ölķ·ć&#333;m&gt;<br />
  &#160;&#160;&#160;&#160;Do Not Copy Eml-Adrs, Type In 
  English/<a href="https://en.Wikipedia.org/wiki/Basic_Latin_%28Unicode_block%29" target="_blank">basic-Latin</a> 
  Char, No-Permission is Given To Solicit)&#46;<br />
  &#160;&#160;&#160;&#160;All rights reserved.<br />
  <br />
  <br />
  "Transpiler.And.Similar.List" : List of transpilers/transcompilers, etc.<br />
  Copyright (C) 2020  atErik (Erik T. Ashfolk).
  
  This program is free software: you can redistribute it and/or modify<br />
  it under the terms of the GNU Affero General Public License as<br />
  published by the Free Software Foundation, either version 3 of the<br />
  License, or (at your option) any later version.
  
  This program is distributed in the hope that it will be useful,<br />
  but WITHOUT ANY WARRANTY; without even the implied warranty of<br />
  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.&#160; See the<br />
  GNU Affero General Public License for more details.<br />
  
  You should have received a copy of the GNU Affero General Public License<br />
  along with this program.&#160; If not, see &lt;https://www.gnu.org/licenses/&gt;.<br />
  &lt;https://www.gnu.org/licenses/agpl-3.0.html&gt;<br />
  <br />
  <br />
  <br />
  <b class="b">•</b> (All other trademarks, etc cited here are the property 
  of their respective owners&#46;)<br />
  <b class="b">•</b> (All other copyright items cited here are the copyright 
  of their respective author/creator&#46;)<br />
  <br />
  <br />
  <br />
  <h3>IF YOU DO NOT AGREE WITH ABOVE LICENSE RESTRICTIONS & PERMISSIONS , THEN YOU CANNOT USE ANY DATA/SERVICE FROM THIS PROJECT OR WEB-PAGES , PRESS BACK BUTTON IN YOUR WEB-BROWSER , AND COMPLETELY STOP USING/VIEWING THIS WEBPAGE/DATA ( AND ANY OTHER WEBPAGES/DATA UNDER IT ).</h3>
  </dd>
 </dl>
</div>
<br />
<br />
<br />
<br />
<br />
<br />
&#160;&#160;&#160;&#160;<b>CPL</b>&#160;=&#160;Computer&#160;Programming&#160;Language.<br />
<br />
<br />
Which TRANSPILER Can Convert/**[Transpile][1]**/Transcompile/Transform Input Source-Code (`"Go"` or Any/✱ other CPL) Into Output Source-Code (`"C"` or Any/✱ other CPL) <b>?</b><br />
Which TRANSPILER Can Keep High-Level Algorithms / Structures Used In Source-Code (here: `"Go"` or Any/✱ other CPL) , Fairly Accurately Intact/Same In Generated / Output / Destination / Target Source-Code (here: `"C"` or Any/✱ other CPL), As Much As Possible <b>?</b>  
  
( abbreviations : `lang` = language &#124; . `C++` = `Cpp` = `C-plus-plus` . `Go` = `Golang` )  
  
TRANSPILE : source-code to source-code conversion , where high-level structures, algorithms, etc (of input code) are kept same or accurate during conversion process, (in output code) . Sometime extra codes are needed in output code, to function it same as input code.  
  
<h4>( YOU MAY GOTO LIST OF ALL TRANSPILERS DIRECTLY FROM <a href="https://github.com/atErik/Transpiler.and.similar.List/blob/main/Transpiler.And.Similar.List.md">HERE</a> )</h4>
  
For example, when input code (`"Go"` language code) contains:
```Go
// "Go" based source-code:
var n int
type Node struct {
    left, right *Node
    data    interface{}
}

func twice(f func(int) int, v int) int {
    return f(f(v))
}

func main() {
    f := func(v int) int {
        return v + 3
    }
    twice(f, 7) // returns 13
}
```

then, this `"Go"`-to-`"C"` conversion/transpilation<sup>[1][2]</sup> process need to convert & generate/output below `"C"` language code:
```C
// Converted "C"-lang based source-code
#include <stdio.h>

typedef int (*int_func_int) (int);

int n;
struct Node {
    struct Node *left, *right;
    void    *data;
};

int add3(int x) {
    return x + 3;
}

int twice(int_func_int f, int v) {
    return f(f(v));
}

int main() {
    printf("%d\n", twice(add3, 7));
    return 0;
}
```
when `"Go"`-to-`"C++"` (`C++14`) transpilation is done, then output should be:
```C++
// Converted "C++"(C++14)-lang based source-code
#include <iostream>

int n;
struct Node {
    struct Node *left, *right;
    void    *data;
};  

auto twice = [](auto f, int v)
{
    return f(f(v));
};

auto f = [](int i)
{
    return i + 3;
};

int main()
{
    std::cout << twice(f, 7) << std::endl;
}
```
when `"Go"`-to-`"C++"` (`C++11`) transpilation is done, then output should be:
```C++
// Converted "C++"(C++11)-lang based source-code
#include <iostream>
#include <functional>

int n;
struct Node {
    struct Node *left, *right;
    void    *data;
};  

auto twice = [](const std::function<int(int)>& f, int v)
{
    return f(f(v));
};

auto f = [](int i)
{
    return i + 3;
};

int main()
{
    std::cout << twice(f, 7) << std::endl;
}
```
An actual EXAMPLE of "C"-to-"Go" CODE is shown [here][3] <sup>[2][4], [3][5]</sup>, but we want opposite of "C"-to-"Go" : so we want "Go"-to-"C" (go-to-c / go2c).  
<br />

FEW&#160; POINTS:  
`•` Let us assume, you're more familiar with `"C"` & `"C++"` more, than `"Go"`.  
`•` In computer programming language, let us assume, `C`/`C++`/`Assembly` are your native computer language (these you have learned in School/University, & then practiced).  
`•` So it should be okay to convert `non-C` & `non-C++` language `"Go"` aka: `"Golang"` , into `"C"` or `"C++"`, to understand better.  
`•` Learning a second computer language (for example: `"Go"`) (or lets say: French) & hoping to become expert within 7-days or so like your native computer language (`"C"` or `"C++"`) (or lets say: English) , is not only a plain wrong expectation , if any fool suggested such then that i consider a wrong advice , because this will NOT take you to a LEVEL where you can begin to contribute in real open-source projects . But one of the right advice can be this : Start to learn+practice the second computer language in parallel (in a different, easy & forked project), as it will take long time & effort to reach expert level in that second computer language.  
`•` So, we do not want to keep any input (`"Go"`) source-code remaining in output (`C/C++`) source-code . ( But some `Assembly` is fine in output if you're okay with `Assembly` language ) . And also be aware of that ['Go' Has Problems][6] <sup>[2][7], [3][8]</sup> , [Security Vulnerabilities of 'Golang'][9] <sup>[2][10], [3][11], [4][12], [5][13]</sup>, etc are just few reasons to move away from `"Go"`, and use other language . You have full freedom & right to choose what you want to do.  
`•` Let us assume, Necessary Features or Functionality that i or you need to add, those are developed & optimized for `C/C++`, not-available in `"Go"`.  
`•` Programs that i or you want to TRANSPILE/CONVERT from `Go-to-C` or from `Go-to-C++`, that type of programs should be developed with `C/C++`, as that type of programs work better with `C`, and even more better with `C++`.  
`•` Recreating complex & large software/systems with years of development from scratch with another (second) computer language , is not-only hard , that is also not-suggested<sup>[1][14]</sup> (not-adviced) , So transcompilation steps are helpful to give a head-start by converting easier source-code . Transcompilation process always requires human developer based manual code conversion, as none of the Transpilers are perfect or supports ALL aspects of source/input language or different programming styles, codes, libraries, etc that are used in real practical projects/languages . Small project(s) or new project can be built from scratch, and even by using a second computer language.  
`•` If source code is from open-source project , then Human/manual and/or automated transpilation of output source-code should also be released as open-source , same as input source-code . In that way, another group of developers skilled at output language (`C/C++`) can also participate in open-source development, to help all users & people.  
<br />  
<br />

<h4>( YOU MAY GOTO LIST OF ALL TRANSPILERS DIRECTLY FROM <a href="https://github.com/atErik/Transpiler.and.similar.List/blob/main/Transpiler.And.Similar.List.md">HERE</a> )</h4>
<br />

SOLUTIONS&#160; FOR&#160; `Go`-To-`C`<b>:</b>  
Currently, i SPECIFICALLY have these four solutions/choices to use:  
`•` Solution A or #1 : "[go2cs][15]", "[CSharp.lua][16]", "[lua2c][17]".  
`•` Solution B or #2 : "[go2cs][15]", "[Blazor][18]", "[wasm2c][19]".  
`•` Solution C or #3 : "[gomoku][20]", "[Cfront][21]" or "[Comeau C&#47;C&#43;&#43;][22]".  
`•` Solution D or #4 : "[go2c][23]".  
<br />
<br />
WHICH&#160; `Go`-To-`C` SOLUTION&#160; (out of above solutions) IS BETTER <b>?</b>  
( better at keeping high-level algorithms/structures,etc fairly or accurately same in output source-code )  
is there (similar) better transpiler solution, among the links that i have shown ?  
Along with `Go-to-C` conversion , if you can then please show `Go-to-C++` conversion.  
Above four (transpiler-set) solutions have what Pros/Cons ?  
<br />
<br />

SOLUTION&#160; ANALYSIS&#160; &amp;&#160; PROs/CONs&#160; &amp;&#160; PROBLEM(s)<b>:</b>

SOLUTION A or &#35;1<b>:</b>
* steps: we are attempting to do these:  
  `"Go"`--&gt;`"C#"`--&gt;`"Lua"`--&gt;`"C"`
  * (**A**-1) use this "[go2cs][15]" transpiler to convert `"Go"`/`"Golang"` source-code into `"C#"` (C-sharp) based code.
    * (place your GoProject here: `D:\Dev\GoProject\`)  
    (create & go inside this folder: `D:\Dev\Go-to-CS-GoProject\`)  
    Convert a single Go file: `go2cs -l D:\\Dev\\GoProject\\src\\Main.go`  
    Convert entire Go project: `go2cs D:\\Dev\\GoProject`  
    Convert Go Standard Library: `go2cs -s -r D:\\Dev\\GoProject\\src\\`
  * (**A**-2) convert that `"C#"` source-code into `"Lua"` code with this "[CSharp.lua][16]" transpiler.
    * D:&#92;&gt; `dotnet CSharp.Lua.Launcher.dll -h`  
    Usage: CSharp.lua [-s srcfolder] [-d dstfolder]  
    Arguments  
    `-s` : can be a directory where all cs files will be compiled, or a list of files, using ';' or ',' to separate  
    `-d` : destination directory, will put the out lua files  
    Options  
    `-h` : show the help message and exit  
    ...  
    (source folder should be: `D:\Dev\Go-to-CS-GoProject\`)  
    (create & specify destination folder: `D:\Dev\CS-to-Lua-GoProject\`)
  * (**A**-3) convert that `"Lua"` source-code into `"C"` code with this "[lua2c][17]" transpiler.
    * (create & go into a folder 1st like this: `D:\Dev\Lua-to-C-GoProject\` or specify previous as destination folder in next command)  
    `lua` to `C` cmd: `lua lua2c.lua D:\Dev\CS-to-Lua-GoProject\Main.lua`
* in this solution-"A", a developer have to be familiar with `"C#"` & `"Lua"`, and you can also clearly see that transpile/conversion occurred 3-TIMES : `"Go"`--&gt;`"C#"`--&gt;`"Lua"`--&gt;`"C"`, which is not-very-good . Conversion done by `go2cs` is high-quality(HQ), but other tools in chain are not that much HQ, so overall conversion quality is not good.  
  As dev/user also need to know middle language(s), ( and i'm not very familiar with `C#` or `Lua` ).  
  In solution-"A", atleast final destination `"C"` code will still have high-level structures fairly intact that were used in initial `"Go"` source-code.

SOLUTION B or &#35;2<b>:</b>
* steps: in this solution we attempt to do these:  
  `"Go"`--&gt;`"C#"`--&gt;`"WebAssembly"`--&gt;`"C"`. (also see alternative Solution-E)
  * (**B**-1) use this "[go2cs][15]" transpiler to convert `"Go"`/`"Golang"` source-code into `"C#"` (C-sharp) based code.
    * see sub-section inside above Solution-A-1.
  * (**B**-2) convert that `"C#"` source-code into `"WebAssembly"` code with this "[Blazor][18]" transpiler.
  * (**B**-3) convert that `"WebAssembly"` source-code into `"C"` code with this "[wasm2c][19]" transpiler.
* in this solution-"B" also doing conversion 3-TIMES : `"Go"`--&gt;`"C#"`--&gt;`"WebAssembly"`--&gt;`"C"`, but these steps will completely breakdown all high-level structures & meaningful programming codes into large amount of micro (machine level) elements, etc,  
  Thus its depriving me or developer from chance to improve source-code further or improve quickly.  
  ( btw, in my case, i'm familiar with `"Assembly"` & `"C"` ).

SOLUTION C or &#35;3<b>:</b>
* (**C**-1) use this "[gomoku][20]" transpiler to convert `"Go"`/`"Golang"` source-code into `"C++"` based code.  
  (**C**-2) convert that `"C++"` source-code into `"C"` code with (any one of these) transpilers like these: [Cfront][21], [Comeau C&#47;C&#43;&#43;][22], also see these SO(StackOverflow) pages for more info: [1][24], [2][25], [3][26], [4][27].  
  Compiler tools can also convert `C++`-to-`C`:  
  &#160;&#160;`clang -c CPPtoC.cpp -o CPPtoC.bc -emit-llvm`  
  &#160;&#160;`clang -march=c CPPtoC.bc -o CPPtoC.c`  
  &#160;&#160;&#160;or  
  &#160;&#160;`llvm-g++ -c CPPtoC.cp -o CPPtoC.bc -emit-llvm`  
  &#160;&#160;`llc -march=c CPPtoC.bc -o CPPtoC.c`
* in this solution-"C" steps, transpile/conversion occurred 2-TIMES : `"Go"`--&gt;`"C++"`--&gt;`"C"`, and in both case destination languages are closer language, so final `"C"` code will still have high-level structures fairly intact that were used in initial `"Go"` source-code, which can be improved by a dev/user.

SOLUTION D or &#35;4<b>:</b>
* (**D**-1) use this "[go2c][23]"(mukadr) transpiler to convert `"Go"` source-code into `"C"` based code, though it can transpile `"Go"`-to-`"C"` by itself, but at this moment (when this was posted here), sadly this supports only a subset components of Go.  
These transpilers can also be used for `Go2C` conversion : [goc][28], [go-transpiler][29](mewbak), etc, but these also only supports subset of `"Go"` language, at this moment (when this was posted here).
* in this solution-"D", transpiler can convert 'Go' into 'C' directly in one-time w/o using any other intermediate transpilers : `Go`--&gt;`"C"` , but does not support conversion of all components of `Go`-language.

EXTRA - SOLUTIONS<b>:</b>

SOLUTION E or &#35;5<b>:</b>  
* steps: this Solution-E is alternative of above Solution-B.
  * (**E**-1) use these commands to convert `"Go"` into `"Go"-"Assembly"`, `"go2goasm"`, output of `"Go"`-tool is a Google/Golang flavored `"Assembly"`, its not completely Standard/regular `Assembly`, but close to it . Commands:  
  `go tool compile -S Main.go`  
  &#160;or  
  `go build -gcflags -S Main.go`  
  * (**E**-2) use [Boomerang][30] decompiler<sup>[2][31], [3][32]</sup> on `Go-"Assembly"` source-code file, and manually change/convert incompatible portions into general `Assembly` until it can do Asm-to-C . Or use [asm2c][33],etc transpiler, that can convert `Assembly`(`Asm`) into `C` (`Asm`-to-`C`) . Other solutions are mentioned [here][34], [2][35], [3][36].
* Conversion happens 2-TIMES : `"Go"`-&gt;`"Assembly"`-&gt;`"C"` . Because of "go2asm" conversion, allmost all higher-level structures in `"Go"` will go away from `"Assembly"` (low-level language) . So, after `Assembly` to `C` conversion , `C` source-code will not-include any high-level structures of "Go" source, new high-level `C` will be something different, though functioning same way.  
  Usually this solution is faster.

SOLUTION F or &#35;6<b>:</b>  
* steps:
  * (**F**-1) use "go2cs" to convert `"Go"` into `"C#"`(`CSharp`).  
  see sub-section under Solution A-1, for usage.
  * (**F**-2) use "[hurley][37]" to convert `C#` into `C`.
* Conversion happens 2-TIMES : `"Go"`-&gt;`"C#"`-&gt;`"C"` . Many higher-level structures in `"Go"` will remain in final output . The "go2cs" does HQ conversion, but next step not that much, need more improvements.

<s>&#160;SOLUTION G or &#35;7<b>:</b>&#160;
* &#160;(**G**-1) "[go-transpiler][38]". According to it's dev, though original goal was to make a transpiler but now its a parser that checks if code is valid as per Golang grammar.&#160;</s>

OTHER:
* This "[esp32-transpiler][39]" can convert 'Go' into 'C' for Arduino (an embedded system), but only small subset of 'Go' lang spec is supported.  
<br />

CONCLUSION OF `"Go"`-to-`"C"` FOUR SOLUTIONS<b>:</b>
* at this point:  
  So, solution-"A" (go2cs-&gt;CSharp.lua-&gt;lu2c) is better than solution-"B" (go2cs-&gt;Blazor-&gt;wasm2c).  
  solution-"E" (go2asm-&gt;asm2c) is obviously better than solution-"B" (go2cs-&gt;Blazor-&gt;wasm2c).  
  solution-"F" (go2cs-&gt;hurley) is better than solution-"A" (go2cs-&gt;CSharp.lua-&gt;lu2c).  
  solution-"C" (gomoku-&gt;cfront) is better than solution-"A" (go2cs-&gt;CSharp.lua-&gt;lu2c).  
  solution-"F" (go2cs-&gt;hurley) is better than solution-"C" (gomoku-&gtcfront;).
  solution-"C" (gomoku-&gt;cfront) is better than solution-"D" (go2c/goc/go-transpiler).  
  So, solution-"F" (go2cs-&gt;hurley) is best `"Go"`-to-`"C"` transpiler-set,  
  at this point, among previous choices (when this message was posted here).  
  *Note: none of these transpilers support all components of "input" language, but their developers are improving them . So, often check out supported component list, which is shown in their website.*
<br />

ANOTHER&#8239;/&#8239;ALTERNATIVE OPTION & SOLUTION `Go`-To-`C++`<b>:</b>  
As other developers have pointed out, in some cases `C++` (based compiled program) can often be much better & faster than `C` ones, so i'm also displaying these below few options to convert/transpile `Go` directly into `C++` while keeping higher-level structures fairly intact, & output `C++` code is also easier to improve as/when necessary:
* ALT-SOLUTION A or &#35;1<b>:</b> use [gomoku][20] for `Go` to `C++`.  
  ALT-SOLUTION B or &#35;2<b>:</b> use [go2cpp][40] for `Go` to `C++20`/`C++17`.  
  ALT-SOLUTION C or &#35;3<b>:</b> use [GoLite Transpiler][41] for `GoLite` (subset of `Go`) to `C++` . GoLite Transp supports only subset of `Go`.  
  ALT-SOLUTION D or &#35;4<b>:</b> use [go2cs][15] for `Go` to `C#`(C-Sharp), then use any of these: [cs2cpp][42], [Alter-Native][43], [CoreRT][44], [OneLang][45], [Ranger][46], etc to convert `C#` into `C++`.  
  ALT-SOLUTION E or &#35;5<b>:</b> use [go-transpiler][47](Theodus) for `Go` to `C++`.
* WHICH&#160; `Go`-To-`C` SOLUTION&#160; (out of above solutions) IS BETTER <b>?</b>  
( better at keeping high-level algorithms/structures,etc fairly or accurately same in output source-code )
* CONCLUSION ON `"Go"`-to-`"C++"`<b>:</b>  
  Alt-Solution-A (gomoku) is obviously slightly better than Alt-Solution-B (go2cpp),  
  and Alt-Solution-B (go2cpp) is much better than Alt-Solution-C (GoLite Transp),  
  and Alt-Solution-D (go2cs+cs2cpp) is also much better than Alt-Solution-C (GoLite Transp).  
  in Alt-Soln-D, though `go2cs` conversion quality is higher, but next stage `cs2cpp` tools are not.  
  and Alt-Solution-D (go2cs+cs2cpp) is better than Alt-Solution-B (go2cpp).  
  So Alt-Solution-A (gomoku) is best at this point, among these available transpiler choices, (when this message was posted here).  
<br />
<br />


abbreviations : `aka` = also known as

TRANSPILER<sup>[1][1]</sup><b>:</b>  
Transpiler/Transcompiler internally contains primarily three major components<b>:</b>
* 1of3: Parser : it is used to create AST<sup>[1][48]</sup> from input/source code, by using Lexical<sup>[1][49]</sup> analysis and Syntax<sup>[1][50]</sup> analysis.  
  • [Comparison of Parser-Generators and Lexer-Generators][51].
* 2of3: Transformation : with one or more steps, input code's AST will be converted into output/target code's AST . Uses semantic<sup>[1][52]</sup> analysis, Intermediate Representation (IR)<sup>[1][53]</sup> generation . IR is aka: Intermediate Language (IL)<sup>[1][54]</sup>.
* 3of3: Generator : output AST is used to generate output/target language code.
* Transpiler can/may use MetaProgramming<sup>[1][55]</sup>, NLP(Natural Language Processing)<sup>[1][56]</sup>, Finite-state Automata<sup>[1][57], [2][58]</sup>, Lexical Analysis<sup>[1][49]</sup>, Syntax/AST Analysis<sup>[1][48]</sup>, Parser<sup>[1][59], [2][60]</sup>, etc<sup>[1][51]</sup>, etc, to convert source-code of one CLP(computer programming language) into source-code of another CLP.
* Notes/References:  
  `•` [Transpiler][61].  
  `•` [How to write a transpiler][14], [2][62].  
  `•` [Transpiling between any languages][63].  
<br />
<br />

OTHER&#160; INFORMATION&#160; &&#160; REFERENCES<b>:</b>  

**Go2C** Conversion : My objective is here is to share simple steps/directions on converting / transpiling `Go`-language source-code into `C`-language (or `C++`) source-code, with one of the mentioned (in above) possible set of TRANSPILER solutions, that can still keep high-level algorithms / structures, etc used in initial/input `Go` source-code , fairly or accurately same/intact in final destination / output `C` (or `C++`) source-code.  
Then we can compile `C/C++` code into binary machine code when necessary, to run it faster.  
So after `Go-to-C` or `Go-to-C++` source-code conversion , it will be possible to change source-code (to add required necessary feature or functionality) & improve `C` (or `C++`) source-code.  
<br />
<br />

I have added data/info from accredited computer COMPETITION, BENCHMARKS, etc to prove which is better & which is not.  
And, ANYONE/USER/people have full freedom+right+choice to choose what he/she wants, and also have full freedom+right to convert one language into another.<sup>[1][64], [2][65], [3][66], [4][67], [5][68]</sup>  
<br />
<br />

abbreviations : `CPL` = Computer Programming Language

CAPABILITIES<b>:</b>  
Here are some results of a yearly competition on CPL, based on CAPABILITIES of CPL and tools<b>:</b>
* https://en.wikipedia.org/wiki/ICFP_Programming_Contest  
  In this competition, 1st prize means: "it is the programming tool of choice for discriminating hackers" . 2nd prize means: "it is a fine programming tool for many applications" . 3rd prize means: "it is also not too shabby" . And "Lightning" prize means: "it is very suitable for rapid prototyping".  
  In 2019:&#160;&#160; 1st: `Rust` &#124; 2nd: `C++` &#124; 3rd: - &#124; Lightning: `C++` & `Haskell`.  
  In 2018:&#160;&#160; 1st: `Rust` &#124; 2nd: `C++`, `Python`, `Ruby`, `JavaScript`, `bash`, `SQL` &#124; 3rd: - &#124; Lightning: `OCaml`.
* RESULT <b>:</b> So from above section you can see, As of 2018 `Go`(Golang) HAS NOT ACHIEVED ANY PRIZE in any category . In 2002 `C` achieved 2nd prize . And in 2018 `C++` achieved 2nd prize again.
<br />

FAST or SLOW<b>:</b>  
Various benchmarks: [1][69], [2][70], [3][71], [4][72], [5][73], [6][74], [7][75].
* Please see these Q+A on CS.StackExchange site<b>:</b>  
  [What Determines the Speed of a Programming-language?][76]  
  [Why are some programming languages “faster” or “slower” than others?][77]  
  `CS` = Computer-Science.
* Benchmarks from "[The Computer Language Benchmarks Game][78]" (CLBG) are based on <b>:</b> Overall user runtime, Peak memory allocation, Gzip'ped size of the solution's source code, Sum of total CPU time over all threads, Individual CPU utilization . BE-AWARE <b>:</b> many notable developers pointed out results are not perfect benchmarks, due to: various programming techniques, configuration issues, weak programming, etc that exist in various software & hardware tools & human expertise.  
  In this CLBG [page][79] you can see performance chart on compiled program of different computer programming language (CPL) . I'm displaying names of selected few (not all) CPL in below from "Program Busy Time / Least Busy" category chart of July-1, 2020, in the ORDER of their placement shown there , so, better performing one is mentioned earlier in left-side , & less-better are mentioned later or after that <b>:</b> `C++` (`g++`), `C` (`gcc`), `Rust`, `Julia`, `Intel Fortran`, `Ada 2012`, `C# .NET Core`, `Free Pascal`, `F# .Net Core`, `Go`, `Java`, etc.
* RESULT <b>:</b> So you can see in above section, there is a huge performance gap between `Go` & `C` . The `"Go"`(Golang) is ~2 to ~5.25 TIMES SLOWER THAN `"C"` . `"Go"/"Golang"` is ~2.25 to ~7 TIMES SLOWER THAN `"C++"`.  
<br />

COMPARISONS<b>:</b>  
Comparison of Programming Language's ...  
`•` [Basic instructions][80].  
`•` [Syntax][81].  
`•` [Higher-order function][82].  
`•` [Operators][83].  
`•` [Object-Oriented Programming(OOP)][84].  
`•` [OOP Constructor][85].  
`•` [Exception handling][86].  
<br />
<br />
<br />
abbreviation : `CPL` = Computer Programming Language.

HOW TO DETERMINE WHICH ONE IS BETTER THAN ANOTHER<b>:</b>

SUPPORTED COMMANDS/INSTRUCTIONS, FUNCTIONS, etc LIST Provided By TRANSPILER<b>:</b>  
Transpiler software primary-dev or project's website displays list of supported commands/instructions, functions, etc language components . Their primary developer(s) & other developers are developing+improving those transpiler-projects when they can . So, often check out those lists, & COMPARE, to find out which one is better.  
Then use same source file and convert with multiple transpilers, and check output source-code file, to find out which transpiler able to do conversion completely or which portions are skipped or incorrect.  
Which one is BEST, that will always change or most-likely be different at different time.  
(and "BEST" is connected with "Category", so based on that there are different types of BEST, and at different time)
<br />

PRE & POST STEPS<b>:</b>  
Most of the time, certain code/strings need to be modified/changed, & prepared in each initial source-code (here `"Go"`) files (with [PreProcessor][87] type of software), before the primary transpiler can be used.  
And, often you have to change some specific style of code/string in each output (here `"C"` or `"C++"`) file , to fix or change something that was not automatically generated by transpiler.  
So use below code/string replacing script-codes, mentioned in below linked SO/SE pages:
* These SO(StackOverflow)/&#8239;SE(StackExchange) Q+A(s) are showing various solutions:  
  `•` [Use sed to replace a multi line string][88].  
  `•` [Do recursive find &amp; replace string with awk or sed][89].  
  `•` [Find &amp; replace string in all files recursively using grep &amp; sed][90].  
  `•` [How can I replace a newline &#40;&#92;n&#41; using sed&#63;][91].  
  `•` [Re2c][92]: fast flexible scanner for regular expression matching.  
  `•` [Recursively read folders & execute command on each][93].  
  `•` [Process all files in all directories][94].  
  `•` [Execute command on all files in a directory][95].  
  `•` [In Bash, Handle paths that have spaces and wildcards][96].  
<br />



ANY USER/PEOPLE HAVE FULL FREEDOM+RIGHT+CHOICE TO CHOOSE ANY LANGUAGE & ANY TRANSPILER<sup>[1][64], [2][65], [3][66], [4][67], [5][68]</sup>.

SOURCE TRANSPILING & SOFTWARE DEVELOPMENT (BASIC)<b>:</b>  
* So, to clarify to READERS & ALL, after reading more advice of more knowledgeable persons & their discussions, (and also IMHO), the CORRECT ADVICE is<b>:</b>
  * there are some USE CASES where using `C/C++` is better, if that is the case for your software need or your project's target/objectives, then TRANSPILE `Go`/`✱` into `C/C++` with transpiler, Or transpile manually by hand-typing in `C`/`C++` code, by replacing `Go`/`✱` (with equivalent `C`/`C++` code) . Which steps you will take, that freedom & choice is yours.
  * And there are also some USE CASES where using `Go` is better, if that is the case for your software need or project's target, then you should avoid conversion/transpilation of `Go` into something else, instead improve existing `Go` codebase, if you can after learning it . And again, which steps you will take, that freedom & choice is yours.
  * So, transpile into `C`/`C++`, when features & specialties & benefits of `C`/`C++` usage are needed, And know firsthand/early, where (aka: in which USE CASES) `C`/`C++` excels and where `Go` excels, then decide to do+follow correct & balanced steps.
    * Use multiple search-engine websites to find-out <b>:</b> "<i>When to use Go/Golang</i>", "<i>When to not use Go/Golang</i>", "<i>When to use `C/C++`</i>", "<i>When to not use `C/C++`</i>", or use only `C` or `C++` or `Go` or `Golang`, etc.
* Anyone can transpile/translate any source-code for personal use or for test purpose, etc, etc . Information related activities are fundamental human rights <sup>[1][64], [2][65], [3][66], [4][67], [5][68]</sup> . Everyone has fundamental-rights to transpile/translate any lang code into any other lang code, for-example: to defend ourselve from harmful code, etc.
* For example, If you don't understand a Book written in French, then learning French would be "good" but it will for sure take you many many months or years to actually understand many facets & layers of French in order to accumulate related layers of required understanding/knowledge on French, but "better" is to have the content (that Book) TRANSLATED by expert language-translators into your own NATIVE LANGUAGE OR simply find the translated version of that Book (many Book publishers publish translated editions when its popular), then you will actually understand it (that Book's translation) much much better . Normally human cannot learn ALL about French within even 6months<b>.</b>
* If you want to add a very specific feature in a (specific) software, later we will call it "upstream" software, which that software's dev has denied to add, then ask again & this time propose to sponsor/pay to add that feature if you have (monetary) resource.  
• But when that is not possible, you can try to add that feature by yourself in a "fork" of that software. Specify publicly in your fork, what exactly you're trying to do in your fork. You may even find more users contributing in your fork to develop/improve that feature, to ultimately include improvements in that upstream software.  
• But, if you do not understand the language used in that (upstream) software very well, then one option is to learn it, & try to understand related sections, so "fork" that (upstream) software, & try to add new feature in that forked software . You can add copyright notice on your code & code-files contribution, but usually you have to release it with same license used by the "upstream" project, not with a different or incompatible license.<sup>[1][97], [2][98], [3][99], [4][100]</sup>  
Disclaimer: IANAL.  
• If above steps are not working well to achieve your goal/objectives, then, one of the option you have is: "Transpile" the entire (upstream) software into the "destination" computer language which is your native computer language which you have LEARNED & understand better. By the way, this is not an easy option.  
• So begin with by creating a new project in GitHub<sup>[1][101]</sup>, BitBucket<sup>[1][102]</sup>, GNU-Savannah<sup>[1][103]</sup>, SourceForge<sup>[1][104]</sup>, GitLab<sup>[1][105]</sup>, etc etc various open-source code collaboration repository sites<sup>[1][25]</sup> (aka: SCH=Source-Code-Hosting), choose such site where more devs with higher-skill on that "destination" computer language are hanging-out, and posses friendly collaborative spirit . Or, create project in multiple code-collaboration sites & SYNC each one after each code-update . Or, load Git<sup>[1][106], [2][107], [3][108]</sup> VCS (version control software<sup>[1][109]</sup>) in your own server or personal computer, & put your transpiled code in it. (Repo=Repository)  
• Transpile a specific version of upstream software inside your own computer, then immediately upload output source-code of transpilation, into your SCH or VCS, either publish it publicly if you want to share it , Or create "private"-type repo (without publishing it publicly) . If you're skilled enough to develop all side by yourself, then "private"-type repo is useful, Or, keep it "private" until you completely convert all remaining `Go` into `C/C++` . If you publish publicly then other devs/users can see & may join to improve it or contribute in it.  
• In source-code conversion/transformation steps, if input source-code is `GPL` licensed, then output also have to be licensed under `GPL` (in most cases. CWPL) . And without all copyright-holder(s) & code-contributor's permission, the `GPL` license (generally) cannot be changed into another license . When input source-code is licensed under `Apache`, `BSD`, `MIT`, etc (or code was released in Public Domain) then output can have same Or different license . If you use or have used your own hand, eye, brain to transform/transpile (aka: source-to-source code conversion) manually some portions or significant portions of source-code, then you can claim copyright ONLY on the portions of code which you yourself have manually by yourself modified or transformed or written (without using any machine/software based transpilation), so in such case you can add your name under the input/"upstream" software's copyright-holder(s) name, in the destination language (here `"C/C++"`) code . If you have used machine or mechanized process or software to do complete code transpilation, then you cannot claim any copyright on any portion which were transpiled in such way (because, a machine has done it, not you), and in such case, input/"upstream" software's copyright-holder(s) name(s) must be added/declared back into the destination/output source-code, (and again, you cannot add your name under those "upstream"/input software's copyright-holders).<sup>[1][110]</sup>&#160;  If you have seen (input) source-code or source-algorithms, and then if you have written / transformed those algorithms with your own hand, eye, brain, etc manually by yourself into a DIFFERENT destination/output language based code, here `C/C++`, only then, it is a totally new work done/created by you, (and if input & output has same language, then you can only see "algorithms" of source-code, not the source-code itself, to create "new work", otherwise it will be treated as a "derivative work"), so in such "new work" case, you can add your name as copyright-holder, without adding "upstream"/input software's previous copyright-holder(s), & you can also use whichever license you prefer, for output code.  
  Disclaimer: IANAL. CWPL.  
• Usually, in a transpiled output/destination code , many many code-portions have to be re-worked/re-written, to functionally perform same-way as "upstream" (aka: input source-code) software , especially those portions, which you did/could not transpile during manual transpilation/transformation process, and, there will also be many many non-transpiled source-code portions, when you have used mechanized (or automated) transpilation process or transpiler software, as these tools are not yet capable to transpile (all type of codes) completely, and instead transpiles only a subset(smaller portion) of (simple or limited-advanced) input source-code language into destination/output language . So you have to write, fix, adjust, & adapt ("destination" language) source-code, and compile / run / test / improve it.  
• Once you have achieved the state, where, your (transpiled output/destination code based) software can run same-way as upstream software, then start adding your feature that you need to add . You may also find that other devs have began to join & contribute in this new project.  
• In any OPEN-SOURCE project, one of the most helpful thing to bring in more code contributors is : Addition of DETAIL COMMENTS & NOTES on each code line & section, and describe what a code-line/code-section is actually doing . So create a ToDo for yourself & for any code-contributors, that, beside improving code directly, this new project also need contribution of more detail COMMENTS & NOTES ON CODE . So that some devs can spend time on understanding + identifying each line & section & algorithm, and start adding detail general human-friendly notes & comments . Do not make comment & note helpful only for advanced devs, that creates islands & separation & division . That is opposite of open-source spirit . Everyone, even general user, should be able to understand a code line/section, after reading comments & notes.  
• If upstream software's dev also transpiles new feature, that you or your team has added into the software, then upstream dev can also add it into the upstream software.  
• Abbreviations : IANAL = I Am Not A Lawyer . CWPL = Consult With Professional Lawyer.  
<br />
<br />
<br />
Transpiler.And.Similar.List : <a href="#list">Copyright</a> (C) 2020  atErik (Erik T. Ashfolk).


  [1]: https://en.wikipedia.org/wiki/Source-to-source_compiler
  [2]: https://cs.stackexchange.com/questions/67284/
  [3]: https://github.com/elliotchance/c2go#usage
  [4]: https://stackoverflow.com/questions/8788866/
  [5]: https://github.com/Konstantin8105/c4go#example-with-c-pointers-and-c-arrays
  [6]: https://bravenewgeek.com/go-is-unapologetically-flawed-heres-why-we-use-it/
  [7]: https://www.yager.io/programming/go.html
  [8]: https://www.toptal.com/go/4-go-language-criticisms
  [9]: https://www.cvedetails.com/vulnerability-list/vendor_id-14185/Golang.html
  [10]: https://www.cvedetails.com/vulnerability-list.php?vendor_id=14185&product_id=29205
  [11]: https://www.cvedetails.com/vulnerability-list/vendor_id-14185/product_id-36900/Golang-Crypto.html
  [12]: https://cxsecurity.com/cveproduct/13980/26095/go/
  [13]: https://security.stackexchange.com/questions/194557/
  [14]: https://tomassetti.me/how-to-write-a-transpiler/
  [15]: https://github.com/GridProtectionAlliance/go2cs
  [16]: https://github.com/yanghuan/CSharp.lua
  [17]: https://github.com/davidm/lua2c
  [18]: https://github.com/aspnet/AspNetCore/tree/master/src/Components
  [19]: https://github.com/WebAssembly/wabt/tree/master/wasm2c
  [20]: https://github.com/lpereira/gomoku
  [21]: http://www.softwarepreservation.org/projects/c_plus_plus
  [22]: http://www.comeaucomputing.com/
  [23]: https://github.com/mukadr/go2c
  [24]: https://stackoverflow.com/questions/737257/
  [25]: https://stackoverflow.com/questions/15970804/
  [26]: https://stackoverflow.com/questions/1833484/
  [27]: https://stackoverflow.com/questions/5050349/
  [28]: https://github.com/gopherc/goc
  [29]: https://github.com/mewbak/go-transpiler
  [30]: https://sourceforge.net/projects/boomerang/
  [31]: https://github.com/radareorg/radare2
  [32]: https://github.com/radareorg/r2dec-js
  [33]: https://github.com/frranck/asm2c
  [34]: https://reverseengineering.stackexchange.com/questions/3748/
  [35]: https://stackoverflow.com/questions/1376856/
  [36]: https://reverseengineering.stackexchange.com/questions/2096/
  [37]: https://sourceforge.net/projects/hurley/
  [38]: https://github.com/supercoww/go-transpiler
  [39]: https://github.com/andygeiss/esp32-transpiler
  [40]: https://github.com/xyproto/go2cpp
  [41]: https://github.com/vaquierm/GoLite_Transpiler
  [42]: https://github.com/ASDAlexander77/cs2cpp
  [43]: https://github.com/AlexAlbala/Alter-Native
  [44]: https://github.com/dotnet/corert
  [45]: https://github.com/onelang/OneLang
  [46]: https://github.com/terotests/Ranger
  [47]: https://github.com/Theodus/go-transpiler
  [48]: https://en.wikipedia.org/wiki/Abstract_syntax_tree
  [49]: https://en.wikipedia.org/wiki/Lexical_analysis
  [50]: https://en.wikipedia.org/wiki/Syntax_analysis
  [51]: https://en.wikipedia.org/wiki/Comparison_of_parser_generators
  [52]: https://en.wikipedia.org/wiki/Semantic_analysis_%28compilers%29
  [53]: https://en.wikipedia.org/wiki/Intermediate_representation
  [54]: https://en.wikipedia.org/wiki/Intermediate_language
  [55]: https://en.wikipedia.org/wiki/Metaprogramming
  [56]: https://en.wikipedia.org/wiki/Natural_language_processing
  [57]: https://en.wikipedia.org/wiki/Finite-state_machine
  [58]: https://en.wikipedia.org/wiki/Automata-based_programming
  [59]: https://en.wikipedia.org/wiki/Parser_generator
  [60]: https://en.wikipedia.org/wiki/Parsing#Computer_languages
  [61]: https://devopedia.org/transpiler
  [62]: https://stackoverflow.com/questions/29193069/
  [63]: https://engineering.mongodb.com/post/transpiling-between-any-programming-languages-part-1
  [64]: https://en.wikipedia.org/wiki/Freedom_of_Information
  [65]: http://www.unesco.org/new/en/communication-and-information/freedom-of-expression/freedom-of-information/about/
  [66]: https://www.ohchr.org/EN/NewsEvents/Pages/RightToKnow.aspx
  [67]: https://en.wikipedia.org/wiki/Freedom_of_speech
  [68]: https://www.un.org/en/sections/issues-depth/human-rights/
  [69]: https://benchmarksgame-team.pages.debian.net/benchmarksgame/
  [70]: https://julialang.org/benchmarks/
  [71]: https://attractivechaos.github.io/plb/
  [72]: https://github.com/drujensen/fib
  [73]: http://www.hildstrom.com/projects/langcomp/index.html
  [74]: https://github.com/kostya/benchmarks
  [75]: https://modelingguru.nasa.gov/docs/DOC-2783
  [76]: https://cs.stackexchange.com/questions/40400/
  [77]: https://cs.stackexchange.com/questions/71979/
  [78]: https://en.wikipedia.org/wiki/The_Computer_Language_Benchmarks_Game
  [79]: https://benchmarksgame-team.pages.debian.net/benchmarksgame/q6600/which-programs-are-fastest.html
  [80]: https://en.wikipedia.org/wiki/Comparison_of_programming_languages_%28basic_instructions%29
  [81]: https://en.wikipedia.org/wiki/Comparison_of_programming_languages_%28syntax%29
  [82]: https://en.wikipedia.org/wiki/Higher-order_function#Support_in_programming_languages
  [83]: https://en.wikipedia.org/wiki/Operator_%28computer_programming%29#Operator_features_in_programming_languages
  [84]: https://en.wikipedia.org/wiki/Comparison_of_programming_languages_%28object-oriented_programming%29
  [85]: https://en.wikipedia.org/wiki/Constructor_%28object-oriented_programming%29
  [86]: https://en.wikipedia.org/wiki/Exception_handling_syntax
  [87]: https://en.wikipedia.org/wiki/Preprocessor
  [88]: https://unix.stackexchange.com/questions/26284/
  [89]: https://stackoverflow.com/questions/1583219/
  [90]: https://stackoverflow.com/questions/15920276/
  [91]: https://stackoverflow.com/questions/1251999/
  [92]: https://sourceforge.net/projects/re2c/
  [93]: https://stackoverflow.com/questions/1333813/
  [94]: https://stackoverflow.com/questions/55789226/
  [95]: https://stackoverflow.com/questions/10523415/
  [96]: https://unix.stackexchange.com/a/607424/367237
  [97]: https://gitlab.com/the-language/lua2rust
  [98]: https://objectivec2swift.com/#/converter/code/
  [99]: https://github.com/LuizZak/SwiftRewriter
  [100]: https://github.com/elliotchance/c2go
  [101]: https://en.wikipedia.org/wiki/GitHub
  [102]: https://en.wikipedia.org/wiki/Bitbucket
  [103]: https://en.wikipedia.org/wiki/GNU_Savannah
  [104]: https://en.wikipedia.org/wiki/SourceForge
  [105]: https://en.wikipedia.org/wiki/GitLab
  [106]: https://git.kernel.org/pub/scm/git/git.git/
  [107]: https://git-scm.com/
  [108]: https://en.wikipedia.org/wiki/Git
  [109]: https://en.wikipedia.org/wiki/Comparison_of_version_control_software
  [110]: https://opensource.stackexchange.com/questions/10521/
