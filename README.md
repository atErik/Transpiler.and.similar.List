# Transpiler.and.similar.List

List Of Transpilers, TransCompilers, Decompilers, etc &amp; similar &amp; related tools/apps.  
( History : I created a [question](https://stackoverflow.com/questions/64180191/) in StackOverflow, where i have initially asked Which transpiler can convert `"Go"` source-code into `"C"` source-code, and then i had to change question & ask : Which transpiler (out of four specific transpiler) can convert from `Go` to `C/C++` and can still keep (almost all) high-level algorithms & structures used in source-code , fairly accurately same/intact in output source-code . And this project/data borned from that research, so later when StackOverflow's `"PRO-GOOGLE"` & `"PRO-GO"` evil mods ganged-up on the Quesiton+Answer & deleted it , i had to publish from github here & improve it here. )

<a name="License"></a>
<div width="100%"><b>LICENSE of this project "Transpiler.and.similar.List":</b><br />
 "Transpiler.and.similar.List" project pages, info, data, file, etc
 are <b>Released with following combined LICENSE(s) + 
 RESTRICTIONs + PERMISSIONs:</b><dl>
 <dd> 
  <b class="b">•</b> Do Not Use This To Kill/Harm/Violate (or Steal-from)(Any) Human/Community,Earth,etc.<br />
  <b class="b">•</b> Do Not Use Any Data/File From This Project Into Military,Offense/Attack Forces,etc.<br />
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
  "Transpiler.and.similar.List" : List of transpilers, transcompilers, etc.<br />
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
  <h3>IF YOU DO NOT AGREE WITH ABOVE LICENSE RESTRICTIONS & PERMISSIONS , THEN YOU CANNOT USE ANY DATA/SERVICE FROM THIS PROJECT , PRESS BACK BUTTON IN YOUR WEB-BROWSER , AND COMPLETELY STOP USING/VIEWING THIS WEBPAGE/DATA.</h3>
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
  
( You may goto LIST OF TRANSPILERS directly from <a href="#list">here</a> )  
  
For example, when input code (`"Go"` language code) contains:

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


then, this `"Go"`-to-`"C"` conversion/transpilation<sup>[1][1]</sup> process need to convert & generate/output below `"C"` language code:

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

when `"Go"`-to-`"C++"` (`C++14`) transpilation is done, then output should be:

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

when `"Go"`-to-`"C++"` (`C++11`) transpilation is done, then output should be:

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

An actual EXAMPLE of "C"-to-"Go" CODE is shown [here][2] <sup>[2][3], [3][4]</sup>, but we want opposite of "C"-to-"Go" : so we want "Go"-to-"C" (go-to-c / go2c).  
<br />

FEW&#160; POINTS:  
`•` Let us assume, you're more familiar with `"C"` & `"C++"`, than `"Go"`.  
`•` In computer programming language, let us assume, `C`/`C++`/`Assembly` are your native computer language (these you have learned in University, & then practiced).  
`•` So it should be okay to convert `non-C` & `non-C++`/`nonCpp` language `"Go"` aka: `"Golang"` , into `"C"` or `"C++"`, to understand better.  
`•` Learning a second computer language (for example: `"Go"`) & hoping to be expert within 7-days or so , like your native computer language `"C"` or `"C++/Cpp"`, is a plain wrong expectation , and i consider a wrong advice . But one of the good advice can be this : Start to learn the second computer language in parallel, as it will take long time to become expert in that second computer language.  
`•` So we do not want to keep any input (`"Go"`) code remaining in output (`C/C++`) source-code . But (some) `Assembly` is fine in output (if you're okay with `Assembly`) . Be aware of that ['Go' Has Problems][5] <sup>[2][6], [3][7]</sup> , [Security Vulnerabilities of 'Golang'][8] <sup>[2][9], [3][10], [4][11], [5][12]</sup>, etc are just few reasons to move away from `"Go"`, and use other language . You have full freedom & right to choose what you want to do.  
`•` Let us assume, Necessary Features or Functionality that i or you need to add, those are developed & optimized for `C/C++`, not-available in `"Go"`.  
`•` Programs that i or you want to TRANSPILE/CONVERT from `Go-to-C` or from `Go-to-C++`, that type of programs should be developed with `C/C++`, as that type of programs work better with `C`, and even more better with `C++`.  
`•` Recreating complex & large software/systems with years of development from scratch with another (second) computer language , is not-only hard , that is also not-suggested<sup>[1][13]</sup> (not-adviced) , So transcompilation steps are helpful to give a head-start by converting easier source-code . Transcompilation process always requires human developer based manual code conversion, as none of the Transpilers are perfect or supports ALL aspects of source/input language or different programming styles, codes, libraries, etc that are used in real practical projects/languages . Small project(s) or new project can be built from scratch, and even by using a second computer language.  
`•` If source code is from open-source project , then Human/manual and/or automated transpilation of output source-code should also be released as open-source , same as input source-code . In that way, another group of developers skilled at output language (`C/C++`) can also participate in open-source development, to help all users & people.  
<br />  

SOLUTIONS&#160; FOR&#160; `Go`-To-`C`<b>:</b>  
Currently, i SPECIFICALLY have these four solutions/choices to use:  
`•` Solution A or #1 : "[go2cs][14]", "[CSharp.lua][15]", "[lua2c][16]".  
`•` Solution B or #2 : "[go2cs][14]", "[Blazor][17]", "[wasm2c][18]".  
`•` Solution C or #3 : "[gomoku][19]", "[Cfront][20]" or "[Comeau C&#47;C&#43;&#43;][21]".  
`•` Solution D or #4 : "[go2c][22]".  
<br />


ANOTHER&#8239;/&#8239;ALTERNATIVE OPTION & SOLUTION (`"Go"-to-"C++"`)<b>:</b>  
As other developers have pointed out, in some cases `C++` (based compiled program) can often be much better & faster than `C` ones, so i'm also displaying these below few options to convert/transpile `Go` directly into `C++` while keeping higher-level structures fairly intact, & output `C++` code is also easier to improve as/when necessary:
* ALT-SOLUTION A or &#35;1<b>:</b> use [gomoku][19] for `Go` to `C++`.  
  ALT-SOLUTION B or &#35;2<b>:</b> use [go2cpp][23] for `Go` to `C++20`/`C++17`.  
  ALT-SOLUTION C or &#35;3<b>:</b> use [GoLite Transpiler][24] for `GoLite` (subset of `Go`) to `C++` . GoLite Transp supports only subset of `Go`.  
  ALT-SOLUTION D or &#35;4<b>:</b> use [go2cs][14] for `Go` to `C#`(C-Sharp), then use any of these: [cs2cpp][25], [Alter-Native][26], [CoreRT][27], [OneLang][28], [Ranger][29], etc to convert `C#` into `C++`.  
  ALT-SOLUTION E or &#35;5<b>:</b> use [go-transpiler][30](Theodus) for `Go` to `C++`.
* CONCLUSION ON `"Go"`-to-`"C++"`<b>:</b>  
  Alt-Solution-A (gomoku) is obviously slightly better than Alt-Solution-B (go2cpp),  
  and Alt-Solution-B (go2cpp) is much better than Alt-Solution-C (GoLite Transp),  
  and Alt-Solution-D (go2cs+cs2cpp) is also much better than Alt-Solution-C (GoLite Transp).  
  in Alt-Soln-D, though `go2cs` conversion quality is higher, but next stage `cs2cpp` tools are not.  
  and Alt-Solution-D (go2cs+cs2cpp) is better than Alt-Solution-B (go2cpp).  
  So Alt-Solution-A (gomoku) is best at this point, among these available transpiler choices, (when this message was posted here).  
<br />


WHICH&#160; SOLUTION&#160; (out of above FOUR solutions) IS BETTER <b>?</b>  
( better at keeping high-level algorithms/structures,etc fairly or accurately same in output source-code )  
is there (similar) better transpiler solution, among the links that i have shown ?  
Along with `Go-to-C` conversion , if you can then please show `Go-to-C++` conversion.  
Above four (transpiler-set) solutions have what Pros/Cons ?  
<br />
<br />

abbreviations : `aka` = also known as

TRANSPILER<sup>[1][31]</sup><b>:</b>  
Transpiler/Transcompiler internally contains primarily three major components<b>:</b>
* 1of3: Parser : it is used to create AST<sup>[1][32]</sup> from input/source code, by using Lexical<sup>[1][33]</sup> analysis and Syntax<sup>[1][34]</sup> analysis.  
  • [Comparison of Parser-Generators and Lexer-Generators][35].
* 2of3: Transformation : with one or more steps, input code's AST will be converted into output/target code's AST . Uses semantic<sup>[1][36]</sup> analysis, Intermediate Representation (IR)<sup>[1][37]</sup> generation . IR is aka: Intermediate Language (IL)<sup>[1][38]</sup>.
* 3of3: Generator : output AST is used to generate output/target language code.
* Transpiler can/may use MetaProgramming<sup>[1][39]</sup>, NLP(Natural Language Processing)<sup>[1][40]</sup>, Finite-state Automata<sup>[1][41], [2][42]</sup>, Lexical Analysis<sup>[1][33]</sup>, Syntax/AST Analysis<sup>[1][32]</sup>, Parser<sup>[1][43], [2][44]</sup>, etc<sup>[1][35]</sup>, etc, to convert source-code of one CLP(computer programming language) into source-code of another CLP.
* Notes/References:  
  `•` [Transpiler][45].  
  `•` [How to write a transpiler][13], [2][46].  
  `•` [Transpiling between any languages][47].  
<br />
<br />

OTHER&#160; INFORMATION&#160; &&#160; REFERENCES<b>:</b>  

**Go2C** Conversion : My objective is here is to share simple steps/directions on converting / transpiling `Go`-language source-code into `C`-language (or `C++`) source-code, with one of the mentioned (in above) possible set of TRANSPILER solutions, that can still keep high-level algorithms / structures, etc used in initial/input `Go` source-code , fairly or accurately same/intact in final destination / output `C` (or `C++`) source-code.  
Then we can compile `C/C++` code into binary machine code when necessary, to run it faster.  
So after `Go-to-C` or `Go-to-C++` source-code conversion , it will be possible to change source-code (to add required necessary feature or functionality) & improve `C` (or `C++`) source-code.  
<br />
<br />

Some users suggested wrong+incorrect things in their answer/comment.  
So i have added data/info from accredited computer COMPETITION, BENCHMARKS, etc to prove which is better & which is not.  
And, ANYONE/USER/people have full freedom+right+choice to choose what he/she wants, and also have full freedom+right to convert one language into another.<sup>[1][48], [2][49], [3][50], [4][51], [5][52]</sup>  
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
Various benchmarks: [1][53], [2][54], [3][55], [4][56], [5][57], [6][58], [7][59].
* Please see these Q+A on CS.StackExchange site<b>:</b>  
  [What Determines the Speed of a Programming-language?][60]  
  [Why are some programming languages “faster” or “slower” than others?][61]  
  `CS` = Computer-Science.
* Benchmarks from "[The Computer Language Benchmarks Game][62]" (CLBG) are based on <b>:</b> Overall user runtime, Peak memory allocation, Gzip'ped size of the solution's source code, Sum of total CPU time over all threads, Individual CPU utilization . BE-AWARE <b>:</b> many notable developers pointed out results are not perfect benchmarks, due to: various programming techniques, configuration issues, weak programming, etc that exist in various software & hardware tools & human expertise.  
  In this CLBG [page][63] you can see performance chart on compiled program of different computer programming language (CPL) . I'm displaying names of selected few (not all) CPL in below from "Program Busy Time / Least Busy" category chart of July-1, 2020, in the ORDER of their placement shown there , so, better performing one is mentioned earlier in left-side , & less-better are mentioned later or after that <b>:</b> `C++` (`g++`), `C` (`gcc`), `Rust`, `Julia`, `Intel Fortran`, `Ada 2012`, `C# .NET Core`, `Free Pascal`, `F# .Net Core`, `Go`, `Java`, etc.
* RESULT <b>:</b> So you can see in above section, there is a huge performance gap between `Go` & `C` . The `"Go"`(Golang) is ~2 to ~5.25 TIMES SLOWER THAN `"C"` . `"Go"/"Golang"` is ~2.25 to ~7 TIMES SLOWER THAN `"C++"`.  
<br />

COMPARISONS<b>:</b>  
Comparison of Programming Language's ...  
`•` [Basic instructions][64].  
`•` [Syntax][65].  
`•` [Higher-order function][66].  
`•` [Operators][67].  
`•` [Object-Oriented Programming(OOP)][68].  
`•` [OOP Constructor][69].  
`•` [Exception handling][70].  
<br />
<br />

<a name="list"></a>
LIST<b>:</b>

abbreviations: `JS` = JavaScript &#124; `Asm` = Assembly &#124; `C++` = `Cpp` = C plus plus &#124; `AS` = ActionScript &#124; `✱` = any = others = few others

By the way, here is a list of `Go-to-C` and `Go-to-C++` and other type of SOURCE-CODE CONVERTER/&#8239;TRANSPILER from various websites<b>:</b>
* `Go` to `C`:  
`•` [go2c][22] (mukadr)  
`•` [go-transpiler][71] (mewbak)  
`•` [goc][72]  
`•` <s>&#160;[go-transpiler][73] (supercoww)&#160;</s>
* `Go/Golang` to `C++/Cpp`:  
`•` [gomoku][19]  
`•` [go-transpiler][30] (Theodus) (powered by tardisgo)
* `Go` to `C++20` & `C++17`:  
`•` [go2cpp][23] (xyproto)
* `Go/Golang` to `C#` (C-sharp):  
`•` [go2cs][14] (GridProtectionAlliance)
* `Go/Golang` to `C++11`:  
`•` [meego][74] (miniature bootstrapped `Golang` to vanilla `C++`)
* `✱` (various programming languages) to `C/C++` source:  
`•` [Programming languages that compile to `C/C++` source&#63;][75]
* `C++` to `C`:  
`•` CFront, Comeau `C/C++`  
`•` [How to convert C&#43;&#43; Code to C][76]  
`•` [&#67;&#43;&#43; implemented in plain C][77]  
`•` [&#67;&#43;&#43; frontend only compiler &#40;convert &#67;&#43;&#43; to C&#41;][78]  
`•` [Compile Cpp to C code][79]  
`•` [llcc][80] (cpp-&gt;llvm-&gt; ansi C transpiler kit) LLVM-powered `C/C++` toolchain for Cortex-M.
* `C` to `C++`:  
`•` [ctcpp][81]
* `Go` to `✱` & `C`:  
`•` [go-transpiler][71] (mewbak)
* `Rust` &amp; `✱` to `C`:  
`•` [llvm-cbe][82]  
* `Rust` to `C`:  
`•` [llvm-cbe][82]  
`•` [mrustc][83]
* `Java` to `C`:  
`•` [java2c][84]  
`•` [java2c][85] (RaphaelCohn)  
`•` [jack][86] (BadLogic)
* `Java` to `objC`:  
`•` [j2objc][87]
* `Python` program&#47;source to `C/C++` code:  
`•` [Convert Python program to C&#47;C&#43;&#43; code&#63;][88]  
`•` [nuitka][89]<sup>[2][90]</sup>  
`•` [py14][91] (`Python` to `C++14`)
* `Python` to `C`:  
`•` [transpiler][92] (gaurav139v)  
`•` [transpyle][93] (`Python`&lt;--&gt;`C`)  
`•` [py2cmod][94] (`Python` To `C` Module Generator)  
`•` [RPython][95]<sup>[2][96]</sup> (Subset of `Python` --&gt;`C`)  
`•` [ptc][97]
* `Lua` to `C`:  
`•` [lua2c][16] (davidm)
* `WebAssembly`-source to `C`:  
`•` [wasm2c][18]
* `Assembly`-source to `C`:  
`•` [Boomerang][98]  
`•` [RetDec][99]  
`•` [masm2c][100](xor2003) (DOS x86 (MASM)<sup>[2][101]</sup> assembler code to SDL C)  
`•` [asm2c][102](frranck) (DOS/PMODEW 386 TASM `Assembly`-code to `C`)  
`•` [Dcc][103] (DOS (8086/16-bit) `Assembly`-code to `C`)
* `Assembly`-source to `C++`:  
`•` [asmeta][104]  
`•` [CPP-to-Assembly-to-CPP][105]
* `JavaScript`/`JS`/`TypeScript` to `C`:  
`•` [ts2c][106]
* `Perl` to `C`:  
`•` [Perl2C][107]
* `Lisp` to `C`:  
`•` [LispTranspiler][108]/`lispc`  
`•` [ECL][109]<sup>[2][110]</sup> (`Common-Lisp`-to-`C`)
* `Go-Lite` (subset of `Go`) to `C++`:  
`•` [GoLite Transpiler][24]
* `C#` to `C++/Cpp`:  
`•` [cs2cpp][25] (ASDAlexander77) (powered by Roslyn)  
`•` [Alter-Native][26]<sup>[2][111]</sup> (`C#` & `✱` to `C++`)  
`•` [CoreRT][27] (`.NET`/`C#` to `C++`)  
`•` [Hurley][112]
* `Lisp` to `C++`:  
`•` [TinyCompiler][113]
* `Python3` to `C++11`:  
`•` [javelin][114]
* `TypeScript` to `C++11`:  
`•` [ts2cpp][115]
* `C/C++` to `Rust`:  
`•` [crust][116]
* `C` to `Rust`:  
`•` [corrode][117]  
`•` [crust][116]  
`•` [c2rust][118]  
`•` [cparser][119]/cparser-to-rust  
`•` [citrus][120]
* `TinyCC` (tiny `C`) to `Rust`:  
`•` [tinycc-rs][121]
* `Python` to `Rust`:  
`•` [pyrs][122]  
`•` [serpent-rs][123] (Python to Rust AST-to-AST transpiler prototype)
* `Clojure` to `Rust`:  
`•` [rustly][124]
* `Ruby` to `Rust`:  
`•` [Rusby][125]
* `Clojure` to `Rust`, `C++`, `Java`, `Clojure`:  
`•` [Kalai][126]
* `CoffeeScript` to `Rust`:  
`•` [RusteeScript][127]
* `Lua` to `Rust`:  
`•` [lua2rust][128] (the-language)
* `objC` to `Swift`:  
`•` [Swiftify][129]  
`•` [SwiftRewriter][130]
* `C` to `Go`:  
`•` [Tool to convert &#40;translate&#41; C to Go&#63;][3]  
`•` [c2go][131] (elliotchance)  
`•` [c4go][132]
* `C`-`Assembly` source to `Go`-`Assembly` source:  
`•` [c2goasm][133]
* `C` to GNU-`Assembly`<sup>[2][134]</sup>(`GAS`) source:  
`•` use cmd: `gcc -S example.c`, & check `example.s` file
* `C++`/`Cpp` to GNU-`Assembly` source:  
`•` use cmd: `gcc -S example.cpp`, & check `example.s` file  
`•` [CPP-to-Assembly-to-CPP][105]
* `C`(generic) to `NASM`(elf64)<sup>[2][135]</sup> `Assembly` source:  
`•` [ape][136]
* `C` to `NASM`-`Assembly` source:  
`•` [c2nasm][137]<sup>[1][138], [2][139]</sup>
* `Rust` to `WebAssembly`(wasm):  
`•` [yew][140]
* `Python` to `WebAssembly`:  
`•` [Compiling Python to WebAssembly][141]
* `C#` to `Lua`:  
`•` [CSharp.lua][15]
* `C#` to `WebAssembly`:  
`•` [Blazor][17]
* `C#` to `D`, `C++11`, `Java`, `Swift`:  
`•` [SharpNative][142] (powered by Roslyn)
* `C#` to `C`, `C++`, `Nim`, `D`, `Go`, `Java`, `JavaScript`, `Python`, `ActionScript`:  
`•` [CSharpTranspiler][143] & [CS2X][144] (powered by Roslyn)
* `Go` to `Python`:  
`•` [gotopython][145]
* `Go` to `JavaScript`:  
`•` [gopherjs][146]
* `Go` to `Java`:  
`•` [go-transpiler][30] (Theodus) (powered by tardisgo)
* `Go` to `Haxe`:  
`•` [tardisgo][147]
* `Go` to `Ruby`:  
`•` [gruby][148]
* `Go` to `JSON`:  
`•` [go2json][149]
* `Go` to `Go-"Assembly"`<sup>[1][150]</sup>:  
`•` run cmd: `go tool compile -S Main.go` (Google/Golang flavored `"Assembly"`<sup>[2][151]</sup>, its NOT general `Assembly`),  
  or, run this cmd: `go build -gcflags -S Main.go`
* `C#` &lt;--&gt; `VB.Net`:  
`•` [roslyn][152]
* `Rust`(MIR output) to `JavaScript`:  
`•` [cyano](https://github.com/ticki/cyano)
* `Rust` to `JavaScript`:  
`•` [fear](https://github.com/DevNvll/fear)
* `Fortran` to `C++`:  
`•` [fable](https://cci.lbl.gov/fable/)
* `Python` to `Java`:  
`•` [voc](https://github.com/beeware/voc)
* `C++` to `C#`:  
`•` [cxx2s](https://sourceforge.net/projects/cxx2cs/)
* `C++` to `Python`:  
`•` [seasnake](https://github.com/pybee/seasnake)  
`•` [cpp2python](https://github.com/andreikop/cpp2python)  
* From `Java`, `Kotlin`, `Scala`  
  to `JavaScript`, `C++`, `D`, `C#`, `PHP`, `AS3`, `Dart`, `Haxe`:  
`•` [jtransc][153]
* `Java` to `✱`:  
`•` [spoon][154]<sup>[2][155]</sup>
* `Haxe` to `ActionScript 3`/`AS3`, `AS2`, `JavaScript`/`JS`, `Java`, `C++`, `C#`, `PHP`, `Python`, `Lua`, `Neko`:  
`•` [Haxe][156]
* `C` to `✱`:  
`•` [CIL][157]  
`•` [Coccinelle][158] <sup>[2][159], [3][160]</sup>
* From `JavaScript`, `Java`, `Go`, `Swift`, `PHP`, `C++`, `C#`, `Scala`  
  to `JavaScript`, `Java`, `Go`, `Swift`, `PHP`, `C++`, `C#`, `Scala`:  
`•` [Ranger][29] (multi/cross language transpiler)
* From `Java`  
  to `Java`, `C`, `C++`, `JavaScript`, `C#`, `R`, `PHP`, `Python`, `VisualBasic`/`VBA`:  
`•` [Progsbase][161] (Community plan is free)
* From `C#`, `TypeScript`, `Ruby`  
  to `C++`, `C#`, `Go`, `Java`, `JS`, `Perl`, `PHP`, `Python`, `Ruby`, `Swift`, `TypeScript`:  
`•` [OneLang][28]
* `C` to `C#` , `JavaScript` to `Prolog` , `PHP` to `Python` , `Lua` to `Perl` or `PHP` , `C` to `Haskell` , `C#` to `Fortran` , `Java` to `OCaml` or `GLSL`:  
`•` [Universal-transpiler][162]<sup>[2][163]</sup>
* `pseudo` based Algorithms<sup>[1][164]</sup>/Libs to idiomatic<sup>[1][165]</sup> `Python 3`, `JS`, `Go`, `C#`, `Ruby`:  
`•` [pseudo][166]
* `CUDA` to Portable HIP<sup>[1][167]</sup> `C++/Cpp`:  
`•` [HIPIFY][168]<sup>[2][169], [3][170]</sup>  
`•` [cu2c][171] (`CUDA` to `C++`)
* `✱` to `✱` <sup>[1][172]</sup> : Framework/Library, etc:  
`•` [RascalMPL][173] <sup>[2][174], [3][175]</sup>  
`•` [JetBrains MPS][176] <sup>[2][177] </sup>  
`•` [DMS Software Reengineering Toolkit][178] (DMS)  
`•` [ROSE compiler framework][179]
* Transpiling internals, tools, etc:  
`•` [Comparison of Parser-Generators][35]: see various types of internal parser engines.  
`•` [walkngo][180] (Walker for Go-AST)  
`•` [llvm2c][181](staticafi) fork of [llvm2c][182](petrv7) LLVM bitcode to `C`  
<br />



abbreviation : `CPL` = Computer Programming Language.

HOW TO DETERMINE WHICH ONE IS BETTER THAN ANOTHER<b>:</b>

SUPPORTED COMMANDS/INSTRUCTIONS, FUNCTIONS, etc in CPL<b>:</b>  
Transpiler software primary-dev or project's website displays list of supported commands/instructions, functions, etc language components . Their primary developer(s) & other developers are developing+improving those transpiler-projects when they can . So, often check out those lists, & COMPARE, to find out which one is better.  
Then use same source file and convert with multiple transpilers, and check output source-code file, to find out which transpiler able to do conversion completely or which portions are skipped or incorrect.  
Which one is BEST, that will always change or most-likely be different at different time.  
(and "BEST" is connected with "Category", so based on that there are different types of BEST, and at different time)
<br />

PRE & POST STEPS<b>:</b>  
Most of the time, certain code/strings need to be modified/changed, & prepared in each initial source-code (here `"Go"`) files (with [PreProcessor][183] type of software), before the primary transpiler can be used.  
And, often you have to change some specific style of code/string in each output (here `"C"` or `"C++"`) file , to fix or change something that was not automatically generated by transpiler.  
So use below code/string replacing script-codes, mentioned in below linked SO/SE pages:
* These SO(StackOverflow)/&#8239;SE(StackExchange) Q+A(s) are showing various solutions:  
  `•` [Use sed to replace a multi line string][184].  
  `•` [Do recursive find &amp; replace string with awk or sed][185].  
  `•` [Find &amp; replace string in all files recursively using grep &amp; sed][186].  
  `•` [How can I replace a newline &#40;&#92;n&#41; using sed&#63;][187].  
  `•` [Re2c][188]: fast flexible scanner for regular expression matching.  
  `•` [Recursively read folders & execute command on each][189].  
  `•` [Process all files in all directories][190].  
  `•` [Execute command on all files in a directory][191].  
  `•` [In Bash, Handle paths that have spaces and wildcards][192].  
<br />



ANY USER/PEOPLE HAVE FULL FREEDOM+RIGHT+CHOICE TO CHOOSE ANY LANGUAGE & ANY TRANSPILER<sup>[1][48], [2][49], [3][50], [4][51], [5][52]</sup>.

SOURCE TRANSPILING & SOFTWARE DEVELOPMENT (BASIC)<b>:</b>  
* So, to clarify to READERS & ALL, after reading more advice of more knowledgeable persons & their discussions, (and also IMHO), the CORRECT ADVICE is<b>:</b>
  * there are some USE CASES where using `C/C++` is better, if that is the case for your software need or your project's target/objectives, then TRANSPILE `Go`/`✱` into `C/C++` with transpiler, Or transpile manually by hand-typing in `C`/`C++` code, by replacing `Go`/`✱` (with equivalent `C`/`C++` code) . Which steps you will take, that freedom & choice is yours.
  * And there are also some USE CASES where using `Go` is better, if that is the case for your software need or project's target, then you should avoid conversion/transpilation of `Go` into something else, instead improve existing `Go` codebase, if you can after learning it . And again, which steps you will take, that freedom & choice is yours.
  * So, transpile into `C`/`C++`, when features & specialties & benefits of `C`/`C++` usage are needed, And know firsthand/early, where (aka: in which USE CASES) `C`/`C++` excels and where `Go` excels, then decide to do+follow correct & balanced steps.
    * Use multiple search-engine websites to find-out <b>:</b> "<i>When to use Go/Golang</i>", "<i>When to not use Go/Golang</i>", "<i>When to use `C/C++`</i>", "<i>When to not use `C/C++`</i>", or use only `C` or `C++` or `Go` or `Golang`, etc.
* Anyone can transpile/translate any source-code for personal use or for test purpose, etc, etc . Information related activities are fundamental human rights <sup>[1][48], [2][49], [3][50], [4][51], [5][52]</sup> . Everyone has fundamental-rights to transpile/translate any lang code into any other lang code, for-example: to defend ourselve from harmful code, etc.
* For example, If you don't understand a Book written in French, then learning French would be "good" but it will for sure take you many many months or years to actually understand many facets & layers of French in order to accumulate related layers of required understanding/knowledge on French, but "better" is to have the content (that Book) TRANSLATED by expert language-translators into your own NATIVE LANGUAGE OR simply find the translated version of that Book (many Book publishers publish translated editions when its popular), then you will actually understand it (that Book's translation) much much better . Normally human cannot learn ALL about French within even 6months<b>.</b>
* If you want to add a very specific feature in a (specific) software, later we will call it "upstream" software, which that software's dev has denied to add, then ask again & this time propose to sponsor/pay to add that feature if you have (monetary) resource.  
• But when that is not possible, you can try to add that feature by yourself in a "fork" of that software. Specify publicly in your fork, what exactly you're trying to do in your fork. You may even find more users contributing in your fork to develop/improve that feature, to ultimately include improvements in that upstream software.  
• But, if you do not understand the language used in that (upstream) software very well, then one option is to learn it, & try to understand related sections, so "fork" that (upstream) software, & try to add new feature in that forked software . You can add copyright notice on your code & code-files contribution, but usually you have to release it with same license used by the "upstream" project, not with a different or incompatible license.<sup>[1][128], [2][129], [3][130], [4][131]</sup>  
Disclaimer: IANAL.  
• If above steps are not working well to achieve your goal/objectives, then, one of the option you have is: "Transpile" the entire (upstream) software into the "destination" computer language which is your native computer language which you have LEARNED & understand better. By the way, this is not an easy option.  
• So begin with by creating a new project in GitHub<sup>[1][193]</sup>, BitBucket<sup>[1][194]</sup>, GNU-Savannah<sup>[1][195]</sup>, SourceForge<sup>[1][196]</sup>, GitLab<sup>[1][197]</sup>, etc etc various open-source code collaboration repository sites<sup>[1][77]</sup> (aka: SCH=Source-Code-Hosting), choose such site where more devs with higher-skill on that "destination" computer language are hanging-out, and posses friendly collaborative spirit . Or, create project in multiple code-collaboration sites & SYNC each one after each code-update . Or, load Git<sup>[1][198], [2][199], [3][200]</sup> VCS (version control software<sup>[1][201]</sup>) in your own server or personal computer, & put your transpiled code in it. (Repo=Repository)  
• Transpile a specific version of upstream software inside your own computer, then immediately upload output source-code of transpilation, into your SCH or VCS, either publish it publicly if you want to share it , Or create "private"-type repo (without publishing it publicly) . If you're skilled enough to develop all side by yourself, then "private"-type repo is useful, Or, keep it "private" until you completely convert all remaining `Go` into `C/C++` . If you publish publicly then other devs/users can see & may join to improve it or contribute in it.  
• In source-code conversion/transformation steps, if input source-code is `GPL` licensed, then output also have to be licensed under `GPL` (in most cases. CWPL) . And without all copyright-holder(s) & code-contributor's permission, the `GPL` license (generally) cannot be changed into another license . When input source-code is licensed under `Apache`, `BSD`, `MIT`, etc (or code was released in Public Domain) then output can have same Or different license . If you use or have used your own hand, eye, brain to transform/transpile (aka: source-to-source code conversion) manually some portions or significant portions of source-code, then you can claim copyright ONLY on the portions of code which you yourself have manually by yourself modified or transformed or written (without using any machine/software based transpilation), so in such case you can add your name under the input/"upstream" software's copyright-holder(s) name, in the destination language (here `"C/C++"`) code . If you have used machine or mechanized process or software to do complete code transpilation, then you cannot claim any copyright on any portion which were transpiled in such way (because, a machine has done it, not you), and in such case, input/"upstream" software's copyright-holder(s) name(s) must be added/declared back into the destination/output source-code, (and again, you cannot add your name under those "upstream"/input software's copyright-holders).<sup>[1][202]</sup>&#160;  If you have seen (input) source-code or source-algorithms, and then if you have written / transformed those algorithms with your own hand, eye, brain, etc manually by yourself into a DIFFERENT destination/output language based code, here `C/C++`, only then, it is a totally new work done/created by you, (and if input & output has same language, then you can only see "algorithms" of source-code, not the source-code itself, to create "new work", otherwise it will be treated as a "derivative work"), so in such "new work" case, you can add your name as copyright-holder, without adding "upstream"/input software's previous copyright-holder(s), & you can also use whichever license you prefer, for output code.  
  Disclaimer: IANAL. CWPL.  
• Usually, in a transpiled output/destination code , many many code-portions have to be re-worked/re-written, to functionally perform same-way as "upstream" (aka: input source-code) software , especially those portions, which you did/could not transpile during manual transpilation/transformation process, and, there will also be many many non-transpiled source-code portions, when you have used mechanized (or automated) transpilation process or transpiler software, as these tools are not yet capable to transpile (all type of codes) completely, and instead transpiles only a subset(smaller portion) of (simple or limited-advanced) input source-code language into destination/output language . So you have to write, fix, adjust, & adapt ("destination" language) source-code, and compile / run / test / improve it.  
• Once you have achieved the state, where, your (transpiled output/destination code based) software can run same-way as upstream software, then start adding your feature that you need to add . You may also find that other devs have began to join & contribute in this new project.  
• In any OPEN-SOURCE project, one of the most helpful thing to bring in more code contributors is : Addition of DETAIL COMMENTS & NOTES on each code line & section, and describe what a code-line/code-section is actually doing . So create a ToDo for yourself & for any code-contributors, that, beside improving code directly, this new project also need contribution of more detail COMMENTS & NOTES ON CODE . So that some devs can spend time on understanding + identifying each line & section & algorithm, and start adding detail general human-friendly notes & comments . Do not make comment & note helpful only for advanced devs, that creates islands & separation & division . That is opposite of open-source spirit . Everyone, even general user, should be able to understand a code line/section, after reading comments & notes.  
• If upstream software's dev also transpiles new feature, that you or your team has added into the software, then upstream dev can also add it into the upstream software.  
• Abbreviations : IANAL = I Am Not A Lawyer . CWPL = Consult With Professional Lawyer.  
<br />


  [1]: https://cs.stackexchange.com/questions/67284/
  [2]: https://github.com/elliotchance/c2go#usage
  [3]: https://stackoverflow.com/questions/8788866/
  [4]: https://github.com/Konstantin8105/c4go#example-with-c-pointers-and-c-arrays
  [5]: https://bravenewgeek.com/go-is-unapologetically-flawed-heres-why-we-use-it/
  [6]: https://www.yager.io/programming/go.html
  [7]: https://www.toptal.com/go/4-go-language-criticisms
  [8]: https://www.cvedetails.com/vulnerability-list/vendor_id-14185/Golang.html
  [9]: https://www.cvedetails.com/vulnerability-list.php?vendor_id=14185&product_id=29205
  [10]: https://www.cvedetails.com/vulnerability-list/vendor_id-14185/product_id-36900/Golang-Crypto.html
  [11]: https://cxsecurity.com/cveproduct/13980/26095/go/
  [12]: https://security.stackexchange.com/questions/194557/
  [13]: https://tomassetti.me/how-to-write-a-transpiler/
  [14]: https://github.com/GridProtectionAlliance/go2cs
  [15]: https://github.com/yanghuan/CSharp.lua
  [16]: https://github.com/davidm/lua2c
  [17]: https://github.com/aspnet/AspNetCore/tree/master/src/Components
  [18]: https://github.com/WebAssembly/wabt/tree/master/wasm2c
  [19]: https://github.com/lpereira/gomoku
  [20]: http://www.softwarepreservation.org/projects/c_plus_plus
  [21]: http://www.comeaucomputing.com/
  [22]: https://github.com/mukadr/go2c
  [23]: https://github.com/xyproto/go2cpp
  [24]: https://github.com/vaquierm/GoLite_Transpiler
  [25]: https://github.com/ASDAlexander77/cs2cpp
  [26]: https://github.com/AlexAlbala/Alter-Native
  [27]: https://github.com/dotnet/corert
  [28]: https://github.com/onelang/OneLang
  [29]: https://github.com/terotests/Ranger
  [30]: https://github.com/Theodus/go-transpiler
  [31]: https://en.wikipedia.org/wiki/Source-to-source_compiler
  [32]: https://en.wikipedia.org/wiki/Abstract_syntax_tree
  [33]: https://en.wikipedia.org/wiki/Lexical_analysis
  [34]: https://en.wikipedia.org/wiki/Syntax_analysis
  [35]: https://en.wikipedia.org/wiki/Comparison_of_parser_generators
  [36]: https://en.wikipedia.org/wiki/Semantic_analysis_%28compilers%29
  [37]: https://en.wikipedia.org/wiki/Intermediate_representation
  [38]: https://en.wikipedia.org/wiki/Intermediate_language
  [39]: https://en.wikipedia.org/wiki/Metaprogramming
  [40]: https://en.wikipedia.org/wiki/Natural_language_processing
  [41]: https://en.wikipedia.org/wiki/Finite-state_machine
  [42]: https://en.wikipedia.org/wiki/Automata-based_programming
  [43]: https://en.wikipedia.org/wiki/Parser_generator
  [44]: https://en.wikipedia.org/wiki/Parsing#Computer_languages
  [45]: https://devopedia.org/transpiler
  [46]: https://stackoverflow.com/questions/29193069/
  [47]: https://engineering.mongodb.com/post/transpiling-between-any-programming-languages-part-1
  [48]: https://en.wikipedia.org/wiki/Freedom_of_Information
  [49]: http://www.unesco.org/new/en/communication-and-information/freedom-of-expression/freedom-of-information/about/
  [50]: https://www.ohchr.org/EN/NewsEvents/Pages/RightToKnow.aspx
  [51]: https://en.wikipedia.org/wiki/Freedom_of_speech
  [52]: https://www.un.org/en/sections/issues-depth/human-rights/
  [53]: https://benchmarksgame-team.pages.debian.net/benchmarksgame/
  [54]: https://julialang.org/benchmarks/
  [55]: https://attractivechaos.github.io/plb/
  [56]: https://github.com/drujensen/fib
  [57]: http://www.hildstrom.com/projects/langcomp/index.html
  [58]: https://github.com/kostya/benchmarks
  [59]: https://modelingguru.nasa.gov/docs/DOC-2783
  [60]: https://cs.stackexchange.com/questions/40400/
  [61]: https://cs.stackexchange.com/questions/71979/
  [62]: https://en.wikipedia.org/wiki/The_Computer_Language_Benchmarks_Game
  [63]: https://benchmarksgame-team.pages.debian.net/benchmarksgame/q6600/which-programs-are-fastest.html
  [64]: https://en.wikipedia.org/wiki/Comparison_of_programming_languages_%28basic_instructions%29
  [65]: https://en.wikipedia.org/wiki/Comparison_of_programming_languages_%28syntax%29
  [66]: https://en.wikipedia.org/wiki/Higher-order_function#Support_in_programming_languages
  [67]: https://en.wikipedia.org/wiki/Operator_%28computer_programming%29#Operator_features_in_programming_languages
  [68]: https://en.wikipedia.org/wiki/Comparison_of_programming_languages_%28object-oriented_programming%29
  [69]: https://en.wikipedia.org/wiki/Constructor_%28object-oriented_programming%29
  [70]: https://en.wikipedia.org/wiki/Exception_handling_syntax
  [71]: https://github.com/mewbak/go-transpiler
  [72]: https://github.com/gopherc/goc
  [73]: https://github.com/supercoww/go-transpiler
  [74]: https://github.com/aniketp/meego
  [75]: https://stackoverflow.com/questions/6498850/
  [76]: https://stackoverflow.com/questions/737257/
  [77]: https://stackoverflow.com/questions/15970804/
  [78]: https://stackoverflow.com/questions/1833484/
  [79]: https://stackoverflow.com/questions/5050349/
  [80]: https://github.com/ponyatov/llcc
  [81]: https://sourceforge.net/projects/ctocpp/
  [82]: https://github.com/JuliaComputing/llvm-cbe
  [83]: https://github.com/thepowersgang/mrustc
  [84]: https://sourceforge.net/projects/java2c/
  [85]: https://github.com/raphaelcohn/java2c
  [86]: https://github.com/badlogic/jack
  [87]: https://developers.google.com/j2objc/
  [88]: https://stackoverflow.com/questions/4650243/
  [89]: https://nuitka.net/
  [90]: https://github.com/Nuitka/Nuitka
  [91]: https://github.com/lukasmartinelli/py14
  [92]: https://github.com/gaurav139v/Transpiler
  [93]: https://github.com/mbdevpl/transpyle
  [94]: https://sourceforge.net/projects/py2cmod/
  [95]: https://rpython.readthedocs.io/en/latest/getting-started.html
  [96]: https://foss.heptapod.net/pypy/pypy/blob/branch/default/rpython/translator
  [97]: https://github.com/alexander-jackson/ptc
  [98]: https://sourceforge.net/projects/boomerang/
  [99]: https://github.com/avast/retdec
  [100]: https://github.com/xor2003/masm2c
  [101]: https://en.wikibooks.org/wiki/X86_Assembly/MASM_Syntax
  [102]: https://github.com/frranck/asm2c
  [103]: https://github.com/nemerle/dcc
  [104]: https://sourceforge.net/projects/asmeta/
  [105]: https://github.com/anteraaron/CPP-to-Assembly-to-CPP
  [106]: https://github.com/andrei-markeev/ts2c
  [107]: https://github.com/AshutoshFreak/Perl2C
  [108]: https://github.com/matthew-c21/LispTranspiler
  [109]: https://common-lisp.net/project/ecl/main.html
  [110]: https://gitlab.com/embeddable-common-lisp
  [111]: https://alexalbala.github.io/Alter-Native/
  [112]: https://sourceforge.net/projects/hurley/
  [113]: https://github.com/amaiorano/TinyCompiler
  [114]: https://github.com/Mulan-Szechuan-Sauce/javelin
  [115]: https://github.com/yakir22/ts2cpp
  [116]: https://github.com/NishanthSpShetty/crust
  [117]: https://github.com/jameysharp/corrode
  [118]: https://github.com/immunant/c2rust
  [119]: https://github.com/PeterReid/cparser-to-rust
  [120]: https://gitlab.com/citrus-rs/citrus
  [121]: https://github.com/immunant/tinycc-rs
  [122]: https://github.com/konchunas/pyrs
  [123]: https://github.com/hegza/serpent-rs
  [124]: https://github.com/timothypratley/rustly
  [125]: https://github.com/rambler-digital-solutions/rusby
  [126]: https://github.com/echeran/kalai
  [127]: https://github.com/phaux/rustee
  [128]: https://gitlab.com/the-language/lua2rust
  [129]: https://objectivec2swift.com/#/converter/code/
  [130]: https://github.com/LuizZak/SwiftRewriter
  [131]: https://github.com/elliotchance/c2go
  [132]: https://github.com/Konstantin8105/c4go
  [133]: https://github.com/minio/c2goasm
  [134]: http://en.wikibooks.org/wiki/X86_Assembly/GAS_Syntax
  [135]: https://en.wikibooks.org/wiki/X86_Assembly/NASM_Syntax
  [136]: https://github.com/harrego/ape
  [137]: https://github.com/diogovk/c2nasm
  [138]: https://stackoverflow.com/a/20743090/3553808
  [139]: https://stackoverflow.com/a/27232672/3553808
  [140]: https://github.com/yewstack/yew
  [141]: https://stackoverflow.com/questions/44761748/
  [142]: https://github.com/afrog33k/SharpNative
  [143]: https://github.com/zezba9000/CSharpTranspiler
  [144]: https://github.com/reignstudios/CS2X
  [145]: https://github.com/mbergin/gotopython
  [146]: https://github.com/gopherjs/gopherjs
  [147]: https://github.com/tardisgo/tardisgo
  [148]: https://github.com/DAddYE/gruby
  [149]: https://github.com/CreativeInquiry/go2json
  [150]: https://golang.org/cmd/compile/
  [151]: http://dtrace.org/blogs/wesolows/2014/12/29/golang-is-trash/
  [152]: https://sourceforge.net/projects/roslyn.mirror/
  [153]: https://github.com/jtransc/jtransc
  [154]: https://spoon.gforge.inria.fr/
  [155]: https://github.com/SpoonLabs/spoon-examples
  [156]: https://haxe.org/
  [157]: https://people.eecs.berkeley.edu/~necula/cil/
  [158]: https://coccinelle.gitlabpages.inria.fr/website/
  [159]: https://github.com/coccinelle/coccinelle
  [160]: https://en.wikipedia.org/wiki/Coccinelle_%28software%29
  [161]: https://www.progsbase.com/
  [162]: https://jarble.github.io/transpiler/
  [163]: https://github.com/jarble/transpiler/
  [164]: https://en.wikipedia.org/wiki/List_of_algorithms#Computer_science
  [165]: https://en.wikipedia.org/wiki/Programming_idiom
  [166]: https://github.com/pseudo-lang/pseudo
  [167]: https://en.wikipedia.org/wiki/Heterogeneous-compute_Interface_for_Portability
  [168]: https://github.com/ROCm-Developer-Tools/HIPIFY
  [169]: https://github.com/ROCm-Developer-Tools/HIP
  [170]: https://github.com/ROCm-Developer-Tools/HIPIFY/blob/master/README.md
  [171]: https://github.com/cu2c/cu2c
  [172]: https://en.wikipedia.org/wiki/List_of_program_transformation_systems
  [173]: https://www.rascal-mpl.org/
  [174]: https://en.wikipedia.org/wiki/RascalMPL
  [175]: https://github.com/usethesource/rascal
  [176]: https://www.jetbrains.com/mps/
  [177]: https://github.com/JetBrains/MPS
  [178]: https://www.semanticdesigns.com/Products/DMS/DMSToolkit.html
  [179]: https://github.com/rose-compiler/rose
  [180]: https://github.com/raff/walkngo
  [181]: https://github.com/staticafi/llvm2c
  [182]: https://github.com/petrv7/llvm2c
  [183]: https://en.wikipedia.org/wiki/Preprocessor
  [184]: https://unix.stackexchange.com/questions/26284/
  [185]: https://stackoverflow.com/questions/1583219/
  [186]: https://stackoverflow.com/questions/15920276/
  [187]: https://stackoverflow.com/questions/1251999/
  [188]: https://sourceforge.net/projects/re2c/
  [189]: https://stackoverflow.com/questions/1333813/
  [190]: https://stackoverflow.com/questions/55789226/
  [191]: https://stackoverflow.com/questions/10523415/
  [192]: https://unix.stackexchange.com/a/607424/367237
  [193]: https://en.wikipedia.org/wiki/GitHub
  [194]: https://en.wikipedia.org/wiki/Bitbucket
  [195]: https://en.wikipedia.org/wiki/GNU_Savannah
  [196]: https://en.wikipedia.org/wiki/SourceForge
  [197]: https://en.wikipedia.org/wiki/GitLab
  [198]: https://git.kernel.org/pub/scm/git/git.git/
  [199]: https://git-scm.com/
  [200]: https://en.wikipedia.org/wiki/Git
  [201]: https://en.wikipedia.org/wiki/Comparison_of_version_control_software
  [202]: https://opensource.stackexchange.com/questions/10521/
